---
aliases: [Matrices et applications linéaires]
dg-publish: true
order: 15
active: true
---

#maths/cours 

Les EV de ce chapitre sont de dimension finie.

# Matrice d'une application linéaire

Soit $F$ un $\mathbb{K}-$espace vectoriel. On prend $\mathcal{B}$ une base. Pour $x\in F$, on note $\text{Mat}_{\mathcal{B}}x$ ses coordonnées dans $\mathcal{B}$.

$$
\text{Mat} x=\begin{pmatrix}
x_{1} \\
\vdots \\
x_{n}
\end{pmatrix}
$$

> Si $F=\mathbb{K}^{n}$ avec $\mathcal{B}$ canonique alors $\text{Mat }_{}x=x$.

On étend la définiton à toute famille $\mathfrak{F}$ de $F$.
$$
\text{Mat} (f_{1}\dots f_{n})= \begin{pmatrix}
\begin{pmatrix}
 \\\text{Mat}f_{1} \\ \\
\end{pmatrix} \dots \begin{pmatrix}
\\ \text{Mat}f_{n} \\ \\
\end{pmatrix}\\
\end{pmatrix}

$$

Soient $E,F$ deux espaces avec pour bases $\mathcal{B}_{E}=(e_{1}\dots e_{n})$ et $\mathcal{B}_{F}=(f_{1}\dots f_{n})$ et $\mathfrak{u}\in L(E,F)$. On appelle matrice de $f$ dans les bases $\mathcal{B}_{E},\mathcal{B}_{F}$ la matrice suivante
$$
\text{Mat}_{\mathcal{B}_{E},\mathcal{B}_{F}} \mathfrak{u}=\begin{pmatrix}
\begin{pmatrix}
\\ \text{Mat}_{\mathcal{B}_{F}} f(e_{1}) \\ \\
\end{pmatrix}\dots \begin{pmatrix}
\\ \text{Mat}_{\mathcal{B}_{F}} f(e_{n}) \\ \\
\end{pmatrix}
\end{pmatrix}
$$

# Liens opératoires

## Multiplication de matrice

Soient $E,F$ deux espaces avec pour bases $\mathcal{B}_{E}=(e_{1}\dots e_{n})$ et $\mathcal{B}_{F}=(f_{1}\dots f_{n})$ et $\mathfrak{m}\in L(E,F)$.

$$
\text{Mat}_{\mathcal{B}_{F}} \mathfrak{m}(x)=\text{Mat}_{\mathcal{B}_{E},\mathcal{B}_{F}}\mathfrak{m}\times \text{Mat}_{\mathcal{B}_{E}} x
$$

![[Maths/Preuve - AL Matmul]]

> Calculer le noyau de $\mathfrak{m}$ revient à résoudre $MX=0$. 

## Isomorphisme

$$
\varphi(f)=\text{Mat}_{\mathcal{B}_{E},\mathcal{B}_{F}} f
$$

est un isomorphisme de $L(E,F)$ dans $\mathcal{M_{n,p}}(\mathbb{K})$

![[Maths/Preuve - Isomorphisme mat]]

### Corollaire, dimension des applications linéaires

$$
\text{dim}L(E,F)=\text{dim}E \times \text{dim}F
$$

## Composition

Soient $E,F,G$ trois $\mathbb{K}-$evdf, $\mathfrak{u}\in L(E,F),\mathfrak{v}\in L(F,G)$

$$
\text{Mat }\mathfrak{v\circ  u}=\text{Mat } \mathfrak{v} \times \text{Mat } \mathfrak{u}
$$

>[!warning] Attention aux bases

![[Maths/Preuve - Composition matrices]]

# Matrices Inversible

## Caractérisation d'un isomorphisme

Soit $\mathfrak{u}\in L(E,F)$, alors $\mathfrak{u}$ est bijective si et seulement si $\text{Mat }\mathfrak{u}$ est inversible et on a
$$
\text{Mat } \mathfrak{u^{-1}}= (\text{Mat }\mathfrak{u})^{-1}
$$

![[Preuve - Inversibilité AL]]

## Matrice de Passage

On appelle matrice de changement de base de $\mathfrak{B}$ à $\mathcal{B}$ la matrice de l'identité entre ces bases.
$$
P=\text{Mat}_{\mathcal{B},\mathfrak{B}} \text{Id}
$$

### Changement de base

Soient $\mathcal{E},\mathfrak{E}$ deux bases de $E$ et $\mathcal{F},\mathfrak{F}$ deux base de $F$, et $\mathfrak{u}\in L(E,F)$
$$
\text{Mat}_{\mathcal{B},\mathcal{F}} \mathfrak{u} = \text{Mat}_{\mathfrak{F},\mathcal{F}} I \times \text{Mat}_{\mathfrak{B},\mathfrak{F}}\mathfrak{u} \times \text{Mat}_{\mathcal{B},\mathfrak{B}} I
$$

>[!note] Cas particulier, les Endomorphismes
>On s'arrange pour avoir la même base de départ et d'arrivée

# Rang d'une Matrice

Soient $M\in \mathcal{M}_{n,p}(\mathbb{K})$ et $\varphi _M$ l'application linéaire canoniquement associée à $M$.

- $\text{Ker}M=\text{Ker}\varphi_{M}$
- $\text{Im}M=\text{Im}\varphi_{M}$
- $\text{rg}M=\text{dim}\text{Vect}M=\text{rg}\varphi_{M}$

## Propriétés

$$
\text{rg}f=\text{rg Mat}f
$$

![[Maths/Preuve - Rang matrice AL]]

## Rang

Soient $A\in \mathcal{M_{n,p}}(\mathbb{K}),B\in \mathcal{M}_{p,q}(\mathbb{K})$

- $\text{rg}(AB)\leq \text{min} \{ \text{rg}A,\text{rg}B \}$
- $\text{rg}A=p\implies \text{rg}AB=\text{rg}B$
- $\text{rg}B=p\implies \text{rg}AB=\text{rg}A$

![[Preuve - Rang produit]]

### Corollaire

Soient $P,Q\in \text{GL}(\mathbb{K})$,
$$
\text{rg}PMQ=\text{rg}M
$$

## Matrices équivalentes

Soient $A,B\in \mathcal{M}_{n,p}(\mathbb{K})$ on dit que $A$ et $B$ sont équivalentes elles ont le même rang.

### Bloc Identité 

Soit $A\in \mathcal{M}_{n,p}(\mathbb{K})$, il existe $P\in \text{GL}_{n}(\mathbb{K}),Q\in \text{GL}_{p}(\mathbb{K})$ tels que
$$
PAQ= \begin{pmatrix}
\begin{pmatrix}
1 & 0&\dots &0 \\
0& 1 &\dots &0 \\
\vdots & \ddots &\ddots &\vdots \\
0 & \dots & \dots & 1
\end{pmatrix} & (0) \\
(0) &(0)
\end{pmatrix}=\begin{pmatrix}
\begin{pmatrix}
\\&I_{r}& \\ \\
\end{pmatrix}&(0) \\
(0)&(0)
\end{pmatrix}
$$

avec $r=\text{rg}A$

![[Maths/Preuve - Bloc Identité]]

#### Corollaire, Transposée

- $\text{rg}A=\text{rg}A^{T}$
![[Maths/Preuve - Rang transposée]]

## Matrice Extraite

On appelle matrice extraite de $M$ les sous-matrices $N$ telles que
$$
n_{ij}=m_{\varphi(i),\psi(j)}
$$
avec $\varphi$ et $\psi$ strictement croissantes

### Inversibilité

Soit $M$ de rang $r$, toutes les sous-matrices d'ordre strictement plus grandes que $r$ sont non-inversibles et il existe une sous-matrice d'ordre $r$ inversible.

![[Preuve - Inversibilité extraites]]

# Matrices semblables

## Matrices semblables

$A$ et $B$ sont semblables si et seulement si

$$
A=PBP^{-1}
$$

## Caractérisation

$A$ et $B$ sont semblables si et seulement si $A$ et $B$ sont la matrice de la même application linéaire dans des bases différentes.

![[Maths/Preuve - matrices semblables]]

## Trace

### Commutativité

$$
\text{Tr}(AB)=\text{Tr}(BA)
$$

### Indépendance

Pour tout base, $\text{Tr Mat}_{\mathcal{B}}f$ est la même quantité notée $\text{Tr}f$.

![[Maths/Preuve - Trace f]]

>[!tip] Pour matrices semblables
>Si deux matrices ont des traces différentes, elles ne sont pas semblables.
>La réciproque est fausse, $\begin{pmatrix}0&0\\0&0\end{pmatrix}$ et $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ on des rangs différents.

### Proposition

Soit $p$ projecteur,
$$
\text{rg}f=\text{Tr}f
$$

![[Maths/Preuve - Trace proj]]
