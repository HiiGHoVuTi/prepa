---
dg-publish: true
order: 5
---
#maths/cours 

# Construction de $\mathbb{N}$

La construction de $\mathbb{N}$ est hors-programme, la voici:
L'ensemble des entiers naturels $\mathbb{N}$ est un ensemble non vide totalement ordonné possédant trois propriétés:
1. $\mathbb{N}$ ne possède pas de plus grand élément
2. toute partie de $\mathbb{N}$ non vide admet un plus petit élément
3. toute partie non vide majorée de $\mathbb{N}$ admet un plus grand élément

# Cardinal d'un ensemble fini

## Ensemble fini

Définition: un ensemble $E$ est dit fini s'il existe un entier $n$ et $\varphi$ une bijection:
$$
\varphi : E \longleftrightarrow \textlbrackdbl   1, n \textrbrackdbl
$$
## Injections et surjections de $\textlbrackdbl 1,p \textrbrackdbl$ dans $\textlbrackdbl 1,q \textrbrackdbl$

Soit $f : \textlbrackdbl 1,p \textrbrackdbl \to \textlbrackdbl 1, q \textrbrackdbl$

1. $f$ injective $\implies$ $p\leq q$
2. $f$ surjective $\implies$ $q \leq p$
3. $f$ bijective $\implies$ $p = q$

> Preuve: par récurrence

## Cardinal

Soit $f : E \longleftrightarrow \textlbrackdbl 1,n \textrbrackdbl$, on définit alors le cardinal de $E$
$$
\left| E \right| = n
$$

## Quelques Propriétés

### Bijectivité finie

Soient $E$ et $F$ finis de même cardinal et $f : E \to F$, les deux propositions suivantes sont équivalentes
1. $f$ injective
2. $f$ surjective
3. $f$ bijective

Il suffit de montrer $1. \iff 2.$

### Cardinal d'image

Si $A$ est fini et $f : A\to B$ alors:
$$
\left| f(A) \right| \leq \left| A \right|
$$

> Preuve: par récurrence

### Cardinal d'injection

Si $f$ injective et $A$ et fini alors
$$
\left| f(A) \right| = \left| A \right|
$$
### Cardinal de produit

Si $A$ et $B$ finis,
$$
\left| A \times B \right| = \left| A \right| \times \left| B \right|
$$

> ceci se généralise à tout produit fini

### Cardinal d'union disjointe

Si $A$ et $B$ finis et disjoints

$$
\left| A \cup B \right| = \left| A \right| + \left| B \right|
$$
### Cardinal d'union

Si $A$ et $B$ finis,

$$
\left| A \cup B \right| = \left| A \right| + \left| B \right| - \left| A \cap B \right|
$$
Preuve:
![[Maths/Preuve - Cardinal d'union]]


### Cardinal de Partie

Si $A$ fini et $B$ une partie de $A$,

$$
\left| A \right| \geq \left| B \right|
$$
> cas d'égalité pour $A=B$

Preuve: laissée au lecteur

### Cardinal de complémentaire

Soit $A$ une partie de $E$ fini

$$
\left| \overline{A} \right| = \left| E \right| - \left| A \right|
$$
Preuve: $E = A \cap \overline{A}$ disjoints


### Corollaire

$$
\left| {\huge \cup} A_{i} \right| \leq \sum \left| A_{i} \right|
$$
![[Maths/Preuve - Inégalité Cardinal Union]]

[[Cours Dénombrement et Ensembles Finis Exercice Cardinaux.excalidraw|Exercice]]

## Quelques cardinaux remarquables

### Lemme du Berger

- Soit $E$ un ensemble tel qu'il existe une partition de $N$ ensembles finis tous de cardinal $k$, alors $E$ est fini de cardinal $Nk$

- Soit $E$ un ensemble tel qu'il existe $k \in \mathbb{N}^{*}$ et $f : E \to F$ tel que chaque élément a $k$ antécédents, $E$ est fini de cardinal $Nk$

### Cardinal d'exponentielle

Soient $E$ et $F$ finis, alors
$$
\left| F^{E} \right| = \left| F \right|^{\left| E \right|}
$$

### Cardinal des parties

Soit $E$ fini, alors
$$
\left| \mathcal{P}(E) \right| = 2^{\left| E \right|}
$$

> se [[Preuve - Somme binomiaux|démontre]] aussi avec [[Formules Dénombrement#Somme|la formule de la somme des coéfficients binomiaux]]


### Nombre d'injections

Soient $p,n \in \mathbb{N}$ et $k$ le nombre d'injections de $\textlbrackdbl 1,p \textrbrackdbl$ dans $\textlbrackdbl 1,n \textrbrackdbl$, alors

$$
k = \frac{n!}{(n-p)!}
$$
### Permutations 

Le nombre $k$ de bijections de $\textlbrackdbl 1,n \textrbrackdbl$ dans lui-même est
$$
k = n!
$$

### Nombre de Parties 

Le nombre de parties de $k$ éléments dans un ensemble à $n$ éléments est
$$
\frac{n!}{k!(n-k)!}= {n \choose k}
$$
[[Cours Dénombrement et Ensembles Finis Exercice Poker.excalidraw|Exemples de Proba]]

## Coéfficients Binomiaux

![[Formules Dénombrement#Binomiaux]]
