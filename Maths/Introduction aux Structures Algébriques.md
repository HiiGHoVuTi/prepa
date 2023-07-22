---
dg-publish: true
order: 4
---
#maths/cours

# Loi de composition interne

> on abrégera par LCI

## Définition

Soit $\mathbf{E}$ un ensemble, une loi de composition interne est une application 
$$
(\cdot) : \mathbf{E}^{2} \to \mathbf{E}
$$

> exemples: $+$ dans $\mathcal{M}_{n,p}(\mathbb{K})$, $\land$ dans les booléens, $\cap$ dans $\mathcal{P}(E)$


## Propriétés

Soit $\mathbf{E}$ muni de $(\cdot)$ et $(*)$

### Associativité

$$
\forall x,y,z \in \mathbf{E},\quad (x \cdot y) \cdot z = x \cdot (y \cdot z)
$$

> $(\circ)$ est associative et $(-)$ ne l'est pas

### Commutativité

$$
\forall x,y \in \mathbf{E}, \quad x \cdot y = y \cdot x
$$

### Unité

$$
\exists e \in \mathbf{E}, \forall x\in \mathbf{E}, \quad e \cdot x = x \cdot e = x
$$

### Symétrie

> il faut une unité pour que la LCI puisse être symétrique

$$
\forall x \in \mathbf{E}, \exists y \in \mathbf{E}, \quad x \cdot y = y \cdot x = e
$$
### Distributivité


On dit que $(*)$ est distributif à gauche (resp. à droite) sur $(\cdot)$

$$
\forall x,y,z \in \mathbf{E}, \quad x * (y \cdot z) = (x * y) \cdot (x * z)
$$

> ex: $(f+g) \circ h = f \circ h + g \circ h$

### Stabilité

Soit $\mathcal{A} \subset \mathbf{E}$, $\mathcal{A}$A est stable par $(\cdot)$ ssi

$$
\forall x,y \in \mathcal{A}, x \cdot y \in \mathcal{A}
$$
donc $(\cdot)$ est une LCI dans $\mathcal{A}$

# Groupes

## Définition

Soit $G$ un ensemble et $(\cdot)$ une LCI sur $G$, on dit que $(G, \cdot)$ est un groupe ssi:

1. associative
2. unifère
3. symétrique

> ex: $(\mathbb{R}, +)$ est un groupe, $(\mathbb{C}^{*}, \times)$ aussi, $(\mathfrak{S}(E), \circ)$

## Groupe Abélien

$(\mathbf{E}, \cdot)$ est dit abélien ssi ![[Introduction aux Structures Algébriques#Commutativité]]
## Sous-Groupe

### Définition

Soit $H \in G$, on dit que $H$ est un sous-groupe de $(G, \cdot)$ si $(H, \cdot)$ est un groupe.

### Caractérisations

1. 
	-  $e \in H$
	-  stable par l'inverse
	-  stable par $(\cdot)$

2. 
$e \in H$ ou $x$ non-vide et
$$
\forall x,y \in G, \quad x \cdot y^{-1} \in H
$$


![[Preuve - Caractérisation Sous-Groupe]]

> $(\mathbb{R},+)$ est un sous-groupe de $(\mathbb{C}, +)$, $(\mathbb{U}_{n},\times)$ est un sous groupe de $(\mathbb{U}, \times)$

[[Introduction aux Structures Algébriques Ex SG.excalidraw|Exercice]]

### Intersection

L'intersection de deux sous-groupes est un sous-groupe également.

![[Maths/Preuve - Intersection sous-groupes]]


## Morphismes de groupes 

C'est un morphisme dans la [[Catégories|catégorie]] des groupes.

Soient $(G, \cdot)$ et $(H, *)$ des groupes. Une application $f: G \to H$ telle que
$$
f(x \cdot y) = f(x) * f(y)
$$

> ex:
> $e^{-} : (\mathbb{R},+) \to(\mathbb{R}^{*}_{+}, \times)$
> $\ln(-): (\mathbb{R}^{*}_{+}, \times) \to (\mathbb{R}, +)$

[[Introduction aux Structures Algébriques Ex1 Morphismes.excalidraw|Exercices]]

| Nom               | Propriété                                   |
| ----------------- | ------------------------------------------- |
| *iso*morphisme    | $(G, \cdot) \longleftrightarrow (H, *)$     |
| *endo*morphisme   | $(G, \cdot) \longrightarrow (G, \cdot)$                 |
| **auto**morphisme | $(G, \cdot) \longleftrightarrow (G, \cdot)$ |

### Propriétés 

Pour $f$ morphisme de groupes, on a:
$$
\begin{align}
f(e_{G}) &= e_{H} \\
f(x^{-1}) &= (f(x))^{-1}
\end{align}
$$
Si $(H, \cdot)$ est un sous-groupe de $(G, \cdot)$ alors $(f(H), \cdot)$ et $(f^{-1}(H), \cdot)$ aussi

[[Preuve - Propriétés Morphismes|Preuve]]

### Corollaire

Soit $f : (G, \cdot) \to(H, *)$,

1. $(f(G), *)$ est un sous-groupe de $(H, *)$
2. $(f^{-1} (\{ e_{G} \}), *)$ est un sous-groupe de $(H, *)$

> On note $\text{Ker}(f)=f^{-1}(\{ e_{G} \})$ et $\text{Im}(f) = f(G)$

[[Introduction aux Structures Algébriques Exemples.excalidraw|Exemple]]

## $-$jectivité

Soit $f : (G, \cdot) \to (H, *)$

1. $f$ surjective $\iff$ $f(G)=G$
2. $f$ injective $\iff$ $\text{Ker}(f) = \{ e_{G} \}$

![[Maths/Preuve - Ker Injectivité]]

# Anneaux et Corps

## Anneau - Définition 

Soit $A$ un ensemble muni de deux lois $+$ et $\cdot$, $(A,+,\cdot)$ est un anneau ssi

1. $(A, +)$ est un groupe abélien (neutre $0$)
2. $(A,\cdot)$ est un magma associatif unifère (neutre $1$)
3. $\cdot$ est distributive sur $+$

On dit que l'anneau est abélien si $(A^{*}, \cdot)$ est un groupe abélien 

> ex: 
> $(\mathbb{Z}, +, \times)$ est un anneau commutatif de neutres $0,1$
> $(\text{Ob}(\mathcal{C}), +, \times)$ est un anneau de neutres l'objet terminal et initial
> $(\mathcal{M}_{n,n}, +, \times)$ est un anneau de neutres $0, I_{n}$

## Sous-Anneaux - Définition 

Soient $(A, +, \times)$ un anneau et $B \subset A$ non-vide, on dit que $(B, +, \times)$ est un sous-anneau de $(A, +, \times)$ ssi

1. $B$ est stable par $+,\times$
2. $(B, +, \times)$ est un anneau 

### Caractérisation 

Soit $(A, +, \times)$ un anneau, $B$ une partie de $A$, ces propositions sons équivalentes

1. $(B, +, \times)$ sous-anneau de $(A, +, \times)$
2. $(B, +)$ sous-groupe de $(A, +)$ $\huge \land$ $1 \in B$ $\huge \land$ $B$ stable par $\times$


> ex: 
> $(\mathbb{Q}, +, \times)$ sous-anneau de $(\mathbb{R}, +, \times)$
> $(\{ a+b\sqrt{ 861 } \;;\; a,b \in \mathbb{Z} \}, +, \times)$ sous-anneau de $(\mathbb{R}, +, \times)$

### Intégrité 

Un anneau $(A, +, \times)$ est un anneau tel que si $xy = 0$, alors $x=0\, \lor\, y=0$.

> $\mathcal{M}_{n}(\mathbb{K}), +, \times$ n'est pas intègre avec $n\geq 2$

## Propriétés Anneau 

### Sommes et Puissances

Soient $a, b \in A$ tels que $ab=ba$, $n \in \mathbb{N}$ et $(A, +, \times)$ un anneau

1. 
$$
(a+b)^{n} = \sum^{n}_{k=0} {n \choose k} a^{k} b^{n-k}
$$
2. 
$$
a^{n} - b^{n} = (a-b) \sum^{n}_{k=0} a^{k}b^{n-k}
$$
3. 
$$
a^{2n+1}+b^{2n+1} = (a+b) \sum^{2n}_{k=0} a^{k}b^{2n-k}(-1)^{k}
$$
### Groupe des inversibles 

Soit $(A, +, \times)$ un anneau, l'ensemble $A^{*}$ des éléments inversibles pour $\times$ forment un groupe $(A^{*},\times)$

![[Maths/Preuve - Groupe des inversibles]]

[[Introduction aux Structures Algébriques Exercice Sous-Anneau.excalidraw|Exercice]]

## Morphisme d'Anneaux

Soient $(A_{1},+_{1}, \times_{1})$ et $(A_{2}, +_{2}, \times_{2})$ deux anneaux et $f: A_{1} \to A_{2}$, on dit que $f$ est un morphisme d'anneaux ssi:

1. $\forall z_{1},z_{2} \in A_{1},\; f(z_{1} +_{1} z_{2}) = f(z_{1}) +_{2} f(z_{2})$
2. $\forall z_{1}, z_{2}, \; f(z_{1} \times_{1} z_{2}) = f(z_{1}) \times_{2} f(z_{2})$
3. $f(1) = 1$

[[Introduction aux Structures Algébriques Exercice Morphisme Anneaux.excalidraw|Exercice]]

## Corps - Définition 

Soit $(A, +, \times)$ un anneau, $(A,+, \times)$ est un corps si $A^{*}=A \setminus \{ 0 \}$

> ex: $(\mathbb{Z}, +, \times)$ est un anneau mais pas un corps, $(\mathcal{M}_{n\geq 2}, +, \times)$ de même

## Sous-Corps

Soient $(\mathbb{K}, +, \times)$ un corps, $B$ une partie de $\mathbb{K}$, on dit que $(B, +, \times)$ est un sous-corps de $(\mathbb{K}, +, \times)$ ssi:

1. $B$ est stable par $\times$ et $(B, +, \times)$ est un anneau 

### Caractérisation 

1. $(B, +, \times)$ est un sous-anneau de $(\mathbb{K}, +, \times)$
2. tout élément non-nul est inversible

### Intégrité

Un corps est un anneau intègre.

![[Maths/Preuve - Intégrité Corps]]
