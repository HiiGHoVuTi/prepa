---
dg-publish: true
order: 12
---

#maths/cours 

Dans ce chapitre, le corps $\mathbb{K}$ considéré sera souvent $\mathbb{R}$ ou $\mathbb{C}$.

# Espace Vectoriel

## Définition

$(E,+,\cdot)$ est un $\mathbb{K}-$espace vectoriel si
$$
\begin{align}
(+) : E^{2} \to E \\
( \cdot) : 𝕂× E → E \\

\end{align}
$$
avec $(E,+)$ est un groupe abélien et
$$
\begin{align}
\lambda \cdot (\mu x) &= (\lambda \mu) \cdot x \\
(\lambda+\mu)\cdot x &= \lambda x+\mu x \\
\lambda \cdot (x+y)&= \lambda \cdot x+\lambda \cdot y \\
1 \cdot x &= x
\end{align}
$$
Le corps $\mathbb{K}$ est appelé corps des scalaires et $0_{E}$ est le vecteur nul.

>[!example] Exemples de référence
>$\mathbb{K}$ est un $\mathbb{K}-$espace vectoriel
>$\{ 1 \}$ est un $\mathbb{K}-$espace-vectoriel
>$\mathbb{R}^{n}$ est un $\mathbb{R}-$espace-vectoriel
>$\mathcal{M}_{n,p}(\mathbb{K})$ l'ensemble des matrices de taille $n,p$
>$\mathbb{C}$ est un $\mathbb{L}\subset \mathbb{C}-$espace vectoriel
>$I^{\mathbb{K}}$ est un $\mathbb{K}-$espace vectoriel

## Propriétés

### Combinaison linéaire

On appelle combinaison linéaire de $x_{1},\dots ,x_{n}$ un objet de la forme
$$
\sum_{i} x_{i}\lambda_{i}
$$
avec $\lambda_{i}\in \mathbb{K}$

### Produit Cartésien

Si $E$ et $F$ sont des espaces vectoriels, alors $E\times F$ est un espace vectoriel, on effectue les opérations en parallèle et distribue la multiplication
$$
\begin{align}
(x,y)+(a,b) &= (x+a,y+b)  \\
\lambda(a,b) &= (\lambda a,\lambda b)
\end{align}
$$

# Sous-Espace Vectoriel

## Définition

Soient $(E,+,\cdot)$ un $\mathbb{K}-$espace vectoriel et $F$ est une partie de $E$, $F$ est un sous-espace vectoriel de $E$ si $(F, +, \cdot)$ est un $\mathbb{K}-$espace vectoriel.

## Caractérisation Principale

$F$ est un sous-espace vectoriel de $E$ si, et seulement si $F$ est non-vide et stable par combinaison linéaire.

![[Maths/Caractérisation Espace Vectoriel]]

## Intersections, Sommes et Engendrés

### Intersection

Soient $E$ un espace vectoriel et $(F_{i})$ une famille de sous-espaces vectoriels de $E$, alors
$$
{\huge\cap}_{i} F_{i}
$$
est un sous-espace vectoriel de $E$.

![[Maths/Preuve - Intersection EV]]

>[!warning] L'union ne convient pas

### Engendré

Soient $E$ un $\mathbb{K}-$espace vectoriel et $A$ une partie non-vide de $E$, on appelle $\text{Vect}A$ ou $<A>$ l'ensemble suivant
$$
\text{Vect}A = \{  a+\lambda b \;;\ a,b\in A,\lambda\in \mathbb{K} \}
$$

> L'engendré d'une partie non-vide est un sous-espace vectoriel

### Somme

Soient $E$ un $\mathbb{K}-$espace-vectoriel, $F$ et $G$ deux sous-espaces vectoriels, on note $F+G$ le sous-espace vectoriel "somme"
$$
F+G = \{ x_{1}+x_{2}\;;\; x_{1} \in F,x_{2} \in G \}
$$

>[!note] $F+G = \text{Vect} (F\cup G)$

### Somme Directe

Une somme est directe si et seulement si la forme $x_{1}+x_{2}$ d'un élément est unique, on note cette somme $F \oplus G$

Il y a équivalence entre
- $F,G$ sont en somme directe
- $F\cap G = \{ 0 \}$

![[Maths/Preuve - Somme Directe]]

### Sous-Espaces Supplémentaires

De même, on a $F,G\subset E$ tels que $E=F\oplus G$, on appelle $F$ et $G$ sous-espaces supplémentaires

Il y a équivalence entre
- $F$ et $G$ sont supplémentaires ($F \oplus G = E$)
- $F\cap G= \{ 0 \}$ et $F+G=E$

### Théorème

Soient $E$ un $\mathbb{K}-$espace-vectoriel, $F\subset E$ sous-espace vectoriel, alors il existe (au moins) un $G$ tel que $F\oplus G=E$.

> dépend de l'axiome du choix dans le cas général

# Applications linéaires

## Définition

Soient $E,F$ deux $\mathbb{K}-$espaces vectoriels, $f\in F^{E}$. On dit que $f$ est une application $\mathbb{K}-$linéaire si et seulement si
$$
f(\mu x+\lambda y)= \mu f(x)+\lambda f(y)
$$

> Pour la définition, il suffit de montrer le cas où $\mu=1$

On note $L(E,F)\subset F^{E}$ l'ensemble des applications linéaires de $E$ dans $F$.
On abrège $L(E,E)$ en $L(E)$

On appelle noyau de $f$ noté $\text{Ker}f$ l'ensemble $f^{-1}(\{ 0 \})$.
On note $\text{Im}f$ l'image directe $f(E)$

> Si $f$ est linéaire, alors $f$ est un morphisme de $(E,+)$ dans $(F,+)$

Si $F=\mathbb{K}$, alors $f$ est appelée *forme linéaire* sur le $\mathbb{K}-$espace vectoriel.

Exemples:
- La dérivation est linéaire de l'ensemble des fonctions dérivables sur $I$ dans l'ensemble des fonctions définies sur $I$
- L'application $\varphi:\mathcal{C}([0,1],\mathbb{R})\to \mathbb{R}$, $\varphi(f)=\int_{0}^{1} f(t) \, dt$ est une forme linéaire sur $\mathbb{R}$
- L'application $f(x,y,z)=(x+y,x+y+z)$ est linéaire

## Propriétés

### Sous-espaces et applications linéaires

Soient $E,F$ deux $\mathbb{K}-$espaces vectoriels, $E_{1},F_{1}$ des sous-espaces et $f\in L(E,F)$.
Alors $f(E_{1})$ est un sous-espace de $E$ et $f^{-1}(F)$ est un sous-espace de $E$.

![[Maths/Preuve - SEV et AL]]

#### Corollaire

- $\text{Ker}f$ sev de $E$
- $\text{Im}f$ sev de $F$

### Injectivité

- $f$ injective $\iff$ $\text{Ker}f=\{ 0 \}$
- $f$ surjective $\iff$ $\text{Im}f=F$

### Opérations 

Soient $E,F,G$ trois $\mathbb{K}-$espaces vectoriels, on a
- $\forall f,g \in L(E,F), \forall \lambda \in \mathbb{K}, f+ \lambda g \in L(E,F)$
- $\forall f\in L(E,F), \forall u\in L(F,G), u\circ f \in L(E,G)$
- $\forall f \in L(E,F), \forall u,v \in L(E,G), (u+v)\circ f \in L(E,G)$
- $\forall f,g \in L(E,F), \forall u \in L(E,G), u \circ (f+g) \in L(E,G)$

#### Corollaire

- $L(E,F)$ est un sous-espace vectoriel de $F^{E}$
- $(L(E),+,\circ)$ est un anneau

#### Vocabulaire

| $-$morphisme               | Propriété         |
| ----------------- | ----------------- |
| *endo*-   | $f(E)\subset E$   |
| *iso*-    | $f$ est bijective |
| **auto**- | endo et iso                  |
#### Formules

![[Introduction aux Structures Algébriques#Sommes et Puissances]]

> mais avec $\circ$ au lieu de $\times$

#### Réciproque

Soit $f$ un isomorphisme linéaire, alors $f^{-1}$ l'est aussi.

![[Maths/Preuve - Réciproque linéaire]]

### Groupe Linéaire

On note $\text{GL}(E)$ l'ensemble des automorphismes de $E$.
C'est un groupe pour la loi $\circ$

![[Maths/Preuve - Groupe Linéaire]]

# Applications Linéaires Remarquables

Soient $E=F\oplus G$, alors pour tout $x\in E$ il existe un unique couple $(x_{1},x_{2})\in F\times G$.

On appelle *projeté* (parallèle à $G$) de $x$ sur $F$ le vecteur $x_{1}$ et on appelle *projecteur* (parallèle à $G$) l'application $p(x)=x_{1}$.

On appelle symétriqque par rapport à $F$ parallèmement à $G$ le vecteur $x_{1}-x_{2}$.

## Propriétés

### Formules

Soient $s$ la symétrie avec $F$ pour *base* et et $G$ pour *direction*, et $p$ le projecteur sur $F$ parallèle à $G$.

- $p,s\in L(E)$
- $p=\frac{s+\text{id}}{2}$
- $F=\text{Im}(p)=\text{Ker}(s-\text{id})$
- $G=\text{Ker}(p)=\text{Ker}(s+id)$

![[Maths/Preuve - Projeté et Symétrie]]

### Caractérisation

Soient $p,s\in L(E)$

- $p \text{ projecteur} \iff p\circ p = p$
- $s \text{ symétrie} \iff s \circ s = \text{id}$

![[Maths/Preuve - Caractérisation proj sym]]

### Projecteur associté

Soient $E$ un $\mathbb{K}$ espace vectoriel et $F$,$G$ deux espaces supplémentaires, avec $p$ un projecteur sur $F$ parallèle à $G$, alors $q=\text{id}-p$ est aussi un projecteur sur $G$ parallèle à $F$.

> preuve, on calcule $q^{\circ2}$, puis $\text{Im}$ et $\text{Ker}$

### Détermination AL

Soient $E,F$ deux espaces vectoriels, avec $E_{1} \oplus E_{2}$ et $f_{1}\in L(E_{1}, F)$ et $f_{2}\in L(E_{2}, F)$, alors il existe une unique $f\in L(E,F)$ qui coïncide avec $f_{1}$ et $f_{2}$

![[Maths/Preuve - Détermination AL]]
