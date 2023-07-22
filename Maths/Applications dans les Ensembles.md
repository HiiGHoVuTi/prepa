---
dg-publish: true
---

#maths #ensembles #fonctions #cours

# Définitions
Une application de $E$ dans $F$ est un triplet $(E,F,G)$ où $G$ est une partie de $E \times F$ vérifiant $\forall x \in E, \space \exists! y, (x,y)\in G$.
![[IllustrationApplication.excalidraw]]
Pour $x\in E$, on note $u(x) \in F$ l'unique élément tel que $(x, u(x)) \in F$.

### Terminologie

L'ensemble E est l'ensemble de départ et l'ensemble F est l'ensemble d'arrivée.
Si $(x,y) \in u$ on dit que
- $x$ est l'antécédent de $y$
- y est l'image de $x$

- L'ensemble des fonctions de $E$ vers $F$ est noté $F^E$.

- Le graphe est l'ensemble des points $C_u = \big\{(x,u(x))\space|\space x\in E\big\}$.

- On appelle l'ensemble image de $u$ l'ensemble des images, $u(E) = \big\{u(x), x\in E\big\}$

- On parle de famille indexée par $I$ une application $E^I$ notée $(f_i)_{i\in I}$.

- L'indicatrice de $I\in E$ dans $E$ est une fonction $\mathbb{1}_I$ telle que:
$$
𝟙_I(x) = 
\begin{cases}
1 \text{ si } x\in I \\
0 \text{ sinon}
\end{cases}
$$
# Composition, prolongements et restrictions

- Soit $f\in F^E$, et $A\subset E$, on dit que $A$ est stable par $f$
$$
\forall x \in A, f(x) \in A
$$
- Soient $f\in F^E$ et $g\in G^F$, la composée de $f$ et $g$ est
$$
\begin{align}
g \circ f &\in G^E  \\
(g\circ f)(x) &= g(f(x))
\end{align}
$$
> $\big(-\circ=\big)$ est associative mais pas commutative
- Soient $f∈F^E$ et $A\subset E$, on appelle restriction de $f$ dans $A$
$$
f_{|A} = \big\{(x,y)\in f \text{ | } x\in A\big\}
$$
- Soient $A \subset E$, $f \in F^E$, $g\in F^A$, on dit que $f$ est un prolongement de $g$
$$
\forall x\in A, f(x)=g(x)
$$
- Soient $f \in F^E$ et $B \subset F$, on appelle corestriction de $f$ dans $B$
$$
f^{|B} = \big\{(x,y)\in f \text{ | } y\in B\big\}
$$

# Image direct et image réciproque

Soient $f \in F^E$, $A\subset E$, $B\subset F$.

- L'image directe de $A$ est
$$
f(A) = \big\{f(x) \text{ | }x\in A\big\}
$$
- L'image réciproque de $B$ est
$$
f^{-1}(B) = \big\{x \text{ | } x\in A\land f(x)\in B\big\}
$$

![[Exercice - Restrictions]]

### Propriétés
Soient $f\in F^E$, $A\subset E$, $B\subset F$

- $f^{-1}(f(A)) \supset A$

- $f(f^{-1}(B)) \subset B$

![[Preuve - Image Inclusion]]

# $-$jections

## Définition

Soit $f\in E^F$, on dit que $f$ est:

| **Nom**       | **Propriété**                                     |
| ------------- | ------------------------------------------------- |
| *Injective*   | $\forall x,y\in F, f(x)=f(y) \Longrightarrow x=y$ |
| *Surjective*  | $\forall y\in F, \exists x\in E, f(x)=y$          |
| **Bijective** | *Injective, Surjective*                           |

### Méthode

#### Preuve d'injectivité
![[PreuveInjectivité.excalidraw|200x200]]
Les éléments de $F$ n'ont pas plusieurs antécédents, c'est-à-dire qu'on peut définir un inverse à gauche $g$ avec $g\circ f = \text{id}_{E}$. 

## Propriétés

- Soient $f\in F^E$, $g\in G^F$.  
Si $f$ et $g$ sont $-$jectives toutes les deux, $f\circ g$ est $-$jective aussi.

![[Preuve - Composition Jectivité]]

- Soient $f\in F^E$ et $g\in G^F$
	- $g\circ f$ injective => $f$ l'est aussi
	- $g\circ f$ surjective => $g$ l'est aussi

![[Preuve - Composition Réciproque]]

## Application Réciproque

### Définition

Soit $f$ une bijection de $E$ dans $F$. On définit la réciproque $f^{-1}$ l'application définie de $F$ dans $E$ telle que $f\circ f^{-1} = f^{-1}\circ f = \text{id}$.
$$
\begin{align}
f(x) &= y \\
f^{-1}(y) &= x
\end{align}
$$
> On sait que l'antécédent existe et qu'il est unique par hypothése.

### Propriétés

- Soit $f$ une application bijective de $E$ dans $F$
$$
\begin{align}
f\circ f^{-1} &= \text{Id}_{E} \\
f^{-1}\circ f &= \text{Id}_{F}
\end{align}
$$
> Rappel: $\forall e\in E, \text{ Id}_{E}(e) = e$

![[Preuve - Composition Identité]]

> $f\circ f^{-1} = f^{-1}\circ f \iff E = F$

- Corollaire: $f$ bijective $\implies$ $f^{-1}$ bijective
	Preuve:
	-  $f\circ f^{-1} = \text{Id}$ avec $\text{Id}$ injective donc $f^{-1}$ injective
	- $f^{-1}\circ f = \text{Id}$ avec $\text{Id}$ surjective donc $f^{-1}$ surjective

- Soient $f\in F^E$, $g\in E^F$ avec $g\circ f = \text{Id} = f \circ g$, les deux fonctions sont bijectives et réciproques.
	Preuve: 	
	-  $f\circ g = \text{Id}$ avec $\text{Id}$ injective donc $g$ injective
	- $g\circ f = \text{Id}$ avec $\text{Id}$ surjective donc $g$ surjective
	Donc $g$ est une bijection.
$$
f\circ g \circ g^{-1} = \text{Id}\circ g^{-1} = f\circ\text{Id}
$$

> $g\circ f = \text{Id}$ permet seulement de dire
> 	$f$ est injective
> 	$g$ est surjective

| $-$Jectivité | $g: (\mathbb{R} \to \mathbb{R})$           |
| ------------ | ----------------- |
| *injective*  | $g(x) = e^x$             |
| *surjective* | $g(0) = 861$ sinon $g(x) = \ln \mid x \mid$ |

## Définitions

- Une bijection de $E$ dans $E$ est appelée une *permutation* de $E$.
- Une application de $E$ dans $E$ telle que $f\circ f = \text{Id}$ est appelée une *involution* de E.
> une involution est une bijection, par l'argument de composition.
> Par exemple, les $f(\omega)$ suivantes sont des involutions:
 $-\omega$, $\frac{1}{\omega}$, $\overline{\omega}$ 

### Proposition

Soient $f\in F^E$, $g\in G^F$  des bijections.
Alors $g\circ f$  est une bijection de réciproque $f^{-1}\circ g^{-1}$.

#### Preuve
Bijection ok.
Réciproque par associativité.

### Groupe des Permutations

L'ensemble $\mathfrak{S}(E)$ des permutations de E muni de $\circ$ est un **[[Introduction aux Structures Algébriques#Groupes|groupe]]**.
- $\circ$ est LCI associative
- $\text{Id}_{E}$ est un élément neutre
- pour $f\in \mathfrak{S}(E)$, on a $f^{-1}(x)\in \sigma(E)$
