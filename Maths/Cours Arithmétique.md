---
dg-publish: true
order: 7
---

#maths/cours 

# Divisibilité et division [[Trivia/Euclide|Euclidienne]]

## Définition

Soient $a,b\in \mathbb{Z}$, on dit que $a$ divise $b$ noté $a|b$ si et seulement si il existe $c\in \mathbb{Z}$ tel que $b=ac$. On dit que $a$ est diviseur de $b$ et que $b$ est multiple de $a$. La négation se note $a \not\mid b$

>[!remark]- Multiples 
> L'ensemble des multiples de $a$ noté $a\mathbb{Z}$ est l'ensemble suivant $\{ ak\;;\; k\in \mathbb{Z} \}$. 

## Propriétés

### Lemme

Si $a,b\in \mathbb{Z} \setminus \{ 0 \}$ et $a$ divise $b$ alors $\left| a \right| \leq \left| b \right|$.

>[!tip]- Preuve
>$\left| c \right|\geq 1$

### Proposition

Soient $a,b,c\in \mathbb{Z}\setminus \{ 0 \}$ alors:

- $a\mid b \text{ et } b\mid c \implies a\mid c$
- $a\mid b \text{ et } a\mid c\implies a\mid b+c$
- $a\mid b \implies a\mid bc$

>[!remark]- Ordre
>La divisibilité est une relation d'ordre sur $\mathbb{N}$ mais pas sur $\mathbb{Z}$
>>[!tip]- Preuve
>>$-1 \mid 1$ et $1 \mid -1$ mais $-1 \neq 1$

## Division [[Euclide|Euclidienne]]

Si $a\in \mathbb{Z}$ et $b\in \mathbb{Z} \setminus \{ 0 \}$, il existe un unique couple $(q,r)\in\mathbb{Z}\times \mathbb{N}$ tel que

$$
a = bq + r,\quad r<\left| b \right|
$$

![[Preuve - Existance et Unicité Division Euclidienne]]

>[!bug]- Représentation
>On préfèrera prendre un intervalle symétrique par rapport à $0$ de longueur $\left| b \right|-1$.
>Par exemple, pour $3$, on prendra $\{ -1,0,1 \}$

# Congruences et anneau $\mathbb{Z}/n\mathbb{Z}$

## Congruence

Soient $n\in \mathbb{Z}^{*}$, $a,b\in \mathbb{Z}$, on a $a$ congru à $b$ noté $a\equiv b[n]$ si et seulement si $c\mid b-a$.

## Proposition

Les congruences sont [[Ensembles#Relations|symétriques]] et [[Ensembles#Relations|transitives]] ainsi que compatibles avec les opérations de l'[[Introduction aux Structures Algébriques#Anneau - Définition|anneau]] $\mathbb{Z}$.

![[Preuve - Produit Congruences]]

## Quelques propriétés immédiates

- $a\equiv b[n] \implies ac \equiv bc [n]$
- $a\equiv b[np] \implies a\equiv b[n]$

## Anneaux $\mathbb{Z}/n\mathbb{Z}$

La congruence définit une relation d'équivalence sur $\mathbb{Z}$ compatible avec l'addition et la multiplication. On a donc une structure d'[[Introduction aux Structures Algébriques#Anneau - Définition|anneau]] sur les [[Ensembles#Définition d'une classe d'équivalence|classes d'équivalence]] modulo $n$.
$$
\mathcal{C\ell}_{\equiv [n]}(x) + \mathcal{C\ell}_{\equiv [n]}(y) = \mathcal{C\ell}_{\equiv [n]}(x+y)
$$
Le neutre de l'addition est alors $\mathcal{C\ell}_{\equiv [n]}(0)$ et le neutre de la multiplication est $\mathcal{C\ell}_{\equiv[n]}(1)$.
On note cet anneau $\mathbb{Z} / n\mathbb{Z}$.

>[!warning]- Pas d'intégrité
![[Introduction aux Structures Algébriques#Intégrité]]
>par exemple, dans $\mathbb{Z} /6\mathbb{Z}$, on a $2 \neq 0 \neq 3$ mais $2 \times 3 = 0$

# Idéaux

## Définition 

Soient $A$ un anneau commutatif et $I$ une partie de $A$, on dit que $I$ est un idéal de $A$ ssi
- $(I, +)$ est un sous-groupe de $(A,+)$
- $x\in I,y\in A \implies xy \in I$

## Proposition 

Soient $I,J$ des idéaux, on a $I+J$ et $I \cap J$ des idéaux.

![[Maths/Preuve - Stabilité des Idéaux]]

## Sous-Groupes  de $\mathbb{Z}$

Les sous-groupes de $\mathbb{Z}$ sont de la forme $a\mathbb{Z}$ 

![[Preuve - Sous-groupes Z]]

## Sous-Groupes de $\mathbb{Z}$

Les idéaux sont les seuls sous-groupes de $\mathbb{Z}$

>[!warning] C'est un cas particulier
>En général il y a des sous-groupes non-idéaux

![[Preuve - Sous-groupes idéaux Z]]


# PGCD

## Définition 

Soient $a,b\in \mathbb{Z}$, comme $a\mathbb{Z}+b\mathbb{Z}$ est un idéal, il existe $c$ tel que $a\mathbb{Z}+b\mathbb{Z}=c\mathbb{Z}$. Il y a au moins deux $c$ valides (opposés). Par convention, on choisit $c$ positif et est appelé "plus grand commun diviseur" noté $a\land b$.

### Lemme - Cohérence avec définition lycée

Soient $a,b\in \mathbb{Z}$ et $d\in \mathbb{Z}^{*}$, on a
$$
d\mid a \text{ et } d \mid b \iff d \mid a\land b
$$
![[Maths/Preuve - Cohérence PGCD]]

### Propriétés élémentaires

- $a \land a = \left| a \right|$
- $0 \land a = \left| a \right|$
- $1 \land a = 1$
- $a \land b = b \land a$

## Algorithme d'[[Euclide]]

[[Cours Arithmétique#Propriétés élémentaires|Cas de base]]

### Cas récursif de l'algorithme d'[[Euclide]] 

Soient $a,b\in \mathbb{Z}^{*}$ et $q\in \mathbb{Z}$ alors 
$$
a\land b = (a-bq)\land b
$$

![[Maths/Preuve - Algorithme d'Euclide]]
![[Preuve - Analyse algo Euclide]]

## Identité de [[Trivia/Bezout|Bezout]]

Soient $a,b\in \mathbb{Z}$, il existe $u,v\in \mathbb{Z}$ tels que 
$$
au+bv = a\land b
$$

![[Maths/Preuve - Identité de Bezout]]

### Algorithme d'[[Euclide]] étendu

Soit $n_{0}$ le rang de terminaison de l'algorithme d'[[Euclide]].
On a donc $a\land b=b_{n_{0}}$
Il existe $(\alpha_{k},\beta_{k})\in (\mathbb{Z}^{2})^{\textlbrackdbl 1, n_{0} \textrbrackdbl}$ tels que:
$$
\alpha_{k}a+\beta_{k}b=b_{k}
$$
![[Preuve - Algorithme étendu d'Euclide]]

## Homogénéité du PGCD

Pour $a,b,c\in \mathbb{Z}^{*}$, on a:
$$
ac\land bc = \left| c \right| (a\land b)
$$

![[Maths/Preuve - distributivité PGCD]]

## Entiers premiers entre eux

### Définition 

Soient $a,b\in \mathbb{Z}$, on dit que $a$ et $b$ sont premiers entre eux ssi $a\land b=1$

### Théorème de [[Bezout]] 

L'[[Cours Arithmétique#Identité de Trivia/Bezout Bezout|Identité de Bezout]]  admet une réciproque seulement si $a\land b=1$

$$
a\land b=1 \iff \exists u,v\in \mathbb{Z}, au+bv=1
$$

![[Maths/Preuve - Théorème de Bezout]]

>[!tip] Théorème de Moi-Bezout
>Soient $a,b\in \mathbb{N}^{*}$ et $p$ premier tel que $p>a\geq b$.
>$$
>\exists u,v\in \mathbb{Z}, au+bv=p \implies a\land b=1
>$$

## Ecriture irréductible d'un rationnel

Soit $x\in \mathbb{Q}^{*}$, il existe $p,q\in \mathbb{Z}^{*} \times \mathbb{N}^{*}$ tels que $x=\frac{p}{q}$

![[Maths/Preuve - Ecriture irréductible]]

## Bezout en congruences 

En termes de congruences, le théorème de Bezout devient:
$$
a\land b = 1 \iff \exists u \in \mathbb{Z}, au\equiv 1 [b]
$$
Autrement dit, $a$ admet un inverse modulo $b$.

![[Maths/Preuve - Bezout Congruences]]

## Lemme de [[Gauss]]

Soit $a\mid bc$ et $a\land b=1$ alors $a\mid c$.

![[Maths/Preuve - Lemme de Gauss]]

En termes de congruences:
$$
bc\equiv 0[a] {\huge \text{ et }} a\land b=1 {\huge\implies} c\equiv {0}[a]
$$
>[!note]
>En termes d'anneaux, cela revient à multiplier par l'inverse de $b$ *car $b$ est inversible* !

## Généralisation

Si $kx\equiv ky[a]$ avec $k\land a=1$, on a $x\equiv y [a]$

>[!example] Polynômes
>Déterminer les racines rationnelles de $P=2x^{3}-x^{2}+2x-1$
>>[!summary]- Solution
>>Supposons $x=\frac{p}{q},p\land q=1$ racine de $P$.
>>$$
>>\begin{align}
>>2\left( \frac{p}{q} \right)^{3}-\left( \frac{p}{q} \right)^{2}+2\left( \frac{p}{q} \right)-1&= 0 \\
>>2p^{3} - p^{2}q + 2pq^{2} - q^{3} &= 0 \\
\end{align}
>>$$
>>Donc $-q^{3}\equiv 0[p]$ et $2p^{3}\equiv 0 [q]$
>>Donc $-1\equiv 0[p]$ et $2 \equiv 0 [q]$
>>Donc $p=\pm1$ et $q \in \{ -2,-1,1,2 \}$.
>>


## Racines rationnelles de polynômes 

Soit 
$$
P= \sum_{k=0}^{n} a_{k}X^{k}, \quad a_{k}\in \mathbb{Z},\quad a_{n}\neq 0 \neq a_{0}
$$
alors les racines rationnelles ont pour forme irréductible $\frac{p}{q}$ tels que:
- $p \mid a_{0}$
- $q\mid a_{n}$

![[Maths/Preuve - Racine rationnelle]]

## Produit de divibilité

Si $a\mid c$ et $b\mid c$ et $a\land b=1$ alors $ab \mid c$

![[Maths/Preuve - Produit divibilité]]

## PGCD de plusieurs entiers 

On peut définir le PGCD de $n$ entiers comme le générateur de l'idéal 
$$
\sum a_{k}\mathbb{Z} = \left({\huge \land} a_{k}\right)\mathbb{Z}
$$
## Théorème de Bezout en $n$ dimensions

$$
{\huge \land} a_{k} = 1 \iff \sum \mu _{k}a_{k} =1
$$

![[Maths/Preuve - Bezout n]]

>[!warning] Confusion 
>Ne pas confondre premiers entre eux dans leur ensemble et premiers deux à deux
>>[!example]- Exemple 
>>$\{ 6,14,21 \}$ sont premiers entre eux mais pas deux à deux
>>$6\land 14 = 2$, $14\land 21=7$, $6\land 21=3$
>>Or $6\mathbb{Z}+14\mathbb{Z}+21\mathbb{Z} = 2\mathbb{Z}+21\mathbb{Z}=\mathbb{Z}$

# Théorème des restes chinois

>[!info] [[Trivia/Restes chinois|Histoire]]
>Le théorème chinois apparaît dans un traîté de Juzhang Suhanshu.

Soient $a,b\in \mathbb{Z}$ avec $a\land b=1$ alors pour tous $\alpha ,\beta \in \mathbb{Z}$ alors le système
$$
\begin{cases}
x\equiv\alpha [a] \\
x\equiv\beta [b]
\end{cases}
$$
admet une solution $x_{0} \in \mathbb{Z}$ et l'ensemble des solutions est $x_{0}+ab\mathbb{Z}$.

![[Preuve - Restes Chinois]]

>[!info]- [[Introduction aux Structures Algébriques#Morphisme d'Anneaux|Morphisme d'Anneaux]]
>Soient $n,m \in \mathbb{Z}^{*}$ avec $n\land m=1$ alors 
>$\varphi : \mathbb{Z}/nm\mathbb{Z} \to (\mathbb{Z}/n\mathbb{Z}, \mathbb{Z}/m\mathbb{Z})$
>$\varphi = \mathcal{C\ell}[nm](k) \mapsto \mathcal{C\ell}[n](k), \mathcal{C\ell}[m](k)$
>est un isomorphisme d'anneaux
>>[!tldr] Preuve
>>![[Maths/Preuve - Morphisme Chinois]]
>>

# Plus Petit Commun Multiple

## Définition 

Soient $a,b\in \mathbb{Z}$ alors $a\mathbb{Z} \cap b\mathbb{Z}$ est un idéal donc il existe un unique entier $a\lor b$ tel que
$$
(a\lor b)\mathbb{Z} = a\mathbb{Z} \cap b\mathbb{Z}
$$
## Cohérence 

$$
a\lor b \mid c \iff a\mid c \text{ et } b\mid c
$$
![[Maths/Preuve - Cohérence PPCM]]

## Propriétés 

- $a \lor a = \left| a \right|$
- $0 \lor a = 0$
- $1 \lor a = a$
- $a\lor b = b \lor a$

## Produit PGCD PPCM

$$
(a\lor b ) \times (a\land b) = \left| ab \right|
$$
![[Maths/Preuve - Produit PGCD PPCM]]

# Nombres Premiers 

## Définition 

On dit que $p\in \mathbb{Z}$ est premier si et seulement si il a exactement deux diviseurs naturels distincts.

>[!tldr]- Premier ou non ?
>- On prouve qu'un nombre est premier en supposant $d>1$ diviseur et arrivant à une contradiction
>- On prouve qu'un nombre est composé en trouvant un diviseur $d>1$
>- Dans tous les cas, on réaliser un crible d'[[Eratosthène]]
>```haskell 
>premiers m = eratos [2..m]
>	where 
>		eratos [] = []
>		eratos (p:xs) = p : eratos (xs \\ [p, p+p ..])
>```

Soit $\mathcal{P}$ l'ensemble des nombres premiers.

## PGCD 

On a $p\land a \in \{ 1, p \}$, ainsi si $p\mid ab$ on a $p\mid a$ et $p\mid b$.

## Infinité des nombres premiers 

![[Maths/Preuve - Infinité des premiers]]

## Théorème de Factorisation

Tout $n \geq 2$ se décompose sous la forme
$$
n = \prod_{p\in \mathcal{D}\subset \mathcal{P}} p^{\alpha_{p}}
$$
![[Maths/Preuve - Factorisation Nombres Premiers]]

## Valuation $p-$adique

Soit $n\in \mathbb{N}^{*}$ et $p$ un nombre premier. On appelle valuation $p-$adique de $n$ notée $\text{val}_{p}(n)$ le plus grand entier $k$ tel que $p^{k} \mid n$

>[!tldr]- Preuve existance 
>Soit $A=\text{max}\{ k\;;\; p^{k}\mid n \}$. 
>On a $0\in A$ majorée car $p^{k}\xrightarrow[k \to +\infty]{}+\infty$ or $p^{k}\mid n \implies p^{k} \leq n$.

## Propriétés 

1. $x=y \iff \forall p\in \mathcal{P}, \text{val}_{p}(x)=\text{val}_{p}(y)$
2. $\forall p\in \mathcal{P},\text{val}_{p}(xy)=\text{val}_{p}(x)+\text{val}_{p}(y)$
3. $x\mid y \iff \forall p \in \mathcal{P}, \text{val}_{p}(x)\leq \text{val}_{p}(y)$

>[!todo]- Prolongation dans $\mathbb{Q^{*}}$ 
>On peut prolonger la valuation $p-$adique à $\mathbb{Q}^{*}$ car tout $x\in \mathbb{Q^{*}}$ et $x=\frac{a}{b}$ avec $a\land b=1$. Donc $x=\frac{p^{k}a'}{b'}$.
>On pose $\text{val}_{p}(x)=k$, c'est un morphisme surjectif de $(\mathbb{Q^{*}}, \times)$ dans $(\mathbb{Z}, +)$

![[Maths/Preuve - Propriétés p-adique]]

## PGCD et PPCM en fonction des premiers 

Soient $a,b\in \mathbb{N}^{*}$,
$$
a\land b=\prod_{p \in \mathcal{P}} p^{\text{min}\{ \text{val}_{p}(a),\text{val}_{p}(b) \}}
$$
et
$$
a\lor b = \prod_{p\in \mathcal{P}}p^{\text{max}\{ \text{val}_{p}(a),\text{val}_{p}(b) \}}
$$

![[Maths/Preuve - PGCD PPCM en p-adique]]

>[!example]- Carré Parfait 
>$n$ est un carré parfait si et seulement si toutes ses valuations $p-$adiques sont paires
>Preuve par double implication, formule du produit.

# Petit Théorème de Fermat

## Lemme

Si $p$ est premier et $k\in \textlbrackdbl 1, p-1 \textrbrackdbl$, on a $p\mid {p \choose k}$

![[Maths/Preuve - Lemme Fermat]]

## Enoncé

Pour $p$ premier et $a\in \mathbb{Z}$ alors:
$$
a^{p}\equiv a[p]
$$
donc si $p\not \mid a$, 
$$
a^{p-1} \equiv 1 [p]
$$

![[Maths/Preuve - Petit Fermat]]

# L'anneau $\mathbb{Z}/n\mathbb{Z}$

On a $\mathbb{Z}/n\mathbb{Z}$ un corps si et seulement si $n$ est premier.

>[!tldr]- Preuve
>Il faut pouvoir simplifier par tout $k$, donc que $n\land k=1$ pour tout $k$ non-nul, ainsi $n$ doit être premier.

>[!tip]- Un diviseur de $0$ n'est pas inversible !
>preuve par l'absurde

## Petit théorème de Fermat *revisité*

![[Preuve - Petit Fermat Revisité]]
