---
aliases: [Systèmes Linéaires]
dg-publish: true
order: 13
active: true
---

#maths/cours 


# Matrices

## Définition

Une matrice à $n$ lignes et $m$ colonnes à coefficients dans $\mathbb{K}$ est une application
$$
M: \textlbrackdbl 1,n \textrbrackdbl \times \textlbrackdbl 1,m \textrbrackdbl \to \mathbb{K}
$$

On les représente
$$
\begin{pmatrix}
m_{1,1}&m_{1,2}& \dots& m_{1,m} \\
m_{2,1}&m_{2,2}&\dots& m_{2,m} \\
\dots&\dots& \ddots&\vdots \\
m_{n,1}&m_{n,2}&\dots&m_{n,m}
\end{pmatrix}
$$

On appelle $\mathcal{M}_{n,m}$ l'ensemble des matrices à $n$ lignes et $m$ colonnes

## Terminologie

| Nom       | Ensemble                            |
| --------- | ----------------------------------- |
| *Carrée*  | $\mathcal{M}_{n}=\mathcal{M}_{n,n}$ |
| *Ligne*   | $\mathcal{M}_{1,n}$                 |
| *Colonne* | $\mathcal{M}_{n,1}$                                    |

On peut extraire les lignes et colonnes d'une matrice en restreignant l'application.

On appelle *transposée* de $M$ notée $M^{T}$ ou $^{t}M$ est l'application:
$$
^tM(i,j)=M(j,i)
$$

La matrice élémentaire est l'application suivante:
$$
E_{i,j}(x,y)=\begin{cases}
1 \text{ si } x=i \text{ et } y=j \\
0 \text{ sinon}
\end{cases}
$$
On introduit le symbole de Kronecker:
$$
\delta_{i,j}=\begin{cases}
1 \text{ si } i=j \\
0 \text{ sinon}
\end{cases}
$$

### Matrices Carrées

Soit $M$ carrée,
- On dit que $M$ est *triangulaire* supérieure si $i>j \implies m_{i,j}=0$.
De même, $M$ est triangulaire inférieure si $i<j \implies m_{i,j}=0$.
On dit triangulaire stricte si $i=j\implies m_{i,j}=0$ aussi.
- On dit que $M$ est *diagonale* si $i\neq j\implies 0$.
- On dit que $M$ est *symétrique* si $M=M^{T}$ et *antisymétrique* si $M=-M^{T}$.
$S_{n}(\mathbb{K})$ est l'ensemble des symétriques et $A_{n}(\mathbb{K})$ des antisymétriques.

## Opérations

### Combinaisons linéaires

$\mathcal{M}_{n,p}(\mathbb{K})$ a une structure d'espace vectoriel pour les lois $+,\times$ définies au point.
$$
\begin{align}
(M+N)(i,j)&=M(i,j)+N(i,j) \\
(aM) (i,j)&=a(M(i,j))
\end{align}
$$

### Produit Matriciel

On définit le produit matriciel pour $A\in \mathcal{M}_{n,p}(\mathbb{K}),B\in \mathcal{M}_{p,q}(\mathbb{K})$ tel que
$$
(A\times B)(i,j)=  \sum_{k=1}^{p} A(i,k)B(k,j)
$$

> En notation "einsum", on a $(A\times B)_{i,j} = A_{i,k}B_{k,j}$

#### Nilpotence

Une matrice est dite nilpotente si il existe $n\in \mathbb{N}^{*}$ si $M^{n}=0$.

### Propriétés

##### Sous-Espaces Vectoriels

L'ensemble des matrices triangulaires sup. (resp triangulaires inf.,  diagonales, symétriques, antisymétriques) sous des sev de $\mathcal{M}_{n}$.

> On peut exprimer avec $\text{Vect}\{ E_{i,j}\;;\; P(i,j) \}$.
> On pose $\varphi(M)=M-M^{T}$ ou $+$, et on a $E=\text{Ker}\varphi$

#### Supplémentaires

On a $A_{n}(\mathbb{K})\oplus S_{n}(\mathbb{K})=\mathcal{M_{n}}$.

![[Preuve - SEV Mn Supp]]

### Bilinéarité

$$
\begin{align}
(A+\lambda B)C&=AC+\lambda(BC) \\
A(C+\lambda D)&= AC+\lambda(AD)
\end{align}
$$

![[Maths/Preuve - Bilinéarité Produit Matriciel]]

#### Application Canoniquement Linéaire

$$
\varphi_{M}(X)=MX
$$

### Structure d'Anneau

#### Matrice Identité

Il existe une unique matrice $I_{p}$ carrée d'ordre $p$ telle que $MI_{p}=M$
De même, $I_{n}$ unique telle que $I_{n}M=M$.

![[Maths/Preuve - Matrice Identité]]


#### Structure

L'ensemble $\mathcal{M}_{n}(\mathbb{K})$ muni des lois usuelles $+,\times$ est un anneau (non-intègre et non-commutatif si $n\geq 2$).

#### Sous-Anneaux

- Matrices diagonales
- Triangulaires (supérieures et inférieures)

![[Maths/Preuve - Sous-Anneaux Matrices]]

#### Transposée

$$
(AB)^{T}=B^{T}A^{T}
$$

![[Maths/Preuve - Produit Transposée]]

# Système Linéaire

## Définition

Le système linéaire $(E)$
$$
\begin{cases}
a_{11}x_{1} +a_{12}x_{2} +\dots +a_{1p}x_{p} &= b_{1} \\
a_{21}x_{1}+\dots&=b_{2} \\
\vdots \quad\vdots \quad \vdots \quad \vdots \quad \quad \ddots & \vdots \\
a_{n1}x_{1} + \dots \quad\quad\quad \;\,+ a_{np}x_{p} &= b_{n}
\end{cases}
$$

On associe à $E$ les matrices
$$
X = \begin{pmatrix}
x_{1} \\
\vdots \\
x_{p}
\end{pmatrix} ,\; A = \begin{pmatrix}
a_{11}\dots a_{1p} \\
\vdots \;\;\ddots\;\; \vdots \\
a_{n1}\dots a_{np}
\end{pmatrix} ,\; B=\begin{pmatrix}
b_{1} \\
\vdots \\
b_{n}
\end{pmatrix} 
$$

On dit que le système est homogène si $B=0$ et compatible si il admet au moins une solution.

## Structure des Solution

### Propriétés

#### Reformulation

Ces deux propositions sont équivalentes:
- $(x_{1},\dots,x_{n})$ est solution
- $AX+B$

#### Linéarité

L'ensemble des solutions d'un système linéaire homogène est un espace vectoriel.

> Preuve: faire le calcul (on passe par les matrices), et $(0\dots 0)$ est solution.

#### Solutions

$$
S_{E}=\{ X_{0}+X\;;\; X \in S_{E_{h}} \}
$$
avec $X_{0}$ solution de $E_{h}$.

![[Maths/Preuve - Solutions Système Linéaire]]

#### Cas $n<p$

Si un système linéaire homogène possède moins d'équations que d'inconnues ($n<p$), alors il admet une solution non-triviale.

## Opérations Elementaires

1. $L_{i}\leftarrow \alpha L_{i}, \quad\alpha\neq 0$
2. $L_{i}\leftarrow L_{i}+\alpha L_{j}, \quad j\neq i$
3. $L_{i}\leftrightarrow L_{j}$

On dit que deux systèmes sont équivalents si on passe de l'un à l'autre en utilisant une suite finie de ces trois opérations.

### Matrices d'opérations élémentaires

1. Permutation: $P_{ij} = I_{n}+E_{ij}+E_{ji}-E_{ii}-E_{jj}$
2. Dilatation: $D_{i}(\lambda)=I_{n}+(\lambda-1)E_{ii}$ avec $\lambda\neq 0$
3. Transvection: $T_{ij}(\alpha)= I_{n}+\alpha E_{ij}$, $i\neq j$

### Matrices Equivalentes par ligne

Deux matrices $M_{1},M_{2}$ sont équivalentes par lignes si il existe une suite finie de multiplications par des matrices d'opérations élémentaires qui permettent de passer de $M_{1}$ à $M_{2}$.

> C'est une relation d'équivalence, et on le note $\sim_{L}$

### Equivalence

Soit $(E)$ un système linéaire, $M$ sa matrice associée et $B$ sa matrice de second membre
Si le système $(E)$ est équivalent au système $(E')$ par le pivot de Gauss, alors il existe une suite de multiplications par matrices d'opérations élémentaires pour obtenir $M'$ associée et $B'$ second membre de $(E')$.

# Calcul Matriciel

## Puissances d'une matrice carrée

### Définition

On définit par récurrence $A^{0}=I_{n}$ et $A^{p+1}=A^{p}\times A=A\times A^{p}$.

### Matrices diagonales

Soit une matrice diagonale $D$, on a alors $(D^{p})_{ij}=(D_{ij})^{p}$.

### Anneau

Si $A$ et $B$ commutent,
![[Introduction aux Structures Algébriques#Sommes et Puissances]]

## Matrice Inversible

### Définition

Une matrice carrée $M$ est inversible si et seulement si il existe $U$ telle que:
$$
MU = UM=I_{n}
$$
L'ensemble $\text{GL}_{n}(\mathbb{K})$ des matrices inversible est un groupe.

### Propriétés

Si $A$ inversible, alors $A^{-1}$ inversible d'inverse $A$.
Si $A$ inversible, alors $A^{T}$ est inversible d'inverse $(A^{-1})^{T}$.
Si $A,B$ inversibles, alors $AB$ inversible d'inverse $B^{-1}A^{-1}$.

Quelques matrices inversibles:
- $\lambda I_{n}$ avec $\lambda\neq 0$
- Les matrices diagonales sans coefficient diagonal nul
- Les matrices d'opérations élémentaires

Soient $A,B$ avec $AB=I_{n}$ alors $A$ est inversible d'inverse $B$.

### Corollaire

$M$ est inversible si et seulement si 
$$
MX=\begin{pmatrix}
0 \\
\vdots \\
1 \\
\vdots \\
0
\end{pmatrix}
$$
admet une solution pour tout placement du $1$.

![[Maths/Preuve - Critère d'inversibilité]]

## Résolution d'un système linéaire

### Lemme

Résoudre $MX=(_0\dots_{1}\dots_{0})$ pour tout placement du $1$ est équivalent à résoudre $MX=B$.

### Méthode

On peut ramener l'inversion d'une matrice à une résolution de système, ou pareillement utiliser des opérations élémentaires pour passer de $MX=I_{n}B \implies I_{n}X=M^{-1}B$.

### Décomposition

Soit $M\in \text{GL}_{n}(\mathbb{K})$, alors $M$ se décompose en produit de matrices d'opération élémentaires.