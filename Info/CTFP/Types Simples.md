---
dg-publish: true
---

#category-theory 

Dans cette leçon on étudie $\mathbf{Ens}$ et $\mathcal{Hask}$.

# Quelques exemples

## $\emptyset$ $\big/$ `Void`

L'ensemble vide $\emptyset$ est l'ensemble le plus important. En haskell (si on oublie $\bot$), il est représenté par le type `Void`. Ce type n'a pas d'instance.
```haskell
-- pour construire un Void, il faut déjà un Void !
newtype Void = Void Void
```

Les fonctions $f:\emptyset \to A$ sont intéressantes car il en existe une pour chaque type $A$. On l'appelle `absurde`. En effet, cette fonction est un "bluff", "si tu me donnes un élément de l'ensemble vide, je te donne un élément de $A$".

> En logique, c'est dire que toute propriété $A$ découle de la proposition fausse $\emptyset$.
> $\forall A,\quad\emptyset \implies A$

```haskell
-- le vrai nom de cette fonction est absurd
bluff :: forall a. Void -> a
bluff = bluff
```
On a alors $\text{id}_{\emptyset} = \text{absurde}$.

## $\mathcal{1}$ $\big/$`()`

L'ensemble à un seul élément $\mathcal{1}$ ou `()` en haskell est aussi très important. C'est le seul type qu'on peut "inventer à partir de rien". Il existe toujours $\mathbf{}{1}_{A} : A \to \mathcal{1}$.

```haskell
data Tautologie = Tautologie
```

> En logique, $\mathcal{1}$ est une tautologie.
> $\forall A, \quad A \implies \mathcal{1}$

```haskell
tautologie :: forall a. a -> ()
tautologie _ = ()
```

On remarque ensuite qu'il existe autant d'éléments de $A$ que de fonctions $e:\mathcal{1}\to A$. On peut dire qu'une telle fonction $e$ "choisit un élément" et on peut même définir (puis généraliser) un élément ainsi.

> On verra ceci plus tard, mais cette propriété vient du fait que $A^{\mathcal{1}} \cong A$.

> On verra plus tard que le type à $n$ éléments $\mathcal{N}$ est construit par coproduit successif de $\mathbb{1}$

## $\mathcal{2}$ $\big /$ `Bool`

Une fonction $p:A\to \mathcal{2}$ est appelée un "prédicat" sur $A$.