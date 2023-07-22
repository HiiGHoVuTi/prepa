---
aliases: [Espaces Euclidiens, Espaces Préhilbertien]
dg-publish: true
order: 23
active: true
---

# Produit Scalaire

On travaille dans $\mathbb{R}$

###### Définition du produit scalaire

$\braket{ - | = }: \mathbf{E}\times \mathbf{E} \to \mathbb{R}$ est un produit scalaire si et seulement si
1. Il est bilinéaire
![[Cours Déterminant#$p-$Linéarité]]
2. Il est symétrique
![[Cours Déterminant#Symétrie]]
3. Il est positif: $\braket{ x | x }\geq 0$
4. Il est défini:  $\braket{ x | x }=0\iff x=0$

Le produit scalaire est une *forme biliénaire symétrique définie positive*.

##### Exemples de référence

1. Dans $\mathbf{E}=\mathbb{R}$, $\braket{ \begin{pmatrix}x_{1}\\y_{1}\end{pmatrix} | \begin{pmatrix} x_{2}\\y_{2}\end{pmatrix}}=x_{1}x_{2}+y_{1}y_{2}$
	2. Symétrie ok
	1. Linéarité d'un côté ok (par symétrie, l'autre ok)
	3. Positivité ok
	4. Définition ok
On étend cette définition à $\mathbb{R}^{n}$.
On obtient de plus $\braket{ X | Y  }=X^{T}Y$ par identification.

2. Dans $\mathbf{E}=\mathcal{M}_{n}(\mathbb{R})$, $\braket{ M | N }=\text{Tr }M^{T}N$
	2. Symétrie (propriété de la trace)
	1. Linéarité ok (deuxième opérande)
	3. Définition et Positivité
$$
\begin{align}
\braket{ M | M } &=\sum_{i} (M^{T}M)_{ii} \\
&= \sum_{i} \sum_{j}=(M^{T})_{ij}M_{ji} \\
&= \sum_{i,j} M_{ij}^{2} \geq 0
\end{align}
$$
cas d'égalité ssi $M_{ij}=0$ donc $M=0$

3. $\mathbf{E}=\mathcal{C}^{0}([a,b])$, $\braket{ f | g }=\int _{a}^{b}f(t)g(t) \, dt$.
	0. Bien forme linéaire ok
	1. Symétrie, ok
	2. Linéaire à gauche ok
	3. Définition et Positivité (intégrale non-nulle d'une fonction positive)
![[Cours Intégration sur un Segment#Nullité]]

4. $\mathbf{E}=\mathbb{R}_{n}[X]$, $\braket{ P | Q }=\sum_{k=0}^{n} P(k)Q(k)$
	1. Symétrique ok
	2. Linéaire à gauche ok
	3. Définition et Positivité (polynôme à $n+1$ racines est nul)

### Le retour de Cauchy-Schwartz

![[Cauchy - Schwartz#En général]]

# Espace Préhilbertien

###### Définition d'un Espace Préhilbertien

Un espace préhilbertien est un $\mathbb{R}-$espace-vectoriel muni d'un produit scalaire

###### Définition d'une norme

La norme est une forme linéaire $\|-\|: \mathbf{E} \to \mathbb{R}_{+}$ vérifiant les propriétés suivantes:
- $\|x+y\|\leq \|x\|+\|y\|$
- $\|\lambda x\|=\lambda \|x\|$
- $\|x\|=0\iff x=0$

Une norme dans un espace préhilbertien est définie comme $\|x\|=\sqrt{ \braket{ x | x } }$.

###### Définition d'une distance

Une distance est une application symétrique $\delta : \mathbf{E}\times \mathbf{E}\to \mathbb{R}_{+}$ vérifiant:
- $\delta(x,y) \geq 0$
- $\delta(x,y) = 0 \iff x=y$
- $\delta(a,c)\leq \delta(a,b)+\delta(b,c)$

La distance dans un espace préhilbertien entre $x$ et $y$ est définie telle que $\delta(x,y)=\|x-y\|$

##### Définition d'un espace Euclidien

Un espace préhilbertien est dit euclidien si sa dimension est finie.

###### Définitions Annexes

1. Un vecteur $x\in \mathbf{E}$ est dit unitaire si et seulement si $\|x\|=1$
2. Deux vecteurs $x,y\in \mathbf{E}$ sont orthogonaux, noté $x\bot y$ si et seulement si $\braket{ x | y }=0$
3. Une famille est dite orthonormée si et seulement si orthogonale et chacun de ses vecteurs est unitaire.

#### Théorème de Pythagore

Soit $(x_{1}\dots x_{n})\in \mathbf{E}^{n}$ une famille de vecteurs orthogonaux, alors
$$
\|\sum_{k=1}^{n} x_{k}\|=\sum_{k=1}^{n} \|x_{k}\|
$$

De plus, si aucun des vecteurs n'est nul, la famille est libre
![[Maths/Preuve - Théorème de Pythagore]]


#### Identités de Polarisation

Soient $x,y\in \mathbf{E}$ espace préhilbertien réel
1. $\frac{1}{4}(\|x+y\|^{2}-\|x-y\|^{2})=\braket{ x | y  }$
2. $\frac{1}{2}(\|x+y\|^{2}-\|x\|^{2}-\|y\|^{2})=\braket{ x | y }$
3. $\|x+y\|^{2}+\|x-y\|^{2}=2\|x\|^{2}+2\|y\|^{2}$

# Sous-Espaces Orthogonaux

### Algorithmes d'orthogonalisation de Gram-Schmidt

Soit $E$ un espace euclidien, il existe une base de $E$ orthogonale et pour tout $i$, $\text{Vect }(e_{1}\dots e_{i})=\text{Vect }(o_{1}\dots o_{i})$.

![[Maths/Preuve - Orthogonalisation]]

#### Corollaire - Orthonormée

Tout espace euclidien admet une base orthonormée.

#### Propriétés de coordonées

Soient $X,Y$ les coordonnées de $x,y$

1. $x_{i}=\braket{ e_{i} | x }$
2. $\braket{ x | y }=X^{T}Y$
3. $\|x\|=\sqrt{ X^{T}X }$

## Sous-Espaces Orthogonaux

###### Sous-Espace Orthogonal

Soit $\mathbf{E}$ préhilbertien réel, et $A$ une partie de $\mathbf{E}$, alors on appelle orthogonale de $A$ noté $A^{\bot}$ l'ensemble des éléments orthogonaux à tous ceux de $A$.

### Sous-Espace

$A^{\bot}$ est un sous-espace vectoriel de $\mathbf{E}$.

![[Maths/Preuve - Sous-Espace Orthogonal]]


##### Inclusion

$$
A\subset B\implies B^{\bot}\subset A^{\bot}
$$

##### Propriétés Evidentes

$F^{\bot}$ supplémentaire à $F$ et $F^{\bot^{\bot}}=F$.

## Equation d'hyperplan

###### Equation d'hyperplan

Un vecteur non-nul est normal à un plan si il est orthogonal à tous les vecteurs de ce plan.

###### Forme Linéaire

$\varphi_{a}(x)=\braket{ a | x }$ est une forme linéaire.

Et $\varphi_{\cdot}$ est une bijection.