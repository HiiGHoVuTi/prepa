---
aliases: [Groupe Symétrique]
dg-publish: true
order: 21
active: true
---

#maths/cours 

# Le Groupe Symétrique

## Groupe des permutations

Soit $E$ un ensemble, on appelle permutation de $E$ une application bijective $\sigma: E \to E$. On note $\mathfrak{S(}E\mathfrak{)}$ l'ensemble des permutations de $E$, c'est un groupe par la composition.

### Permutation de Groupes

On peut étudier $\mathfrak{S}(G)$ et l'application
$$
\begin{align}
\varphi :&\; G \longrightarrow \mathfrak{S}(G) \\
\varphi=&\; a \mapsto x \mapsto ax
\end{align}
$$

![[Maths/Preuve - Permutation de groupe]]

Donc tout groupe $G$ est isomorphe à une partie de $\mathfrak{S}(G)$.

## Groupe Symétrique

Lorsque $E=\textlbrackdbl 1,n \textrbrackdbl$, on dit que $\mathfrak{S}(E)$ est le groupe symétrique noté $S_{n}$ ou $\mathfrak{S}(n)$.
Alors on peut noter pour $\sigma\in S_{n}$,
$$
\sigma=\begin{pmatrix}
1& \dots& n \\
\sigma(1) & \dots & \sigma(n)
\end{pmatrix}
$$

### Quelques exemples

$$
\begin{align}
S_{2}&=\left\{ \begin{pmatrix}
1&2 \\
1&2
\end{pmatrix},\; \begin{pmatrix}
1&2 \\
2&1
\end{pmatrix} \right\} \\
S_{3} &= \left\{ \begin{pmatrix}
1&2&3 \\
1&2&3
\end{pmatrix}, \begin{pmatrix}
1&2&3 \\
2&1&3
\end{pmatrix}, \\
\begin{pmatrix}
1&2&3 \\
1&3&2
\end{pmatrix}, \\
\begin{pmatrix}
1&2&3 \\
3&2&1
\end{pmatrix}, \\
\begin{pmatrix}
1&2&3 \\
2&3&1
\end{pmatrix} \\
\begin{pmatrix}
1&2&3 \\
3&1&2
\end{pmatrix} \right\}
\end{align}
$$

Pas de commutativité en général.

### Support d'une permutation

On appelle support de $\sigma$ l'ensemble des éléments de $\textlbrackdbl 1,n \textrbrackdbl$ non invariants par $\sigma$.
$$
\text{support }\sigma = \{ x\in E\;;\; x \neq \sigma(x) \}
$$

### Ordre d'une permutation

Soit $\sigma\in S_{n}$, l'ordre de $\sigma$ est le plus petit entier $p\in \mathbb{N}^{\star}$ tel que $\sigma^{p}=\text{id}$.

![[Maths/Preuve - Existance Ordre]]

### Sous-groupe engendré

Soit $\sigma\in S_{n}$, le sous-groupe engendré par une permutation est un sous-groupe de $S_{n}$
$$
\braket{\sigma} = \{ \sigma^{k}\;;\; k\in \mathbb{Z} \} \text{ sous-groupe de } S_{n} 
$$

# Cycles et transpositions

## Orbite

On appelle *orbite* de $a\in \textlbrackdbl 1,n \textrbrackdbl$ par $\sigma\in S_{n}$ notée $\mathcal{O}_{\sigma}(a)=\{ \sigma^{k}(a)\;;\; k\in \mathbb{N} \}$.

## Permutation circulaire

Si $\sigma\in S_{n}$ admet une seule orbite, alors on l'appelle *permutation circulaire*.
Il y en a $(n-1)!$ différentes.

## Cycle

Si $\sigma\in S_{n}$ admet une seule orbite de cardinal différent de $1$ alors on l'appelle *cycle*.
Une permutation circulaire est un cycle.

On pourra noter $\sigma=\begin{pmatrix} x_{1}&x_{2}&\dots&x_{p}\end{pmatrix}$ avec $\sigma(x_{i})=x_{i+1\text{ mod }p}$

### Décomposition en Cycles

#### Lemme
Deux cycles à supports disjoints commutent.

#### Décomposition

Toute permutation $\sigma\in S_{n}$ se décompose de manière unique (à l'ordre près) comme une composée de cycles à supports disjoints.

![[Maths/Preuve - Décomposition en cycles]]

#### Corollaire - Méthode

Si on a la cette décomposition, on obtient facilement l'ordre de $\sigma$ (PPCM de l'ordre des cycles, on le montre par double divisibilité).
Aussi, si $\sigma=\bigcirc c_{i}$ alors $\sigma^{k}=\bigcirc c^{k}_{i}$.

## Transposition

Une transposition est un cycle de longueur $2$.

### Décomposition

Tout cycle de $S_{n}$ se décompose en produit de transpositions.

![[Maths/Preuve - Décomposition en transpositions]]

#### Corollaire

Toute permutation de $S_{n}$ se décompose en produit de transpositions.

# Signature d'une permutation

###### Inversion

Le couple $(i,j)$ est une inversion de $\sigma$
$$
i<j\quad\text{ et }\quad\sigma(i)> \sigma(j)
$$

##### Signature

On note $I(\sigma)$ le nombre d'inversion de $\sigma$ et définit la signature de $\sigma$ notée $\varepsilon(\sigma)$ la quantité
$$
\varepsilon(\sigma)=(-1)^{I(\sigma)}
$$
Elle est aussi donnée par
$$
\varepsilon(\sigma)= \prod_{1\leq i<j\leq n} \frac{\sigma(j)-\sigma(i)}{j-i}
$$

###### Parité
Une permutation est $\begin{cases}\text{paire}& \text{si } \varepsilon(\sigma)=\;\;\,1 \\ \text{impaire} & \text{si } \varepsilon(\sigma)=-1 \end{cases}$


### Parité de Transposition

$$
\varepsilon((a\;b)) = -1
$$

![[Maths/Preuve - Parité de transposition]]

### Théorème fondamental

$$
\varepsilon(\sigma_{1} \circ \sigma_{2})=\varepsilon(\sigma_{1})\times \varepsilon(\sigma_{2})
$$

Donc $\varepsilon$ est un morphisme de $S_{n}$ dans $(\{ -1,1 \},\times)$. 

Preuve: utiliser la 2è forme de la signature, et argument combinatoire.
(pas au programme !)

#### Sous-Groupes de parité

Les permutations paires forment un sous-groupe de $S_{n}$ (pas les impaires).

#### Nombre de transpositions

La signature de $\sigma$ est $(-1)^{p}$ avec $p$ le nombre de transpositions dans la décomposition de $\sigma$.

#### Signature de cycle

Si $m$ est la longueur du cycle, sa signature est $(-1)^{m-1}$.

##### Méthodes de calcul de signature

- Force brute: tableau à double entrée des inversions
- Décomposition en cycles: $\varepsilon(\sigma)=\prod_{k}(-1)^{m_{k}-1}$

