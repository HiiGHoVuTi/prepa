---
dg-publish: true
chapitres: Arbres, Tas
difficulté: ⭐⭐⭐
---

Rappels - Motivation
---

Dans cet exercice, on considère les files de priorité possédant les opérations suivantes 
- $\text{insérer} : \mathbb{N} \to \mathcal{F} \to \mathcal{F}$
- $\text{extraire-minimum} : \mathcal{F} \to \mathbb{N} \times \mathcal{F} +1$
> le $+1$ indique le type `Option` de OCaml, on fera comme si le tas n'était jamais vide, donc on l'ignorera

1. Rappeler la complexité des deux opérations pour un tas binaire
2. Donner la complexité des deux opération si on utilisait une liste non-triée

On essaiera alors de garder cette complexité d'insertion en amortissant le coût d'$\text{extraire-minimum}$

3. Implémenter un type forêt de rosiers (arbres $n-$aires)
On suppose ensuite que chaque noeud de chaque arbre est plus petit que tous ses fils
4. Implémenter les deux opérations dans une telle forêt, et donner leur complexité

On cherchera donc à minimiser le nombre d'arbres de la fôret sans ajouter trop de temps de calcul.

Arbres Binomiaux (A.B)
---

Un A.B de hauteur $1$ est un noeud avec une liste vide de fils.
Un A.B de hauteur $n+1$ est un arbre binômial de hauteur $n$ dont la racine a un fils supplémentaire: un A.B de hauteur $n$.

1. Dessiner un arbre binômial de hauteur $1,2,3$ et $4$.
2. 
	- Donner la hauteur d'un tel arbre en fonction de son nombre total de noeuds
	- Montrer que le degré de la racine est égal à la hauteur de l'arbre

Introduisont la condition suivante: un noeud doit être plus petit que tous ses fils.

3. Déterminer une fonction $\text{merge}$ combinant deux A.B de même hauteur en respectant cette condition. On assurera une complexité en temps constant.
4. ⭐ En déduire une fonction $\text{reduce-forest}$ qui minimise le nombre d'arbres d'une forêt de rosiers, en respectant la condition d'ordre. On assurera une complexité en $\mathcal{O}(h)$.
> On fera l'hypothèse qu'un seul arbre de chaque degré existe dans la forêt. On fera en sorte que cette hypothèse soit également vérifiée en sortie de la fonction.

Analyse amortie
---

1. Déduire des parties précédentes une implémentation efficace d'une file de priorité
2. ⭐ Effectuer une analyse amortie de la complexité des fonctions utilisées

Tas de Fibonacci - Pour aller plus loin
---

Implémenter une fonction $\text{decrease-key}$ qui modifie la valeur d'un noeud, tout en satisfaisant la condition d'ordre, en temps constant.
> On pourra considérer posséder une table de hachage adaptée à l'exercice

