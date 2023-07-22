---
dg-publish: true
---

#category-theory 

Quelques choses qu'on veut représenter:
- Abstraction (soustraire l'inutile)
- Composition
- Identité

Il y a plusieurs manières d'être la même chose. Deux choses peuvent être exactement identiques, ou juste suffisamment similaires pour ce qu'on veut en faire.

# Catégorie

Une catégorie $\mathcal{C}$ est:
- des objets/points (parfois un ensemble, parfois plus grand)
- des morphismes/flèches (souvent un ensemble, parfois plus grand)
	pour chaque morphisme $f$, un objet $\text{Dom}(f)$ et un autre $\text{Cod}(f)$ qui correspondent respectivement au départ et à l'arrivée de la flèche
	on note $\mathcal{C}(A,B)$ la collection (souvent un ensemble) de morphismes de $A$ vers $B$

![[Catégories Illustration Catégorie.excalidraw|100%]]
- les morphismes composent
	$\text{Cod}(f) = \text{Dom}(g) \implies \exists g \circ f,\, \text{Dom}(g\circ f) = \text{Dom}(f) \land \text{Cod}(g\circ f) = \text{Cod}(g)$

![[Catégories Composition.excalidraw|100%]]

- la composition est associative (ceci sera **crucial** lors du dessin de diagrammes)
	$f \circ (g \circ h) = (f\circ g) \circ h$

- il existe un morphisme identité pour chaque objet qui le caractérise
	$\forall A, \exists \text{id}_{A}, \forall x, \forall f\in \mathcal{C}(x, A), \forall g \in \mathcal{C}(A,x), \quad g\circ\text{id}_{A}=g \,\land \, \text{id}_{A}\circ f=f$

> Ceci n'est pas la définition la plus rigoureuse, mais elle suffira

> On peut se demander que sont les objets ? Ils sont primitifs, ils n'ont aucune propriétés et leur seule utilité est d'indiquer les bouts des flèches !

> Entre deux objets $A$ et $B$, il peut y avoir autant de flèches que l'on veut (ou aucune), dans les deux sens.

> Une catégorie dont les objets forment un ensemble est dite "petite". Il existe une catégorie des petites catégories notée $\mathbf{Cat}$.

# Un exemple clef

En programmation il existe une catégorie qu'on utilise tout le temps, on la nommera $\mathcal{Hask}$ (car on utilisera haskell, mais elle est valable dans les autres langages fortement typés).
Dans cette catégories, un objet est un type et un morphisme est une fonction. Si un type est un ensemble, on se retrouve dans la catégorie $\mathbf{Ens}$ des ensembles avec des fonctions pour morphismes.

> On peut vérifier les lois des catégories pour se convaincre qu'en effet, elles en sont.

> Dans la catégorie $\mathbf{Ens}$, certes un objet $A$ est un ensemble, mais on "oublie" leur contenus. On connaît juste les fonctions entrantes et sortantes.

> Dans $\mathcal{Hask}$ et $\mathbf{Ens}$, on a `id x = x` $\big/$ $id_{A}(x)=x$, et on l'oublie

On peut retrouver toutes les propriétés d'un type/ensemble juste en regardant les morphismes. C'est de l'abstraction extrême.
