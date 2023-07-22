---
dg-publish: true
---

#category-theory 

Dans cette leçon on se replace dans une catégorie arbitraire $\mathcal{C}$, mais on utilisera de l'intuition de $\mathbf{Ens}$.

# Construction Universelle

Pour effectuer une construction universelle d'une structure dans une catégorie $\mathcal{C}$, on va avoir besoin de:
- un motif à repérer (sous la forme d'une catégorie diagramme $\mathcal{D}$)
- un classement de ces motifs, pour choisir le meilleur
- une preuve qu'il y en a au moins un

# Objet Terminal

On cherche à définir $\mathcal{1}$ dans $\mathbf{Ens}$ sans parler d'éléments. Pour ceci nous utiliserons uns *construction universelle*. On se servira de la propriété qu'il existe une seule fonction de tout ensemble $A$ vers $\mathcal{1}$.

$$
\begin{align}
\forall A \exists f &: A\to \mathcal{1} \\
\forall f,g&:A\to \mathcal{1}, f=g
\end{align}
$$

> dans une catégorie $\mathcal{C}$, l'objet obtenu (s'il existe) est l'objet terminal de $\mathcal{C}$.

> dans un préordre $\leq$, un objet terminal est le plus grand élément

> un morphisme de l'objet initial $\mathcal{1}$ vers un objet $A$ est la généralisation d'un élément

# Objet Initial

On cherche à définir $\emptyset$ dans $\mathbf{Ens}$ sans parler d'éléments. Pour ceci nous utiliserons une *construction universelle*. On va utiliser l'existance d'une unique fonction de $\emptyset$ vers tout $A$.

> dans une catégorie $\mathcal{C}$, l'objet obtenu (s'il existe) est l'objet initial de $\mathcal{C}$

> on peut aussi dire que c'est l'objet initial dans $\mathcal{C}^{\text{op}}$

# Unicité

Les objets initiaux et terminaux sont uniques (à l'isomorphisme). 
Preuve:
Soient $A,B$ deux objets terminaux. Il existe alors un unique morphisme $f:A\to B$ et un unique morphisme $g:B \to A$.
On considère $h=g \circ f$. On remarque $\text{Dom}(h) = \text{Cod}(h)=A$ or il existe un unique morphisme de $A$ vers $A$, et on sait qu'$\text{id}_{A}$ existe. 
De même pour $f\circ g$ de $B$ vers $B$.
On en conclut que $h=\text{id}_{A}$ donc il existe un unique isomorphisme entre $A$ et $B$.


# Par construction universelle

- Le motif est la catégorie $\mathbb{1}$
- L'ordre $\leq$ est défini par $a \leq b \iff$ il existe un unique morphisme de $a$ vers $b$  (ou $b$ vers $a$)
- Preuve d'existence par l'exemple

# Construction Opposée

Pour chaque construction $\mathcal{S}$ dans $\mathcal{C}$, on peut obtenir sa co-construction $\mathcal{S}^{\text{op}}$ dans $\mathcal{C}^{\text{op}}$.

> La co-construction de l'objet initial est l'objet terminal et inversement. On procède de manière identique mais dans $\mathcal{C}^{\text{op}}$

![[Objets Terminaux et Initiaux 2022-11-02 20.47.10.excalidraw|100%]]
