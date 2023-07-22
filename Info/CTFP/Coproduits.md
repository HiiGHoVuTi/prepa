---
dg-publish: true
---

#category-theory 

Dans cette leçon on parle de la [[Objets Terminaux et Initiaux#Construction Opposée|construction opposée]] du [[Produits|produit]], le coproduit. On verra ensuite ses utilisations en programmation pour construire un algèbre des types.

# Produit et Coproduit

Le coproduit (ou somme) de $a$ et $b$ noté $a+b$ (sur le concept, $a \times^{\text{op}} b$) est l'opposé d'un produit. Au lieu d'avoir des *pro*jections, il est muni d'*in*jections ($i$ et $j$).

(à gauche le produit, à droite le coproduit)

![[Coproduits - Illustration Produit & Coproduit.excalidraw|100%]]

# En programmation

On connaît le produit dans $\mathcal{Hask}$, c'est la paire `(,)`. Mais qu'est-ce que le coproduit ?

Regardons $\mathbf{Ens}$. On veut un ensemble a+b qui contiendrait les éléments de a et de b, et rien d'autre. Mais ce n'est pas l'union a∪b, c'est en réalité l'union discriminée a⊔b, car il existe un unique morphisme de a∪b vers a⊔b mais deux morphismes dans l'autre sens. Notre classement nous indique donc que le coproduit doit "se souvenir d'où les éléments viennent".

Et c'est ce qui existe en programmation ! Dans $\mathcal{Hask}$, le coproduit est l'énumération. En `haskell`, 
```haskell
newtype Coproduct a b = Either a b 
```
 > rappel:
 > ```haskell
 > data Either a b = Left a | Right b
 > ```

En `C++` on utiliserait une struct ou une classe avec plusieurs constructeurs.

> On remarque qu'un coproduit a deux constructeurs $\iota_{1}$ et $\iota_{2}$ alors que le produit a deux destructeurs $\pi_{1}$ et $\pi_{2}$.
```haskell
pi1 :: (a,b) -> a
pi2 :: (a,b) -> b

iota1 :: a -> Either a b
iota2 :: b -> Either a b
```

 Il n'y a pas de manière de détruire un coproduit ou construire un produit *à priori*, constatez l'absurdité des signatures suivantes
```haskell
absurd1 :: a -> (a, b)
absurd2 :: Either a b -> a
```

On verra comment exploiter ces types bientôt grâce à l'algèbre des types. En programmation, on appelle ceci du pattern-matching, destructuring, $\dots$

# $\dots$ et ça suffit ?

Si on considère un système de type à l'isomorphisme, il suffit du type vide, de l'unité, produit et coproduit pour former un système de type avec tous les types possibles.

- Produits: `(,)` en haskell, objets en JS, structs en `C++`
- Copduits: `Either` en haskell, enums en Java

> En réalité les cones et cocones seront plus pratiques car ils généralisent à plus que deux types

