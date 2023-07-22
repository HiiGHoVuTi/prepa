---
dg-publish: true
order: 8
---

#maths/cours

On suppose sans précisions contraires $I$ un intervalle de $\mathbb{R}$ et $f\in \mathbb{R}^{I}$

# Terminologie, définitions et propriétés

## Voisinage et propriétés locales

Soit $a$ réel dans $I$ ou une de ses bornes. On dit que $f$ vérifie une propriété $P$ au voisinage de $a$ ssi:
- si $a\in \mathbb{R}$
$$
\exists \eta > 0, \forall x\in I, \left| x-a \right|\leq \eta \implies P(x)
$$
- si $a =+\infty$
$$
\exists M\in \mathbb{R},\forall x\in I, x\geq M \implies P(x)
$$
- si $a=-\infty$
$$
\exists M \in \mathbb{R}, \forall x\in I, x\leq M \implies P(x)
$$

## Borne supérieure (inférieure) et extrema

- La fonction $f$ est majorée (minorée, bornée) sur $I$ si $f(I)$ est majorée (minorée, bornée)
- On dit que $f$ admet un maximum (minimum) sur $I$ si $f(I)$ admet un maximum (minimum)
- Un maximum (minimum) est local si la propriété est vraie au voisinage de $x_{0}$
- La borne supérieure (inférieure) de $f$ sur $I$ est celle de $f(I)$

## Limite d'une fonction et continuité

### Limite ponctuelle 

Soit $a$ élément ou borne de $I$ et $b$ élément de $\mathbb{R}$, on dit que $f$ admet la limite $b$ en $a$ ssi la propriété $\left| f(x)-b \right|\leq \varepsilon$ est vraie au voisinage de $a$
- Si $a \in \mathbb{R}$ 
$$
\forall \varepsilon > 0, \exists \delta > 0, \forall x \in I, \left| x-a \right|\leq \delta\implies \left| f(x)-b \right|\leq \varepsilon
$$
- Si $a=+\infty$
$$
\forall \varepsilon > 0, \exists M > 0, \forall x\in I, x \geq M \implies \left| f(x)-b \right|\leq\varepsilon
$$
- Si $a=-\infty$
$$
\forall \varepsilon > 0, \exists M < 0, \forall x \in I, x\leq M \implies \left| f(x)-b \right|\leq \varepsilon
$$

On dit que $f$ admet une limite de $+\infty$ ($-\infty$) en $a$ si pour tout $M$, $f(x)\geq M$ ($\leq$) est vrai au voisinage de $a$.

>[!note] Si $f$ pas définie en $a$
>On étend cette définition à $I \setminus \{ a \}$ en considérant le même voisinage 

On note alors 
$$
f(x)\xrightarrow[x \to a]{} b
$$
### Continuité 

Soit $a\in I$, si $f$ admet une limite en $a$ alors c'est $f(a)$. On dit que $f$ est continue en $a$

$$
\forall \varepsilon>0, \exists \delta>0,\forall x\in I,\left| x-a \right|\leq \delta \implies \left| f(x)-f(a) \right|\leq \varepsilon
$$

On dit que $f$ est continue sur $I$ si elle est définie pour tout $a\in I$

### Prolongement 

Soient $a \in I$ ou une borne *finie* de $I$, $f\in \mathbb{R}^{I\setminus \{ a \}}$ telle que $f$ admet une limite *finie* $b$ en $a$, on définit $\overline{f}$ l'unique prolongement de $f$ à $I$ continue en $a$
$$
\overline{f}(x)=\begin{cases}
b &\text{si } x=a \\
f(x)&\text{sinon} \\
\end{cases}
$$

![[Maths/Preuve - Prolongement]]

### Limite et Continuité à gauche (ou à droite)

Soient $a$ un élément ou borne de $I$ et $b\in \overline{\mathbb{R}}$, on dit que $f$ admet une limite à gauche (à droite) ssi
$$
\forall \varepsilon>0, \exists \eta>0, \forall x\in I, a-\eta\leq x< a \implies \left| f(x)-b \right|\leq\varepsilon
$$
($a<x\leq a+\eta$)

>[!warning] Cas infini
>Le cas écrit ici est la cas fini, le cas infini se rédige en changeant la partie de droite de l'implication

>[!example] Exemple
>La partie entière est continue à droite et pas à gauche 

Si une fonction est continue à gauche et à droite, elle l'est continue en ce point.

# Résultats sur les limites

## Opérations algébriques

### Lemme de bornes

Si $f(x)\xrightarrow[x \to a]{}b$
- $\forall\alpha <b, \alpha\leq f(x)$
- $\forall\beta>b,f(x)\leq \beta$

![[Maths/Preuve - Lemme de Bornes]]


### Lemme de produit nul

Si $f$ et $g$ tendent vers $0$, alors leur produit aussi.
![[Maths/Preuve - Lemme Produit Nul]]


### Limites

![[Cours Suites#Tableaux de limites]]

## Inégalités de limites et existence de limites 

Soit $a$ un élément ou une borne de $I$, on suppose que $f$ admet une limite $\ell$ en $a$. Alors si $f$ est positive au voisinage de $f$, $\ell \geq0$

![[Maths/Preuve - Limite positive]]

## Théorème des Gendarmes

![[Cours Suites#Théorême des Gendarmes]]

De même, mais avec des fonctions, au voisinage de $a$.

![[Preuve - Théorème des Gendarmes (fonctions)]]


>[!note] A l'infini 
>On généralise [[Cours Suites#Théorème du Gendarme à l'infini|ce résultat]] aussi à l'infini si la suite est minorée (resp. majorée) par une suite qui diverge vers $+\infty$ (resp. $-\infty$)

## Limite à gauche 

Soit $f$ une fonction sur $I$ et $a$ un élément ou borne de $I$. Si $f$ est majorée et croissante au voisinage de $a$, alors $f$ admet une limite finie $\ell$ au voisinage de $a$.

![[Maths/Preuve - Limite à gauche]]

## Caractérisation séquentielle de la limite

Soient $f$ une fonction définie sur $I$, $a$ un élément ou bord de $I$, on a l'équivalence suivante 
1. $f$ admet une limite $\ell\in \overline{\mathbb{R}}$
2. Pour toute suite $(u_{n})_{n\in \mathbb{N}}$ d'éléments de $I$ qui convergent vers $a$,  $(f(u_{n})_{n\in \mathbb{N}})$ converge vers $\ell$

![[Maths/Preuve - Caractérisation séquentielle limite]]

###  Corollaire - Continuité 

Soit $f$ définie sur $I$ et $a\in I$ alors on a l'équivalence suivante 
1. $f$ est continue en $a$
2. Pour toute suite $(u_{n})_{n\in \mathbb{N}}$ d'éléments de $I$ qui convergent vers $a$ alors $(f(u_{n}))_{n\in \mathbb{N}}$ est continue en $a$

> ça n'a aucun sens, je ne sais pas quelle est la bonne propriété (à corriger)

### Corollaire - Composition

Soient $f$ une fonction définie de $I$ dans $J$ et $g$ définie de $J$ dans $\mathbb{R}$, et $a$ un élément ou borne de $I$.
Si $f$ admet une limite en $a$ et $g$ admet une limite en $f(a)$
Alors $g\circ f$ admet la même limite que $g$ en $a$.

![[Maths/Preuve - Limite Composée]]


# Continuité sur un Intervalle 

On note $\mathcal{C}^{0}(I)$ l'ensemble des fonctions continues sur $I$.

## Opérations sur les fonctions continues sur un intervalle 

Soient $f,g\in \mathcal{C}(I)$ et $\lambda \in \mathbb{R}$, on a

- $f+ \lambda g \in \mathcal{C}(I)$
- $f \times g \in \mathcal{C}(I)$

>[!note] [[Introduction aux Structures Algébriques#Anneaux et Corps|Anneaux]] et [[Cours Espaces Vectoriels]] 
>On a bien un sous-anneau et sous-espace-vectoriel de ceux des fonctions

Soit $f\in \mathcal{C}(I)$ à images dans $J$ et $g\in \mathcal{C}(J)$, alors $g\circ f \in \mathcal{C}(I)$

![[Maths/Preuve - Continuité composée]]

## Image d'un intervalle 

### Théorème des valeurs intermédiaires

Soit $f$ continue sur $I$ et $a<b \in I$ alors 
$$
\forall y\in [f(a),f(b)], \exists c\in [a,b], f(c)=y
$$
![[Maths/Preuve - TVI]]

### Théorème des bornes atteintes

Soient $f$ une fonction continue sur le ==segment== $[a,b]$, alors $f$ admet un minimum *et* un maximum sur $[a,b]$.

![[Preuve - Théorème des bornes atteintes]]

### Corollaire - Segments

Soit $f$ continue sur un segment $[a,b]$ alors il existe $\mu,\kappa\in [a,b]$ tels que 
$$
f([a,b])=[f(\mu),f(\kappa)]
$$

### Corollaire - Intervalle 

Soit $f$ continue sur un intervalle $I$, alors $f(I)$ est un intervalle.

![[Maths/Preuve - Corollaire Intervalle]]

### Théorème de la Bijection

Soit $f$ continue strictement monotone sur un intervalle $I$ alors $f$ est une bijection de $I$ dans $f(I)$ un intervalle.

![[Preuve - Théorème de la Bijection]]

### Fonctions continues bijectives

Soit $f$ une fonction continue sur $I$. Ces propositions sont équivalentes:
1. $f$ strictement monotone sur $I$
2. $f$ injective

![[Maths/Preuve - Injectivité Monotonie]]


### Intervalle

Soit $f$ une fonction monotone sur $I$ intervalle, alors les propositions suivantes sont équivalentes 
1. $f$ continue sur $I$
2. $f(I)$ est un intervalle

![[Maths/Preuve - Intervalle continuité]]

### Corollaire 

Soit $f$ une fonction continue bijective de $I$ intervalle dans $f(I)$ alors $f^{-1}$ est continue de $f(I)$ dans $I$.

![[Maths/Preuve - Continuité réciproque]]

# Retour sur les suites

Soit $f$ une fonction telle que $f(I)\subset I$. On considère la suite définie par:
$$
\begin{cases}
u_{0} \in I  \\
u_{n+1} = f(u_{n})
\end{cases}
$$

Si la fonction $f$ est continue et $(u_{n})$ converge vers $\ell$ alors $\ell=f(\ell)$.

![[Maths/Preuve - Point fixe suite]]

Si $f$ est croissante de $I$ dans $I$ alors la suite $(u_{n})$ est monotone 

![[Maths/Preuve - Monotonie suite récurrence]]

Si $f$ est décroissante de $I$ dans $I$, on ne peut rien dire de la suite mais les suites extraites (termes pairs et impairs) vérifient la propriété précedente.

