---
dg-publish: true
order: 6
---
#maths/cours 

# Complément sur le corps des réels

## Borne supérieure

### Définition

Soit $A$ une partie de $\mathbb{R}$ ou de $\mathbb{Q}$, la borne supérieure de $A$, si elle existe, est le plus petit des majorants de $A$, notée

$$
\text{sup}A
$$

### Propriétés

1. Si $A$ est une partie de $\mathbb{R}$ (ou $\mathbb{Q}$) et $A$ admet un plus grand élément $x_{0}$, alors $A$ admet une borne supérieure égale à $x_{0}$. Si $A$ admet une borne supérieure, alors $A$ est majorée.

![[Preuve - Borne Supérieure]]

> pas de réciproque 

2. Il existe des parties de $\mathbb{Q}$ majorées n'admettant pas de borne supérieure dans $\mathbb{Q}$

Preuve: $A = \{ x \in \mathbb{Q} \;;\; x^{2}<2 \}$ est majorée par $861$, mais $\sqrt{ 2 }\not\in \mathbb{Q}$.
> on passe par l'absurde avec $M\pm\frac{1}{n}$ avec $n> \pm\frac{1}{\sqrt{ 2 } - M}$ ($\pm$ pour les cas $M > \sqrt{ 2 }$ et $M < \sqrt{ 2 }$)

3. On peut construire $\mathbb{R}$ comme un ensemble contenant $\mathbb{Q}$ dont toute partie majorée admet une borne supérieure 

4.  Soit $A$ une partie de $\mathbb{R}$ et $M$ un réel. Il y a équivalence entre
	1. $M = \text{sup}A$
	2. $M$ est majorant de $A$ et pour tout $\varepsilon > 0$ il existe $x \in A$ tel que $x \geq M - \varepsilon$
	3. $M$ est majorant de $A$ et il existe une suite d'éléments de $A$ telle que $u_{n} \to M$

![[Maths/Preuve - Caractérisations bornes supérieures]]


## Borne inférieure

On définit la borne inférieure de $A$ notée $\text{inf} A$ tout pareil


[[Cours Suites Exemples Caractérisation de B sup.excalidraw]]

## Partie entière, valeur approchée et densité

### Partie entière 

La partie entière de $x$ notée $\lfloor x\rfloor$ le plus grand entier relatif inférieur à $x$.

### Densité 

Soit $A$ une partie de $\mathbb{R}$, alors $A$ est dense dans $\mathbb{R}$ si pour tout $x\in \mathbb{R}$ et tout $\varepsilon > 0$, il existe $y$ tel que 

$$
\left| x-y \right| < \varepsilon 
$$
### Caractérisation 

1. $\forall x,y \in \mathbb{R}, \exists z\in A,\quad x \leq z \leq y$
2. $\forall x\in \mathbb{R}, \exists u\in A^{\mathbb{N}}, \quad u_{n} \xrightarrow[n\to +\infty]{} x$

![[Maths/Preuve - Caractérisations de la densité]]

Les ensembles $\mathbb{Q}$, $\mathbb{R} \setminus \mathbb{Q}$ et $\mathbb{D}$ sont denses dans $\mathbb{R}$.

> $\frac{\lfloor nx \rfloor}{n} \leq x \leq \frac{\lfloor nx \rfloor+1}{n}$, soit $x-\frac{1}{n} \leq \frac{\lfloor nx \rfloor}{n} \leq x$, et on a une suite qui converge vers $x$ par les gendarmes

> $x-\sqrt{ 2 } \in \mathbb{R}$ donc il existe une suite $u$ de rationnels qui tend vers $x-\sqrt{ 2 }$ et donc notre suite sera $v_{n}=u_{n}+\sqrt{ 2 }$

![[Densité Capat']]

### Approximation

Soit $x$ un réel, $y$ un décimal et $n\in \mathbb{N}$, $y$ est une approximation décimale à $10^{-n}$ près si
$$
\left| x-y \right| \leq 10^{-n} \begin{cases}
\text{par défaut si } y\leq x \\
\text{par excès } \;\; \text{si } x \leq y
\end{cases}
$$

# Définitions et généralités sur les suites

## Définitions 

Une suite de nombres réels est une application de $\mathbb{N}$ dans $\mathbb{R}$. On notera une suite $(u_{n})_{n\in\mathbb{N}}$ ou $(u_{n})_{n\geq 0}$ ou $(u_{n})$

1. Constante: $u$ une suite telle que $u_{n}=u_{0}$ 
2. Vérifiant la propriété $P$ à partir du rang $N$: pour $n\geq N$, $P(u_{n})$
3. Stationnaire: constante à partir d'un certain rang


## Structure algébrique des suites réelles

L'ensemble des suites réelles est un $\mathbb{R}-$[[Cours Espaces Vectoriels|espace vectoriel]] et a une structure d'anneau pour les lois usuelles.

>$(\mathbb{R}^{\mathbb{N}})^{*}$ est l'ensemble des suites ne s'annulant passe 

## Relation d'ordre

Une suite $(u_{n})$ est majorée (resp minorée) si la partie de $\mathbb{R}$ définie par $\{ u_{n} \;;\; n\in \mathbb{N} \}$ est majorée (resp minorée).
$$
\exists M \in \mathbb{R},\forall n\in \mathbb{N}, u_{n} ≤ M
$$

Une suite est bornée si elle est majorée et minorée 
On montrera souvent que $(\left| u_{n} \right|)$ est majorée, soit $\left| u_{n} \right| \leq M$

Une suite est croissante (resp décroissante) si
$$
\forall n \in \mathbb{N}, \quad u_{n+1} \geq u_{n}
$$
(resp $\leq$)

On parle de monotonie stricte pour $<$ ou $>$

Si une suite $u \in \mathbb{R}_{+}^{*^{\mathbb{N}}}$, on peut étudier $\frac{u_{n+1}}{u_{n}}$ et sa position par rapport à $1$.


# Convergence et Divergence

## Définitions

Soit $(u_{n})$ une suite de nombres réels, on dit que la suite converge vers $0$
$$
u_{n} \xrightarrow[n\to +\infty]{} 0 \iff \forall \varepsilon > 0, \exists N \in \mathbb{N}, \forall n \geq N, \; \left| u_{n} \right| \leq \varepsilon
$$
Une suite $(u_{n})$ tend vers $\ell$ si $(u_{n}-\ell)$ tend vers $0$.
La limite est unique

![[Maths/Preuve - Unicité de la limite de suite]]

## Propriétés 

Soient $(u_{n})$ convergente vers $\ell$ et $\alpha,\beta$ avec $\alpha<\ell<\beta$. A partir d'un certain rang, 
$$
\alpha \leq u_{n} \leq \beta
$$
> preuve en choisissant $\varepsilon = \ell - \alpha$

Si $u$ converge alors $u$ est bornée 

![[Maths/Preuve - Convergence bornes]]

Soit $u$ qui converge vers $0$ et $v$ une suite bornée, alors $uv$ converge vers $0$

![[Maths/Preuve - Convergence produit nul]]

## Opérations algébriques sur les limites

### Combinaisons linéaires 

Soient $u,v$ deux suites qui convergent vers $\ell_{1},\ell_{2}$ et $\lambda \in \mathbb{R}$, alors 
1. 
$$
u+\lambda v \to \ell_{1} + \lambda \ell_{2}
$$
2. 
$$
uv \to l_{1}l_{2}
$$
3. 
$$
\frac{1}{v} \to \frac{1}{l_{2}}
$$
si $l_{2}\neq 0$

![[Maths/Preuve - Combinaisons linéaires suites]]

## Suites divergentes

Une suite qui ne converge pas est dite divergente.

On dit qu'une suite diverge vers $+\infty$ ssi elle vérifie 
$$
\forall M\in \mathbb{R}, \exists N \in \mathbb{R}, \forall n>N, u_{n}\geq M
$$

> de même pour $-\infty$

On parle de converger dans $\overline{\mathbb{R}}=\{ -\infty, +\infty \} \cup \mathbb{R}$ si une suite converge dans $\mathbb{R}$ ou diverge vers $\pm \infty$

On étend les opérations algébriques à $\overline{\mathbb{R}}$:
Avec $u,v$ qui convergent vers $\ell_{1},\ell_{2} \in \overline{\mathbb{R}}$ et $\lambda \in \mathbb{R}^{*}$

### Tableaux de limites

| $u+v$                    | $\ell_{1}\in \mathbb{R}$ | $\ell_{1} = +\infty$ | $\ell_{1} = -\infty$ |
| ------------------------ | ------------------------ | -------------------- | -------------------- |
| $\ell_{2}\in \mathbb{R}$ | $\ell_{1}+\ell_{2}$      | $+\infty$            | $-\infty$            |
| $\ell_{2} = +\infty$     | $+\infty$                | $+\infty$            | ==NON==              |
| $\ell_{2} = -\infty$     | $-\infty$                | ==NON==              | $-\infty$            |

| $\lambda u$   | $\ell_{1}\in \mathbb{R}$ | $\ell_{1} = +\infty$ | $\ell_{1} = -\infty$ |
| ------------- | ------------------------ | -------------------- | -------------------- |
| $\lambda < 0$ | $\lambda \ell_{1}$       | $-\infty$            | $+\infty$                     |
| $\lambda>0$   | $\lambda\ell_{1}$        | $+\infty$                     |              $-\infty$        |

| $uv$                          | $\ell_{1}\in \mathbb{R}^{*}$  | $\ell_{1} = 0$ | $\ell_{1} = +\infty$ | $\ell_{1} = -\infty$ |
| ----------------------------- | ----------------------------- | -------------- | -------------------- | -------------------- |
| $\ell_{2} \in \mathbb{R}^{*}$ | $\ell_{1}\ell_{2}$            | $0$            | $+\text{sg}(\ell_{1})\infty$            | $-\text{sg}(\ell_{1})\infty$            |
| $\ell_{2}=0$                  | $0$                           | $0$            | ==NON==              | ==NON==              |
| $\ell_{2}=+\infty$            | $+\text{sg}(\ell_{1}) \infty$ | ==NON==        | $+\infty$            | $-\infty$           |
| $\ell_{2}=-\infty$            | $-\text{sg}(\ell_{1})\infty$  | ==NON==        | $-\infty$            | $+\infty$                     |

# Existence et résultats sur les limites 

## Inégalités

Si $u_{n}>0$ pour tout $n$ et $u$ convergente alors $\ell \geq 0$

![[Maths/Preuve - Signe limite]]

Si $u_{n} \leq v_{n}$ alors $\ell_{u} \leq \ell_{v}$, preuve avec $w_{n} = v_{n}-u_{n}$.

### Théorême des Gendarmes 

Soient $u_{n},v_{n},w_{n}$ telles qu'à partir d'un certain rang $u_{n}\leq v_{n}\leq w_{n}$. Si $u$ et $w$ ont la même limite, alors $v$ aussi.

![[Preuve - Théorème des Gendarmes]]

### Théorème du Gendarme à l'infini

Soient $u_{n}\leq v_{n}$ à partir d'un rang $N$
1. Si $u_{n}$ diverge vers $+\infty$ alors $v_n$ aussi 
2. Si $v_{n}$ diverge vers $-\infty$ alors $u_{n}$ aussi 

![[Maths/Preuve - Gendarmes à l'infini]]

## Suites Monotones

Soit $(u_{n})$ croissante majorée alors la suite converge vers $\ell = \text{sup}\{ u_{n};n\in \mathbb{N} \}$.

![[Maths/Preuve - Suite croissante majorée]]

Soit $(u_{n})$ croissante alors elle converge vers une limite finie ou diverge vers $+\infty$ (donc converge dans $\overline{\mathbb{R}}$)
![[Maths/Preuve - Limite Suite Croissante]]

### Théorème des suites adjacentes

Soient $u$ et $v$ deux suites, $u$ croissante et $v$ décroissante telles que $u-v \to 0$, alors $u$ et $v$ tendent vers $\ell$.

![[Maths/Preuve - Suites Adjacentes]]

## Suites extraites

Soient $(u_{n})$ et $(v_{n})$ deux suites, on dit que $v$ est extraite de $u$ si il existe $\varphi$ strictement croissante de $\mathbb{N}$ dans $\mathbb{N}$ telle que $v_{n} = u_{\varphi(n)}$.

Si $\varphi$ strictement croissante de $\mathbb{N}$ dans $\mathbb{N}$, alors $\varphi(n)\geq n$

Si une suite $u$ converge vers $\ell$, toute suite extraite converge vers $\ell$.
![[Maths/Preuve - Limite suite extraite]]

### Lemme 

Si tous les éléments d'une partition de la suite convergent vers $\ell$ alors la suite aussi.

## Théorême de [[Bernard_Bolzano|Bolzano]]-[[Weierstrass|Weierstrass]]

Soit $(u_{n})$ une suite bornée alors il existe $(v_{n})$ extraite qui converge.

![[Maths/Preuve - Bolzano-Weierstrass]]

# Générlisation à $\mathbb{C}^{\mathbb{N}}$

Soit $(z_{n})$ une suite complexe. On dit que $(z_{n})$ converge vers $\alpha$ ssi $(\text{Re}(z_{n}))$ et $(\text{Im}(z_{n}))$ convergent respectivement vers $\text{Re}(\alpha)$ et $\text{Im}(\alpha)$.

### Proposition

Soit $(z_{n})$ une suite complexe et $\alpha\in \mathbb{C}$, ces propositions sont équivalentes
1. $(z_{n})\quad \quad\;\xrightarrow[n \to +\infty]{} \alpha$
2. $(\left| z_{n}-\alpha \right|)\xrightarrow[n \to +\infty]{}0$

![[Maths/Preuve - Convergence distance complexe]]

Toutes les propriétés n'utilisant pas de relation d'ordre se transfèrent aux complexes.

### Opérations algébriques 

Les combinaisons linéaires, produits, et inverses fonctionnent comme attendu.

### Lemme

Si $z_{n}$ est convergente alors elle est bornée de module.

### Bolzano-Weierstrass complexe 

[[Preuve - Bolzano-Weierstrass|Bolzano-Weierstrass]] fonctionne aussi, l'hypothèse est "bornée de module"

> preuve triviale (fin d'heure) 🗿 🏃‍♂️ 
> On applique BW pour la convergence des réels puis BW à la sous-suite finale sur la partie imaginaire


# Suites usuelles et comparaison de suites 

## Suites Usuelles

![[Maths/Suites Usuelles]]

## Comparaison de suites 

### Définitions 

Soient $u$ et $v$ deux suites sans termes nuls (parfois à partir d'un certain rang)

1. La suite $u$ est dominée par $v$ noté $u_{n}=\mathcal{O}(v_{n})$ (ou $v_{n}=\mathcal{O}(u_{n})$) si la suite $\left( \frac{u_{n}}{v_{n}} \right)$ est bornée.
2. La suite $u$ est négligeable devant la suite $v$ noté $u_{n} = o(v_{n})$ si la suite $\left( \frac{u_{n}}{v_{n}} \right)$ tend vers $0$.
3. La suite $u$ est équivalente à la suite $v$ noté $u_{n} \sim v_{n}$ si la suite $\left( \frac{u_{n}}{v_{n}} \right)$ tend vers $1$

### Propriétés 

1. $\ln(n)^{\alpha} = o(n^{\beta})$
2. $n^{\alpha}=o(\rho^{n})$
3. $n^{\alpha}=o(\rho^{\beta n})$
4. $\rho^{n}=o(n!^{\alpha})$
5. $n!=o(n^{n})$

![[Maths/Preuve - Croissance Comparée de suites]]

### Opération sur les équivalences

Soient $3$ suites $u,v,w$ et $\alpha\in \mathbb{R}^{*}$

1. $u_{n}\to\alpha \iff u_{n} \sim \alpha$
2. $u_{n} \sim v_{n}  \implies u_{n}w_{n} \sim v_{n}w_{n}$
3. $u_{n}\sim v_{n} \land v_{n}\to 0 \implies u_{n} \to 0$

>[!warning]- Attention à l'infini 
>la propriété $2.$ permet de faire un produit FINI d'équivalents

![[Maths/Définition Limite de e]]

### Calcul d'équivalents 

1. $u_{n}=o(v_{n})\implies u_{n}+v_{n} \sim v_{n}$
2. Les propositions suivantes sont équivalentes 
	- $u_{n}\sim v_{n}$
	- $u_{n}-v_{n} = o(v_{n})$
	- $\frac{u_{n}-v_{n}}{v_{n}}\to 0$

![[Maths/Preuve - Calcul d'équivalents de suites]]

![[Maths/Lemme - Logarithmes d'équivalents]]

## Formule de [[James_Stirling_(mathématicien)|Stirling]]

$$
n! \sim \sqrt{ 2\pi n }\left( \frac{n}{e} \right)^{n}
$$

![[Maths/Preuve - Formule de Stirling]]


## Suites implicites

Il est fréquent de définir une suite comme solution d'une suite d'équations.

![[Maths/Exemple de suites implicites]]
