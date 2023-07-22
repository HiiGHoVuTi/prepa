---
aliases: [Déterminant]
dg-publish: true
order: 22
active: true
---

# Déterminant

## Quelques définitions

##### $p-$Linéarité

$f : E^{p}\to F$ est dite linéaire si elle est linéaire dans chacune de ses composantes

##### Symétrie

$f: E^{p}\to F$ est dite symétrique si $p-$linéaire et pour $\sigma\in \mathfrak{S}(E^{p})$, $f\circ \sigma=f$

##### Antisymétrie

$f: E^{p}\to F$ est antisymétrique (ou alternée) si $f$ est $p-$linéaire et pour une transposition $\tau$, $f\circ \tau = -f$.
Alors $f\circ \sigma = \varepsilon(\sigma)\times f$


## Propriétés

### Familles Liées

Soit $f$ une application $p-$linéaire antisymétrique et $x\in E^{p}$
- Si deux composantes de $x$ sont égales, $f(x)=0$
- Si $x$ est liée, $f(x)=0$

## Déterminant

###### Définition Déterminant

Soient $E$ un $\mathbb{K}-$espace vectoriel, de dimension $n$, $\mathcal{B}$ une base de $E$. Il existe une unique forme $n-$linéaire antisymétrique notée $\text{det}:E^{n}\to \mathbb{K}$ telle que
$$
\text{det}_{\mathcal{B}} \mathcal{B}=1
$$
Alors on a pour $u_{j}=\sum x_{ij}$
$$
\text{det}_{\mathcal{B}} (u_{1}\dots u_{n})=\sum_{\sigma\in S_{n}} \varepsilon(\sigma) \times \prod_{i} x_{\sigma(i),i}
$$

![[Maths/Preuve - Déterminant]]

###### Dans $\mathbb{R}^{2}$

$$
\det\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}= ad-bc
$$

obtenu par linéarité.

###### Dans $\mathbb{R}^{n}, n>3$

Horreurs.

##### Aire 

Le déterminant de deux vecteurs est l'aire algébrique formée par eux.
Idem pour $n$ dimensions avec un $n-$volume.

## Calcul du Déterminant

On se place dans $\mathbb{K}^{n}$ muni de sa base canonique et on considère le déterminant d'une matrice de $\mathcal{M}_{n}(\mathbb{K})$ comme déterminant de ses colonnes.

### Propriétés

##### Déterminants Particuliers

###### Matrices Diagonales

$$
\text{det}D= \prod D_{i,i}
$$

###### Matrices de rang $n-1$

$$
\text{det}M = 0
$$

###### Matrice d'opération élémentaire

$$
\text{det}P_{ij}= -1
$$

$$
\text{det}D_{i\lambda}= \lambda 
$$

$$
\det T_{ij\alpha}= 1
$$

###### Multiple

$$
\text{det} (\alpha M)=\alpha^{n}\text{det}M
$$

#### Sous-Matrice

$$
\text{det} \begin{pmatrix}
\lambda & (\star) \\
(0) & (M)
\end{pmatrix}=\lambda\text{det}M
$$

peu importe la matrice $\star$

![[Maths/Preuve - Det de sous-matrice]]

##### Corollaire - $\det$ de matrice triangulaire

Le déterminant d'une matrice triangulaire est égal à celui de la matrice diagonale correspondante

#### Action d'une matrice élémentaire

$$
\det MP_{ij}=-\det M
$$

$$
\det D_{i\alpha} = \alpha \det M
$$

$$
\det T_{ij\lambda}=\det M
$$

preuve: dessin

##### Corollaire - Inversibilité

$$
M \text{ inversible } \iff \det M\neq 0
$$

![[Maths/Preuve - Inversibilité det]]


##### Corollaire - Morphisme

$$
\det MN= \det M \times \det N
$$

![[Maths/Preuve - Det Multiplication]]

##### Corollaire - Inverse

$$
\det M^{-1}=\frac{1}{\det M}
$$

#### Transposée

$$
\det M^{T}=\det M
$$

![[Maths/Preuve - Determinant Transposée]]

##### Corollaire - Linéarité par rapport aux lignes

Le déterminant est une forme $n-$linéaire antisymétrique par rapport aux colonnes *et* aux lignes.

#### Méthode - Calcul de Det

On peut effectuer des opérations élémentaires sur les lignes jusqu'à arriver à l'identité (ce qui revient à l'inverser), en ajustant le $\det$ au besoin.

## Déterminant d'un endomorphisme

###### Déterminant d'un Isomorphisme

$$
\det f=\det \text{Mat} f
$$

Cette valeur est indépendente de la base.

##### Exemples

###### Déterminant d'une symétrie

$$
\det s = \det \text{Mat}_{\mathcal{B}_{\text{Ker}s-\text{id}}\cup \mathcal{B}_{\text{Ker}s+\text{id}}}s=\det \begin{pmatrix}
1 &  & &  \\
& 1 \\
& & \dots \\
& & & -1
\end{pmatrix}=(-1)^{\text{dim Ker}(s+\text{id})}
$$

##### Critère d'automorphisme

$$
f \in GL(E) \iff \det f\neq 0
$$

# Calcul de Déterminants

## Développement par rapport à une ligne

###### Définition d'un cofacteur

On note $M(ij)$ la matrice extraite en supprimant la $i$ème ligne et la $j$ème colonne.
On appelle cofacteur noté $\Delta_{ij}$ la quantité
$$
\Delta_{ij}=(-1)^{i+j}\det M(i,j)
$$

##### Développement

$$
\det M= \sum_{i} \Delta_{ij} M_{ij} = \sum_{j} \Delta_{ij} M_{ij}
$$

![[Maths/Preuve - Développement en blocs]]


###### Méthode

$$
\begin{pmatrix}
+ & - & + \\
- & + & - \\
+ & - & +
\end{pmatrix}
$$

On retrouve alors
$$
\det M= m_{11}(m_{22}m_{33} - m_{32}m_{23}) - m_{21}(m_{12}m_{33}-m_{32}m_{13})+ m_{31}(m_{12}m_{23}-m_{22}m_{13})
$$
