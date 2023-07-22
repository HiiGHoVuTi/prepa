---
dg-publish: true
---

#category-theory 

Dans cette leçon on se place dans une catégorie arbitraire $\mathcal{C}$ et on se servira de l'intuition du produit cartésien $\times$ dans $\mathbf{Ens}$.

Un produit cartésien de deux ensembles $A \times B$ est l'ensemble suivant
$$
A \times B = \{ (a,b) \big | a\in A, b\in B \}
$$

De quelles propriétés peut-on se servir pour "catégoriser" le produit ?

Il existe une fonction $p:A\times B \to A$ et une fonction $q:A \times B \to B$ peu importent $A$ et $B$. Ceci suffit à caractériser le produit, car ceci montre qu'il "contient" $A$ et aussi $B$, ce qui est sa propriété caractéristique.

# Produit dans une catégorie

On procède par [[Objets Terminaux et Initiaux#Construction Universelle|Construction universelle]] du produit de $a$ et $b$, noté $a \times b$, avec
- La catégorie diagramme est $\mathbb{3}$ avec deux projections $p:\mathcal{3} \to 1$ et $q:\mathcal{3} \to 2$. On fixera $1 \to a$ et $2 \to b$. 

> on verra qu'une telle construction (un sommet qui factorise une catégorie discrète) s'appelle un cône, et qu'on l'utiliser pour créer le produit de $n$ objets

- Pour deux candidats $c,c'$, on dit que $c'\leq c \iff$ il existe un unique morphisme $m:c'\to c$ qui factorise $p'$ et $q'$

$$
\begin{align}
p\circ m &= p' \\
q \circ m &= q'
\end{align}
$$

![[Produits - Illustration Produit.excalidraw|100%]]
> la flèche en pointillés insiste sur l'unicité de $m$.

Dans $\mathcal{Hask}$, le produit est le $2$-uplet:
```haskell
type Produit a b = (a,b)
p :: Produit a b -> a
p (x,_) = x
q :: Produit a b -> b
q (_,x) = x
```
Mais d'autres produits existent, par exemple:
```haskell
type Produit a b = (a, b, Int)

type ProduitIntBool = Int
qIntBool _ = True
```
Mais on peut facilement trouver un morphisme $m$ qui factorise les deux transformations.

Une fois la construction faite, on se souviendra du dessin suivant:

![[Produits - Petite Illustration.excalidraw|100%]]

> on peut alors se dire que $p$ et $q$ sont "premiers entre eux" si et seulement si ils sont les projections du vrai produit.