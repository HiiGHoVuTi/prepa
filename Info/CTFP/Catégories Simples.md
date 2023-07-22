---
dg-publish: true
---

#category-theory 

Dans cette leçon nous allons décrire des catégories connues.

# $\mathbb{0}$ 
 Cette catégorie n'a pas d'objets ni de morphismes.

> cette catégorie n'est pas inutile, elle est utile dans $\mathbf{Cat}$

# $\mathbb{1}$
Cette catégorie a un seul objet $1$ et un seul morphisme $\text{id}_{1}$.

# Catégorie Discrète
Une catégorie discrète $n$ est une catégorie à $n$ objets $1,2,\dots,n$ et à $n$ morphismes $\text{id}_{1}, \text{id}_{2}, \dots, \text{id}_{n}$.

> on peut raisonner par récurrence sur ces catégories !

# Préordre
 Soit $\leq$ une relation de préordre sur $A$. On peut créer une catégorie où les objets sont les éléments de $A$ et un unique morphisme existe de $x$ vers $y$ si et seulement si $x \leq y$.
 
> on remarque que la présence d'$\text{id}$ exprime la réflexivité

Soit $\geq$ la relation "opposée" sur $A$. On peut créer une catégorie aussi, et elle est la catégorie *opposée* de celle-ci-dessus.

> La catégorie opposée de $\mathcal{C}$ notée $\mathcal{C}^{\text{op}}$ est la catégorie dans laquelle les flèches sont formellement renversées

> Dans cette catégorie, tous les morphismes sont moniques et épiques mais ne sont pas des isomorphismes !

On peut voir une catégorie comme un préordre mais avec plusieurs "preuves" de relations entre chaque objets. $A ≤_{f} B, \,A ≤_{g} B, \,\dots$

# Monoïde

Un monoïde $\mathcal{M}$ est une catégorie avec un seul objet $1$. Tous ses morphismes sont automatiquement composables. 

On remarque que cette définition crée un monoïde "classique". La LCI est $\circ$ et l'élément neutre est $\text{id}_{1}$. L'ensemble sous-jacent est $\mathcal{M(1,1)}$. 

> les lois des monoïdes sont automatiquement satisfaites grâce aux lois des catégories

> ex: il existe par exemple une catégorie avec un seul objet dont les morphismes sont les éléments de $\mathbb{Z}$ et où $\circ = \times$.

> un monoïde représente le système de typage faible, où il n'existe qu'un type $1$ donc où toutes les fonctions sont composables
