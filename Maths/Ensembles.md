---
dg-publish: true
---

#maths #cours #ensembles 

# A/ Appartenance, inclusion
## 1) Définition
Un ensemble est une "collection d'objets".
- **Appartenance**
$$x\in A \iff x \text{ est un élément de la collection } A$$
la négation est notée x∉A
- **Inclusion**
$$A \subset E \iff \forall (x \in A) .x\in E$$
on dit que A est une partie de E
- **Egalité**
$$A = B \iff (A \subset B) \land (B \subset A)$$
- On note $\emptyset$ l'ensemble vide
$$\nexists x\in \emptyset$$
- On note $P(A)$ l'ensemble des parties de $A$
$$P(A) = \big\{X\space | \space X \subset A\big\}$$
### *Ex:*
$P(\{1,2\}) = \{\emptyset, \{1\},\{2\}, \{1,2\} \}$
$P(P(\emptyset)) = \{\emptyset, \{\emptyset\}\}$

> On peut définir $\mathbb{N}$ tel que:
$$
\begin{align}
0 &= \emptyset \\
n+1 &= P(n) \\
a < b &\iff a \in b 
\end{align}
$$


## 2/ Opérations sur les ensembles
### a) Usuelles
- Soient $A,B \in E$, on définit:
$$
\begin{align}
A \cup B &= \{x \space|\space (x \in A) \lor (x\in B) \} \\
A \cap B &= \{x \space|\space (x \in A) \land (x\in B) \} \\
A \backslash B &= \{x \space|\space (x \in A) \land (x \notin B)\} \\
C^A_E &= E \backslash A
\end{align}
$$
### b) Opératoires
Soient $A,B,C \in E$, on a alors:

- $A \cup A = A \cap A = A$
- $\cup$ et $\cap$ sont commutatives
- $\cup$ et $\cap$ sont associatives

- $A \cap (B \cup C) = A \cup B \bigcup A \cap C$ 
![[IllustrationEnsemblesDistributivité.excalidraw|200x200]]

> **Preuve**
On passe par les propositions logique définissant les ensembles.

### c) Produit Cartésien
On note:
- $A \times B = \big\{(a,b)\space|\space a \in A,\space b \in B \big\}$
- $A^n$ avec $n\in\mathbb{N}$ la $n$-ième iteration de ce produit
- $\prod A_k = A_0 \times A_1 \times \dots \times A_n$

>On abuse souvent de la notation et on aurait:
$(a,(b,c)) = (a,b,c)$
 $(a,b,c) \in \mathbb{N}^3$

# Relations
Soit $\Gamma \subset A^2$, on associe une relation $\mathbf{R}_\Gamma$ à $A$ telle que
$$a \mathbf{R}_\Gamma b \iff (a,b)\in\Gamma$$
>on dit que $a$ est en relation avec $b$

On dit d'une relation qu'elle est:

| **Nom**           | **Propriété**                                           |
| ----------------- | ------------------------------------------------------- |
| *réflexive*       | $\forall x\in A, \space x\mathbf{R}x$                   |
| *symétrique*      | $x\mathbf{R}y \iff y\mathbf{R}x$                        |
| *antisymétrique*  | $x\mathbf{R}y \land y\mathbf{R}x \Rightarrow x=y$       |
| *totale*          | $\forall x,y\in A,\space x\mathbf{R}y\lor y\mathbf{R}x$ |
| **d'ordre**       | *réflexive*, *antisymétrique*, *transitive*             |
| **d'équivalence** | *réflexive*, *symétrique*, *transitive*                 |

### Définition d'une classe d'équivalence
Pour $A$ muni d'une relation $R$, on nomme classe d'équivalence de $x \in A$ l'ensemble suivant:
$$
Cl_R(x) = \big\{a\space|\space aRx \big\}
$$
>**Ex**:
 $2\mathbb{N} = Cl_{\text{mod 2}}(0)$ sur $\mathbb{N}$

Les classes d'équivalence forment une partition de l'ensemble sur lequel elles sont définies.

> **Exercice**
[[Cherche la faute - Relations]]
