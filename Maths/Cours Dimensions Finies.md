---
dg-publish: true
order: 14
active: true
---

#maths/cours 


# Familles et Bases

Soit $\mathcal{F}=(x_{i}\in E)_{i\in \textlbrackdbl 1, n \textrbrackdbl}$ une famille indexée par.

## Famille Génératrice

$\mathcal{F}$ est *génératrice* si pour tout $v\in E$, $v$ est une combinaison linéaire des éléments de $\mathcal{F}$.

On a alors $\text{Vect}\mathcal{F}=E$.

### Propriétés

#### Surfamille Génératrice

Soit $\mathcal{F}$ génératrice, alors toute surfamille est génératrice.

#### Génératrice de Génératrice

Soient $\mathcal{G}$ génératrice et $\mathcal{F}$ quelconque à priori. Il y a équivalence entre:

1. $\mathcal{F}$ génératrice
2. Tout vecteur de $\mathcal{G}$ se décompose comme combinaison linéaire d'éléments de $\mathcal{F}$

![[Maths/Preuve - Génératrice de Génératrice]]

## Famille Libre

Soit $\mathcal{F}$ une famille, on dit qu'elle est *libre* si la seule combinaison linéaire nulle de ses éléments  est triviale (tous les coefficients doivent être nuls).
On dit d'une famille qu'elle est *liée* si elle n'est pas libre.

> Si $0$ est élément de $\mathcal{F}$ ou qu'un élément se répète alors $\mathcal{F}$ est liée.

### Propriétés

Soient $\mathcal{F}$ une famille liée et $\mathcal{G}$ une surfamille, alors $\mathcal{G}$ est liée.
Par contraposée, si $\mathcal{G}$ est libre alors $\mathcal{F}$ aussi.

#### Nouveau Membre

Soit $\mathcal{F}$ libre, il y a équivalence entre
- $\mathcal{F}\cup \{ x \}$ liée
- $x\in \text{Vect}\mathcal{F}$

![[Maths/Preuve - Nouveau Membre Famille]]

#### Décomposition Unique

Soit $\mathcal{F}$ libre et $x\in \text{Vect}\mathcal{F}$, la décomposition est unique (équivalence).

## Base

Une famille $\mathcal{B}$ de $E$ est une base de $E$ si elle est libre et génératrice.

### Caractérisation

Soit $\mathcal{B}=(e_{1},\dots,e_{n})$ une famille de $E$, on a équivalence entre
- $\mathcal{B}$ est une base
- Pour tout $x\in E$ il existe un unique $(\lambda_{1},\dots,\lambda_{n})$ tel que $x=\sum e_{i}\lambda_{i}$

Le $n-\text{uplet}$ des $\lambda_{i}$ est appelé *vecteur des coordonnées* de $x$ dans la base $\mathcal{B}$.

### Lien avec les applications linéaires

#### Caractérisations

Soit $\mathcal{F}$ une famille et $\varphi(\lambda_{1},\dots,\lambda_{n})=\sum \lambda_{k}e_{k}$
1. $\varphi$ surjective $\iff \mathcal{F}$ génératrice
2. $\varphi$ injective $\iff \mathcal{F}$ libre
3. $\varphi$ bijective $\iff$ $\mathcal{F}$ base

![[Maths/Preuve - Caractérisation Base]]

##### Corollaire

Soient $E,F$ deux espaces vectoriels, $\mathcal{B}$ base de $E$, $f\in L(E,F)$, alors
1. $f$ surjective $\iff$ $f(\mathcal{B})$ génératrice dans $F$
2. $f$ injective $\iff f(\mathcal{B})$ libre dans $F$
3. $f$ bijective $\iff f(\mathcal{B})$ base de $F$

> Preuve: on introduit $\varphi$ bijective de $\mathbb{K}^{n}$ dans $E$. 
> On étudie alors $f\circ\varphi$

###### Engendré

Si $\mathcal{B}$ est une base de $E$, alors $f(E)$ est engendré par $f(\mathcal{B})$.

### Caractérisation d'application linéaire

Soient $E,F$ des $\mathbb{K}-$espaces vectoriels, $\mathcal{B}=(e_{1}\dots e_{n})$ une base de $E$ et $\mathcal{F}=(f_{1},\dots f_{n})$ une famille quelconque de $F$, alors il existe une unique application linéaire $\varphi: E\to F$ qui associe $e_{i}$ à $f_{i}$.

> une application linéaire est entièrement caractérisée par l'image d'une base

![[Preuve - Caractérisation app lin]]

# Dimensions

## Définition

Un $\mathbb{K}-$espace vectoriel $E$ est de *dimension finie* si il existe une partie finie génératrice de $E$.
Dans le cas contraire, $E$ est un espace vectoriel de dimension infinie (relou).

>[!example] Exemples
>
| Fini         | Infini          |
| ------------ | --------------- |
| $\mathbb{K}$ | $\mathbb{K}[X]$ |
|    $\mathbb{K}^{n}$          |   $\mathbb{R}^{\mathbb{R}}$              |

### Existence

Si $E$ est de dimension finie alors $E$ admet une base.

![[Maths/Preuve - Existence Base]]

## Dimension

### Famille Liée

Soit $\mathcal{B}=(e_{1}\dots e_{n})$ et $\mathcal{F}=(f_{1}\dots f_{n+1})\subset \text{Vect}\mathcal{B}$
Alors $\mathcal{F}$ liée.

![[Maths/Preuve - Famille liée]]

#### Corollaire

Soient $\mathcal{F}=(f_{1}\dots f_{n})$ libre, $\mathcal{G}=(g_{1}\dots g_{m})$ génératrice.
Alors $\left| \mathcal{F} \right|\leq\left| \mathcal{G} \right|$.

![[Maths/Preuve - Corollaire liberté]]

#### Corollaire - Définition

Toutes les bases de $E$ ont le même cardinal, ce cardinal est appelé *dimension* de $E$ noté
$$
\text{dim}E \text{ ou } \text{dim}_{\mathbb{K}}E
$$

### Propriétés

#### Trois Propriétés

On suppose $\mathcal{F}=(f_{1}\dots f_{n})$, alors si deux des propriétés suivantes sont vérifiées, la troisième aussi:
1. $\text{dim}E=n$
2. $\mathcal{F}$ libre
3. $\mathcal{F}$ génératrice

![[Maths/Preuve – Trois propriétés]]

#### Dimension Infinie

$E$ est infini si et seulement si pour tout $n$ il existe une famille libre de ce cardinal.

![[Maths/Preuve - Dimension Infinie]]

# Théorèmes Généraux *Généraux*

## Base Incomplète

### Lemme de la base incomplète

Soient $\mathcal{L}$ une famille libre de $E$ et $\mathcal{G}$ une sur-famille de $\mathcal{L}$.
Il existe une sous-famille de $\mathcal{G}$ et sur-famille de $\mathcal{L}$ qui est une base $\mathcal{B}$.

![[Maths/Preuve - Base Incomplète]]

### Théorème de la base incomplète

Soit $\mathfrak{F}$ une famille libre de $E$ de dimension finie, alors il existe $\mathfrak{B}$ une sur-famille qui soit aussi base.

>[!tip] Preuve
>Immédiate en choisissant $\mathcal{G}=\mathfrak{F}\cup \mathcal{B}$ avec $\mathcal{B}$ une base assurée d'exister grâce à la contrainte de dimension finie.

## Sev et Dimensions

1. Soient $E$ un $\mathbb{K}-$espace vectoriel de dimension $\mathfrak{d}$, $F$ un sous-espace de $E$, alors $F$ est de dimension finie $d\leq \mathfrak{d}$ avec égalité si et seulement si $E=F$.

![[Maths/Preuve - Dimensions et sev]]

2. Soient $E$ un $\mathbb{K}-$espace vectoriel de dimension $\mathfrak{d}$, et $F$ sous-espace de dimension $d$.
Il existe un supplémentaire à $F$ de dimension $\mathfrak{d}-d$.

![[Maths/Preuve - Sev et dimensions]]


## Relations entre dimensions

Soient $E$ un $\mathbb{K}-$espace vectoriel de dimension finie et $F$ un $\mathbb{K}-$espace vectoriel, il y a équivalence entre:
1. $F$ est de dimension finie, $\text{dim}F=\text{dim}E$
2. $F$ et $E$ sont isomorphes

![[Maths/Preuve - Isomorphisme d'espaces vectoriels finis]]

### $\mathbb{K}$orollaire

Tout espace vectoriel de dimension $\mathfrak{N}$ est isomorphe à $\mathbb{K}^{\mathfrak{N}}$.

### Suites Récurrentes

Soit $F_{a,b}=\{ u;\; u_{0},u_{1}\in \mathbb{K}, u_{n+2}=au_{n+1}+bu_{n} \}$, alors $F$ est un sous-espace vectoriel de $\mathbb{K}^{\mathbb{N}}$ de dimension $2$.
Selon les solutions de l'équation $x^{2}=ax+b$
- $\mathcal{B}=((\alpha^{n}_{1}),(\alpha_{2}^{n}))$ si deux racines
- $\mathcal{B}=((\alpha^{n}),(n\alpha^{n}))$ si $\alpha$ double

![[Maths/Preuve - Suites Récurrentes]]

La base déduite est nulle.
On cherchera des suites géométriques de raison $\alpha$ dans $F_{a,b}$, soit
$$
\alpha^{n+2}=a\alpha^{n+1}+b\alpha^{n} \iff \alpha^{2} = a\alpha+b
$$
Si deux solutions différentes, on a une base (libre et de bonne dimension).
Si la racine est double, on a $a^{2}+4b=0$ et $\frac{a}{2}$ la racine. On remarque que $n\left( \frac{a}{2} \right)^{n}$ conviendrait, montrons que c'est un élément de $F_{a,b}$:
$u_{n+2}-au_{n+1}-bu_{n} = 0$ car $b=-\left( \frac{a}{2} \right)^{2}$
Il ne manque plus qu'à montrer la liberté.

### Dimension de produits

Soient $E,F$ deux $\mathbb{K}-$espaces vectoriels de dimensions finies, alors
1. $\text{dim}E\times F=\text{dim}E+\text{dim}F$
2. Si $\mathfrak{E}$ et $\mathfrak{F}$ sont bases de $E,F$ respectivement, alors $\mathfrak{E\times F}$ est base de $E\times F$

![[Maths/Preuve - Dimension de produit]]

### Dimension de somme

Si $F$ et $G$ sone en somme directe dans $E$, alors
1. $\text{dim}(F\oplus G)=\text{dim}F+\text{dim}G$
2. $\mathfrak{F}\cup \mathfrak{G}$ est une base de $F\oplus G$

![[Maths/Preuve - Dimension de somme]]

### Formule de Grassmann

Soit $E$ un $\mathbb{K}-$espace vectoriel, et $F,G$ deux sous-espaces de dimensions finies, alors

$$
\text{dimF+G}=\text{dim}F+\text{dim}G-\text{dim}F\cap G
$$

![[Preuve - Cetelem]]

#### Corollaire

$$
\begin{align}
F\oplus G =& \,E  \\
\iff  \\
\text{dim}E = \text{dim}F+\text{dim}G &\text{ et } \text{dim}F\cap G = 0 \\
\iff \\
\text{dim} E = \text{dim}F+\text{dim}G& \text{ et } F\cap G=\{ 0 \}
\end{align}
$$

## Rang

### Rang

Soit $\mathcal{F}$ une famille d'un $\mathbb{K}-$espace vectoriel $E$, on appelle rang de $\mathcal{F}$ noté $\text{rg}F$ la dimension du $\mathbb{K}-$sous-espace-vectoriel engendré par $\mathcal{F}$
$$
\text{rg}\mathcal{F}=\text{dim} \text{Vect} \mathcal{F}
$$

Soit $f\in L(E,F)$, on appelle rang de $f$ noté $\text{rg}f$ la dimension de l'image de $f$
$$
\text{rg}f=\text{dim}f(E)
$$

Soit $\mathcal{B}$ une base de $E$, alors $\text{rg}f=\text{dim}(\text{Vect}f(\mathcal{B}))$

### Formules

Soit $\mathcal{F}=(e_{1}\dots e_{n})$

1. $\text{rg}(e_{1}\dots e_{i}\dots e_{n})=\text{rg}(e_{1}\dots \alpha e_{i}\dots e_{n})$
2. $\text{rg}(e_{1}\dots e_{i}\dots e_{n})=\text{rg}(e_{1}\dots e_{i}+\alpha e_{j}\dots e_{n})$
3. $\text{rg}(e_{1}\dots e_{i}\dots e_{j}\dots e_{n})=\text{rg}(e_{1}\dots e_{j}\dots e_{i}\dots e_{n})$
4. $\text{rg}(e_{1}\dots e_{n-1},0)=\text{rg}(e_{1}\dots e_{n-1})$

> preuve: *l'écrire*


### Théorème du rang

#### Isomorphisme à l'image

Soient $f$ une application linéaire de $E$ dans $F$ et $E_{0}$ supplémentaire de $\text{Ker}f$ dans $E$ alors $f$ est isomorphisme de $E_{0}$ dans $\text{Im}f$.

Autrement dit, $E_{0} \oplus \text{Ker}f =E \implies E_{0} \cong \text{Im}f$

![[Maths/Preuve - Lemme image iso]]

#### Théorème *fondamental* du rang

Soient $E$ un espace vectoriel de dimension finie et $f\in L(E,F)$
$$
\text{dim}E=\text{rg}f+\text{dim}\text{Ker}f=\text{dim}\text{Im}f+\text{dim}\text{Ker}f
$$

![[Maths/Preuve - Théorème du rang]]

#### Corollaire: Isomorphisme

Si $\text{dim}F=\text{dim}E<\infty$, il y a équivalence
- $f$ injective
- $f$ surjective
- $f$ bijective

>[!warning] Cette proposition n'est vraie qu'en dimension finie
> L'application $\mathcal{D}:\mathbb{K}[X]\to\mathbb{K}[X]$, $\mathcal{D}(P)=P'$ est surjective, pas injective
> L'application $\psi= P\mapsto XP$ est injective mais pas surjective

#### Corollaires $\text{Ker}$ et $\text{Im}$

Soient $f\in L(E,F),\,g\in L(F,G)$

1. $\text{Ker}(g\circ f)\supset \text{Ker}f$
2. $\text{Im}(g\circ f) \subset \text{Im}g$

3. $\text{rg} (g\circ f)\leq \text{min}\{ \text{rg}f,\text{rg}g \}$

4. $f$ surjective $\implies \text{rg}(g\circ f ) = \text{rg}g$
5. $g$ injective $\implies \text{rg}(g\circ f)=\text{rg f}$
> la composition par un isomorphisme ne change pas le rang

>[!example] Preuves
> revenir aux définitions, utiliser le théorème

## Formes Linéaires et Hyperplans

### Hyperplan

Soit $E$ un $\mathbb{K}-$espace vectoriel, $H$ un sev de $E$, on dit que $H$ est un hyperplan de $E$ si c'est le noyau d'une forme linéaire non-nulle.

### Supplémentaire à l'Hyperplan

Soit $H$ un hyperplan de $E$, et $u\in E \setminus H$ alors
$$
E=H\oplus u\mathbb{K}
$$

![[Maths/Preuve - Supp Hyperplan]]

#### Corollaire

Si $E$ est de dimension finie, $\text{dim}H=\text{dim}E-1$.
Réciproquement, si $\text{dim}\mathfrak{H}=\text{dim}E-1$, alors $\mathfrak{H}$ est un hyperplan.

![[Maths/Preuve - dim Hyperplan]]

### Caractérisation

Soient $H$ un sev de $E$ et $\mathcal{B}=(e_{1}\dots e_{n})$ base de $E$, il y a équivalence entre
1. $H$ hyperplan de $E$
2. $\text{dim}H=n-1$
3. $x=\sum_{k=1}^{n} a_{k}e_{k} \in H \iff \sum_{k=1}^{n} a_{k}\lambda_{k}=0$ (équation d'hyperplan)

![[Maths/Preuve - Caractérisation hyperplan]]

#### Corollaire

Soient $(H_{i})$ $\mathfrak{p}$ hyperplans, on a alors
$$
\text{dim} {\huge\cap}^{\mathfrak{p}}_{i=0} \,H_{i} \geq n-\mathfrak{p}
$$

![[Maths/Preuve - Intersection d'hyperplans]]

> réciproque vraie, à démontrer

# Divers Résultats

## Matrices

| $\mathbb{K}$-espace vectoriel   | dimension          | une base             |
| ------------------------------- | ------------------ | -------------------- |
| $\mathcal{M}_{n,p}(\mathbb{K})$ | $n\times p$        | $(E_{ij})$           |
| $\mathcal{M}_{n}(\mathbb{K})$   | $n^{2}$            | $(E_{ij})$           |
| Triangulaires sup. d'ordre $n$  |   $\frac{n(n+1)}{2}$                 |    $(E_{ij})_{j\geq i}$                  |
| Diagonales d'ordre $n$          | $n$                   | $(E_{ii})=(\delta_{i})$       |
| $S_{n}(\mathbb{K})$             | $\frac{n(n+1)}{2}$ | $(E_{ij}+E_{ji})_{j\geq i}$ |
| $A_{n}(\mathbb{K})$             | $\frac{n(n-1)}{2}$ | $(E_{ij}-E_{ji})_{j> i}$                     |

## Chad Lagrange

### Polynôme d'interpolation de Lagrange

Soient $(x_{0}\dots x_{n})\in \mathbb{K}^{n+1}$ des scalaires *différents* auxquels on associe $(y_{0}\dots y_{n+1})\in \mathbb{K}^{n+1}$ quelconques.

Il existe un unique polynôme $P\in \mathbb{K}_{n}[X]$ tel que pour tout $i$, $P(x_{i})=y_{i}$.

![[Maths/Preuve - Interpolation Lagrange]]

#### Formule Explicite

##### Lemme - Base de Lagrange

La famille $\mathcal{L}=(L_{0}\dots L_{n})$ est une base de $\mathbb{K}_{n}[X]$.
$$
L_{k}=\frac{\prod_{i\neq k} X-x_{i}}{\prod_{i\neq k} x_{k}-x_{i}}
$$


![[Maths/Preuve - Lemme Langrange]]

##### Formule

$$
P=\sum_{j=0}^{n}y_{j}L_{j}
$$

#### Interpolation de Lagrange-Hermite

Soient $(x_{0}\dots x_{n})$ distincts deux à deux et $(y_{0}\dots y_{n}),(z_{0}\dots z_{n})$.
Il existe un unique polynôme dans $\mathbb{K}_{2n+1}[X]$ tel que
$$
P(x_{i})=y_{i} \quad\text{ et} \quad P'(x_{i})=z_{i}
$$

![[Maths/Preuve - Lagrange-Hermite]]

