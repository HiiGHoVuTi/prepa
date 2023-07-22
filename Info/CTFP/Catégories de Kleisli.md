---
dg-publish: true
---

#category-theory 

Dans cette leçon nous abordons rapidement la notion effrayante de "monade".

# Introduction, en `C++`

Votre patron vous contacte et vous demande que chaque fonction que vous avez écrit dans une bibliothèque doit désormais avoir des *logs*. Donc elles doivent toutes écrire un petit message dans un fichier texte.

Une solution rapide et sale serait d'ajouter une variable globale et de l'éditer à chaque fois:
```cpp
std::string log = "";

bool negate(bool x){
	log += "[CALLED negate]\n";
	return !x;
}
```

Cette solution a un problème, elle est certes simple, mais cache la complexité et crée une dépendance entre `negate :: Bool -> Bool` et `log`. Imaginez la catastrophe si vous essayez de paralléliser ce code.
Réimplémentons cette fonction de manière pure
```cpp
std::pair<bool, std::string> negate(bool x, std::string log) {
	return std::make_pair(!x, log + "[CALLED negate]\n");
}
```
Cette fonction est *pure* mais problématique. Elle a des effets qui n'ont rien à voir avec ce pour quoi elle est conçue. Elle n'a aucune raison de "savoir comment" concaténer deux chaînes de caractères. On veut juste qu'elle retourne une paire, sans connaître ses alentours.
```cpp
std::pair<bool, std::string> negate(bool x){
	return std::make_pair(!x, "non !\n");
}
```
Mais maintenant, qui réalise la concaténation ? Créons une fonction qui compose nos "fonctions à log"
```cpp
// composition normale
function<C(A)> compose(function<B(A)> f, function<C(B)> g){
	return [f,g](A x){
		auto y = f(x);
		auto z = g(y)
		return z;
	};
}

// composition, en concaténant les logs
function<pair<C, string>(A)> 
	compose(function<pair<B, string>(A)> f,
			function<pair<C, string>(B)> g) {
	return [f,g](A x) {
		auto y = f(x);
		auto z = g(y, y.first);
		return make_pair(z.first, y.second + z.second);
	};
}
```
Ici la composition est plus cohérente. La concaténation fait partie de la composition des fonctions, pas des fonctions elles-mêmes.

On parle de composition, y a-t-il une catégorie ?

- Composition OK !
- Identité OK !
```cpp
pair<a, string> id(a x) {
	return make_pair(x, "");
}
```

Un morphisme entre $A$ et $B$ est une fonction $f:A\to(B, \texttt{String})$

# Construction d'une Catégorie de Kleisli

Partons d'une catégorie de départ $\mathcal{C}$. Nous allons construire une catégorie de Kleisli $\mathcal{C}_{\mathcal{T}}$ avec les mêmes objets que $\mathcal{C}$ mais les morphismes et la composition modifiée.

On associe à chaque objet $A$ de $\mathcal{C}$ un autre objet $\mathcal{T}A$ toujours dans $\mathcal{C}$.

Un morphisme de $A$ vers $B$ dans $\mathcal{C}_{\mathcal{T}}$ est un morphisme de $A$ vers $\mathcal{T}B$ dans $\mathcal{C}$.

> Dans notre cas particulier, on avait $\mathcal{T}A = (A, \texttt{String})$.

![[Catégories de Kleisli - Illustration Kleisli.excalidraw]]

> Ce n'est pas possible pour tout $\mathcal{T}$, il faut que $\mathcal{T}$ soit *une monade*.