---
dg-publish: true
---

#category-theory 

Dans cette leçon on développe l'intuition précédente sur les types de données algébriques.

# Définition

Un système de types algébrique est fondé sur le types $\mathcal{0}$, $\mathcal{1}$ et tous les types obtentibles par produit, somme, et exponentiation (à l'isomorphisme près).

> On reste à l'isomorphisme près car en effet, `(a,(b,c)) /= ((a,b),c)` mais on a bien $(a\times b) \times c \cong a \times (b \times c)$ par exemple. 
> 
> Pareil pour $a \times b \neq b \times a$ mais $a \times b \cong b \times a$.


# Propriétés

On remarque des identités intéressantes: Si on veut implémenter un entier qui peut être soit positif soit négatif, on peut stocker un entier naturel et un booléen qui représente le signe. Ecrivons ce type de deux manières:

- `(Bool, Nat)`, soit $\text{Bool} \times \text{Nat}$ est la représentation en stockant le booléen de signe
- `Positive Nat | Negative Nat`, soit $\text{Nat} + \text{Nat}$ est la représentation par union taggée

On peut alors observer que dans ce système de types, $2\text{Nat} \cong \text{Nat} + \text{Nat}$.


## Structure de Demi-Anneau

> On rappelle qu'on travaille à l'isomorphisme près.

- Les LCI sont associatives et commutatives
- $a + \mathcal{0} \cong a$
- $a \times \mathcal{1} \cong a$
- $a × \mathcal{0} ≅ \mathcal{0}$
- $a \times (b + c) \cong a\times b + a \times c$

> Vous pouvez chercher à trouver les isomorphismes vous-mêmes ! 

## Résolution d'équations

Résolvons l'équation suivante

$$
\mathcal{L}(a) \cong 1 + a \times \mathcal{L}(a)
$$
En traduisant en code, on remarque le type suivant
```haskell
data List a = Nil | Cons a (List a)
```

Utilisons les formules connues (sans justifier rigoureusement leur validité ici)
$$
\begin{align}
\mathcal{L}(a)  & \cong 1 + a \times \mathcal{L} (a) \\
\mathcal{L}(a) - a \times \mathcal{L} (a)  & \cong 1 \\
\mathcal{L}(a) \times(1-a) &\cong 1 \\
\mathcal{L}(a) &\cong \frac{1}{1 -a} \\
\end{align}
$$
Quel rapport entre ce "quotient de types" et une liste ?
Appliquons la formule de la somme des termes d'une suite géométrique (version série)
$$
\begin{align}
\mathcal{L}(a) &\cong \frac{1}{1-a} \\ \\

\mathcal{L}(a) &\cong \sum^{\infty}_{k=0} a^{k} \\ \\

\mathcal{L}(a) &\cong 1 + a + a² + a^{3} + \dots
\end{align}
$$
Or une liste peut-être vide, contenir un élément, deux éléments, trois éléments, $\dots$
```haskell
data List a = Nil | One a | Two a a | Three a a a | ..
```

On vient de démontrer (avec une rigeur à donner la chaire de poule) que ces deux définitions sont isomorphes.

> On n'a pas justifié la résolution de cette équation mais le résultat et juste et de nombreuses méthodes existent.

> On remarque qu'on a écrit $a^{n}$, et on verra que les exposants sont également possibles avec des types, et qu'ils se généralisent le comportement des entiers naturels.
