---
aliases: [Cours Polynomes]
order: 11
dg-publish: true
---

#maths/cours 

Dans ce chapitre, $\mathbb{K}$ est un corps quelconque.

# La structure $\mathbb{K}[X]$

## Définition

On note $\mathbb{K}[X]$ l'ensemble des polynômes dans $\mathbb{K}$ à *indéterminée* $X$, soit les objets de la forme
$$
P=\sum^{+\infty} a_{k}X^{k}
$$
où $(a_{n})\in \mathbb{K}^{n}$ est une suite à support fini

> $a_{k}X^{k}$ est un monôme de degré $k$, et $a_{k}$ le coéfficient de degré $k$.

## Opérations et degré

On pose $P=\sum p_{k}X^{k}, Q=\sum q_{k}X^{k}\in \mathbb{K}[X]$, $\lambda\in \mathbb{K}$

### Règles Opératoires

- Combinaison linéaire
$$
P+\lambda Q=\sum(p_{k}+\lambda q_{k})X^{k}
$$
- Produit
$$
PQ = \sum_{k}\left( \sum_{\ell=0}^{k} p_{\ell}q_{k-\ell} \right)X^{k}
$$

> On a un $\mathbb{K}-$[[Cours Espaces Vectoriels#Définition|espace vectoriel]], groupe abélien additif, et [[Introduction aux Structures Algébriques#Anneau - Définition|anneau]] *commutatif*.
> Les inversibles sont $\mathbb{K}^{*}$

### Composition

$$
P \circ  Q = \sum a_{k}Q^{k}
$$

### Degré

Soit $P\neq 0_{\mathbb{K}}$, on appelle degré de $P$ noté $\text{deg}P$ la quantité
$$
\text{deg}P = \text{sup}\{ k\,; \; k\in \mathbb{N}, p_k \neq 0 \}
$$

> Donc on a $\text{deg}0 = -\infty$

On appelle $a_{\text{deg}P}$ le *coefficient dominant*, et $P$ est unitaire si son coefficient dominant est $1_{\mathbb{K}}$.

#### Opérations sur les degrés

1. $\text{deg}\lambda P=\text{deg}P$
2. $\text{deg}P+Q\leq \text{max}\{ \text{deg}P,\text{deg}Q \}$
avec égalité ssi $p_{\text{degP}}\neq -q_{\text{deg}Q}$
3. $\text{deg}PQ = \text{deg}P+\text{deg}Q$
4. $\text{deg}P\circ Q=\text{degP}\times \text{deg}Q$
pour $\text{deg}P \neq 0 \neq \text{deg}Q$

> Preuve: exercice d'entraînement
> Pour $\text{deg}PQ$, on montre qu'il est majoré puis on montre que le coefficient n'est pas nul


#### Intégrité

L'anneau $\mathbb{K}[X]$ est intègre.

> Preuve: Soient $P,Q\in \mathbb{K}[X]\setminus \{ 0_{\mathbb{K}} \}$, on a $\text{deg}P,\text{deg}Q\geq 0$ donc $\text{deg}PQ \neq -\infty$

## Division Euclidienne

### [[Cours Arithmétique#Division Euclide Euclidienne|Division Euclidienne]]

Soient $A,B\in \mathbb{K}[X]$, alors il existe un unique couple $(Q,R)\in \mathbb{K}[X]^{2}$ tel que
$$
A=BQ+R, \quad \text{deg} R<\text{deg} B
$$
On appelle $Q$ le quotient et $R$ le reste de la division euclidiennt de $A$ par $B$

> On dit que $B$ divise $A$ ssi $R = 0$

![[Preuve - Division Polynômes]]


```haskell
-- type Polynome = ...
division P Q
	| deg P < deg Q = (0, Q)
	| otherwise     = (coef * Q + qt, rn)
	where
		deltaDeg = deg P - deg Q
		coef     = coefDom P / coefDom Q
		(qn, rn) = division (P - coef * Q) Q
```

## Racines

### Application Polynômiale

On définit l'application polynômiale telle que:
$$
\varphi : \mathbb{K}[X]\to \mathbb{K}\to \mathbb{K}
$$
On remplace formellement $X$ par $x\in \mathbb{K}$.

La fonction $\varphi(P)$ est la fonction polynômiale associée à $P$.

#### Morphisme

La fonction $\varphi$ est un morphisme d'anneaux et d'espaces vectoriels.

### Racine

Soit $P\in \mathbb{K}[X]$, alors $\alpha\in \mathbb{K}$ une racine de $P$ si et seulement si
$$
\varphi(P)(\alpha)=0
$$

On a alors équivalence entre
1. $\alpha$ racine de $P$
2. $(X-\alpha)\mid P$


![[Maths/Preuve - Factorisation Polynômes]]

#### *K*orollaire

Soit $P\in \mathbb{K}[X], (\alpha_{i})\in \mathbb{K}^{\textlbrackdbl 1,n \textrbrackdbl}$ deux à deux disjoints, on a équivalence entre

1. Pour tout $i\in \textlbrackdbl 1,n \textrbrackdbl$, $\alpha_{i}$ racine de $P$
2. $\prod X-\alpha_{i}$ divise $P$

![[Maths/Preuve - Korollaire]]

### Degré

1. Soit $P\in\mathbb{K}[X]$ non-nul, si $P$ a $p$ racines distinctes, alors $\text{deg}P\geq p$.
De plus, si $\text{deg}P=p$, on a $\lambda\in \mathbb{K}$
$$
P=\lambda \prod_{i=1}^{p} X-\alpha_{i}
$$
2. L'application polynômiale est injective
3. Si un polynôme a une infinité de racines il est nul

![[Maths/Preuve - Propositions sur les degrés]]

![[Maths/Polyôme de Tchebytchev]]

# Dérivation et racines multiples

## Dérivation

### Définition

On définit la dérivation $D$ sur $\mathbb{K}[X]$ comme l'unique endomorphisme du $\mathbb{K}-$espace vectoriel tel que

1. $D(X)=1$
2. $D(PQ) = D(P)Q + PD(Q)$

### Dérivée du polynôme

Soit $P=\sum^{n}_{k=1} a_{k}X^{k}$, on définit $P'=DP$, alors on a
$$
P' = \sum^{n}_{k=1} ka_{k}X^{k-1}
$$

### Dérivation usuelle

#### Binôme de [[Leibniz]]

Soit $n\in \mathbb{N}$, $P,Q\in \mathbb{K}[X]$

$$
(PQ)^{(n)}= \sum_{k=0}^{n} {n\choose k}P^{(n)}Q^{(n-k)}
$$

![[Preuve - Formule de Leibniz]]

### Formule de Taylor Polynomiale

Soient $P\in \mathbb{K}[X]$ et $a\in \mathbb{K}$ tel qu'on puisse diviser sans soucis
$$
P=\sum_{k=0}^{+\infty}P^{(k)}(a) \frac{(X-a)^{k}}{k!}
$$

![[Maths/Preuve - Taylor]]

## Racines multiples

### Définition

Soient $P$ un polynôme de $\mathbb{K}[X]$, $\alpha\in \mathbb{K}$ et $n\in \mathbb{N}$, on dit que $\alpha$ est racine d'ordre au moins $n$ de $P$ si $(X-\alpha)^{n}\mid P$
L'ordre est exactement $n$ si $(X-\alpha)^{n+1} \not\mid P$

### Racines multiples et dérivée

Soit $P\in \mathbb{K}[X],\alpha\in \mathbb{K},n\in \mathbb{N}$, il y a équivalence entre
- $\alpha$ est racine d'ordre exactement $n$
- Pour $k\in \textlbrackdbl 0,n-1 \textrbrackdbl, P^{(k)}(\alpha)=0$ et $P^{(n)}(\alpha)\neq0$

![[Maths/Preuve - Dérivée Racine]]

### Factorisation

Soient $P$ un polynôme de $\mathbb{K}[X]$ et $(\alpha_{1},\dots,\alpha^{p})\in \mathbb{K}^{p}$ un $p-$uplet de scalaires distincts deux à deux et $(n_{1},\dots n_{p})\in \mathbb{N}^{p}$.
Si pour tout $k\in\textlbrackdbl 1,p \textrbrackdbl, \alpha_{k}$ est une racine d'ordre $n_{k}$ alors
$$
(X-\alpha_{1})^{n_{1}}\dots(X-\alpha_{p})^{n_{p}} |P
$$
Si de plus $\text{deg}P=\sum n_{i}$ alors il existe $\lambda\in \mathbb{K}$ tel que
$$
P = \lambda \prod (X-\alpha_{i})^{n_{i}}
$$

![[Maths/Preuve - Factorisation Polynôme]]

#### Majoration de la multiplicité des racines

Soient $P\in \mathbb{K}[X]$ non-nul, $\alpha_{i}\in \mathbb{K}$ distincts deux à deux racines d'ordre $n_{i}\in \mathbb{N}$, alors
$$
\sum_{k=1}^{n}n_{k}\leq \text{deg} P
$$

# Arithmétique dans $\mathbb{K}[X]$

## PGCD

### Idéaux

> Contrairement à $\mathbb{Z}$, tous les sous-groupes de $\mathbb{K}[X]$ ne sont pas des idéaux.
> Contre-exemple: $\mathbb{L}=\{ aX+b\;;\; a,b\in \mathbb{K} \} \subset \mathbb{K}[X]$

Les idéaux de $\mathbb{K}[X]$ sont de forme
$$
P\mathbb{K}[X] = \{ PQ\;;\; Q\in \mathbb{K}[X] \}
$$
avec $P\in \mathbb{K}[X]$ fixé

![[Maths/Preuve - Idéaux de Polynômes]]

### Définition

On dit que $H$ est un des plus grands diviseurs de $A$ et $B$ ssi
$$
A\mathbb{K}[X]+B\mathbb{K}[X] = H\mathbb{K}[X]
$$
il n'en existe qu'un qui soit unitaire, on le notera $A\land B$

>[!note]- Preuve
>Supposons $I=P\mathbb{K}[X]=Q\mathbb{K}[X]$ unitaires de même degré.
>On a $\text{deg}P-Q<\text{deg}P$. Si $P-Q\neq 0$, contradiction.

### Propositions

- $P\mathbb{K}[X]\subset Q\mathbb{K}[X] \iff Q \mid P$
- Soient $A,B$ non tous nuls, et $P\mid A,P\mid B$. On a $P\mid A\land B$
![[Maths/Preuve - PGCD Divisibilité]]

On pose $\hat{A}$ égal à $A$ divisé par son coefficient dominant.
- $A\land A = \hat{A}$
- $A\land B=B\land A$
- $A\land 0 = \hat{A}$
- $A \land 1 = 1$

## Algorithme d'Euclide

### Lemme d'Euclide

$$
A\land B=(A-BQ)\land B
$$
Il suffit de montrer $A\mathbb{K}[X]+B\mathbb{K}[X]=(A-BQ)\mathbb{K}[X]+B\mathbb{K}[X]$

![[Maths/Preuve -  Lemme d'Euclide Poly]]

C'est la même que [[Preuve - Algorithme d'Euclide]]

### Algorithme d'[[Euclide]]

![[Preuve - Analyse algo Euclide]]
> on peut n'introduire qu'une suite.

### Bézout

Pour $A,B$ on a $U,V$ tels que
$$
AU+BV = A\land B
$$

![[Preuve - Algorithme étendu d'Euclide]]

## Polynômes premiers entre eux

Soient $A,B$ tels que $A\land B=1$, on dit qu'ils sont premiers entre eux.

### Théorème de Bezout

On a équivalence entre
- $A\land B=1$
- $AU+BV=1$

![[Preuve - Théorème de Bezout]]

### Lemme de [[Gauss]]

Si $A\land B=1$, $A\mid BC$ alors on a $A\mid C$

![[Preuve - Lemme de Gauss]]

## PPCM

On définit aussi le $PPCM$ de $A,B$ noté $A\lor B$ tel que que
$$
A\mathbb{K}[X]\cap B\mathbb{K}[X]=(A\lor B)\mathbb{K}[X]
$$

# Polynômes irréductibles, scindés, Viète

## Polynôme Irréductible

Soit $P\in \mathbb{K}[X]\setminus \mathbb{K}$, alors $P$ est dit irréductible si pour toute factorisation $P=QR$, on a $\text{deg}R \times \text{deg}Q=0$.

>[!warning] Dépend de $\mathbb{K}$
>On a $X^{2}+1$ est réductible dans $\mathbb{C}[X]$ mais pas dans $\mathbb{R}[X]$.

Les polynômes de degré $1$ sont irréductibles quelque soit le corps.
Les polynômes de degré $2,3$ sont irréductibles si et seulement si ils n'ont pas de racine dans $\mathbb{K}$.
Pour des degrés supérieurs, on peut être réductible sans avoir de racine.

## Polynôme Scindé

On dit que $P$ est scindé sur $\mathbb{K}$ si on a $\lambda, \alpha_{i}\in \mathbb{K}$ tels que
$$
P=\lambda \prod (X-\alpha_{k})
$$

##  Formules sur les racines

>[!note] Rappel
>Pour un polynôme de degré $2$ de racines $\alpha,\beta$, avec $P=aX^{2}+bX+c$ on a 
>$\alpha+\beta=-\frac{b}{a}$ et $\alpha\beta=\frac{c}{a}$

Pour le degré $3$ on a
$$
\alpha_{1}+\alpha_{2}+\alpha_{3} = -\frac{a_{1}}{a_{3}}, \quad \alpha_{1}\alpha_{2}\alpha_{3} = -\frac{a_{0}}{a_{3}}
$$

### Produit et Somme

Soit $P$ scindé, n a
$$
\sum_{k=1}^{n} \alpha_{k} = - \frac{a_{n-1}}{a_{n}}, \quad \prod_{k=1}^{n} \alpha_{k} = (-1)^{n}  \frac{a_{0}}{a_{n}}
$$

### Relations de Viète

Soit $P=a_{3}X^{3}+a_{2}X^{2}+a_{1}X+a_{0}$, et $\alpha_{1}, \alpha_{2}, \alpha_{3}$ ses racines
$$
P=a_{3}X^{3}+a_{3}(\alpha_{1}+\alpha_{2}+\alpha_{3})X^{2}+a_{3}(\alpha_{1}\alpha_{2}+\alpha_{1}\alpha_{3}+\alpha_{2}\alpha_{3})X - a_{3}\alpha_{1}\alpha_{2}\alpha_{3}
$$

Soit $P$ scindé, $a_{i}$ ses coéfficients et $\alpha_{i}$ ses racines, on a 
$$
\sum \sigma_{p}(P) = \sum_{i_{1}<\dots<i_{p}} \alpha_{i_{1}}\times \dots \times \alpha_{i_{p}} = (-1)^{p} \frac{a_{n-p}}{a_{n}}
$$
Preuve par développement brutal.

# Factorisation dans $\mathbb{C}[X]$ et $\mathbb{R}[X]$

## Théorème d'Alembert-[[Gauss]] 

Tout polynôme dans $\mathbb{C}[X]$ de degré supérieur ou égal à $1$ admet une racine dans $\mathbb{C}$.

![[Maths/Preuve - Alembert-Gauss]]

### Factorisation unique

Tout polynôme de $\mathbb{C}[X]^{*}$ est scindé et se factorise de manière unique sous la forme
$$
P=\lambda \prod_{k}^{m}  (X-\alpha _{k})^{n_{k}}
$$

![[Preuve - Factorisation Polynôme C]]

### Irréductibles de $\mathbb{C}[X]$

Les irréductibles de $\mathbb{C}[X]$ sont exactement les polynômes de degré $1$.

![[Preuve - Irréductibles de C]]

### Racines Communes

Soient $A,B\in \mathbb{K}[X]$, $\mathbb{K}\in \{ \mathbb{R}, \mathbb{C} \}$, on a équivalence entre

1. $A\land B=1$
2. $A$ et $B$ n'ont pas de racine commune dans $\mathbb{C}$

![[Maths/Preuve - Racines Communes]]

### Polynômes conjugués

On note $\overline{P}$ le conjugué de $P\in \mathbb{C}[X]$ dont tous les coéfficients sont conjugués

L'application $\varphi = P \mapsto \overline{P}$ est $\mathbb{R}-$linéaire telle que $\overline{PQ}=\overline{P}\,\overline{Q}$

> preuve par linéarité de la somme et $\mathbb{R}-$linéarité de $\overline{(-)}$

### Racines de Conjugués 

Soient $P\in \mathbb{C}[X]$, $\alpha\in \mathbb{C}$ et $p\in \mathbb{N}$, il y a équivalence entre
- $\alpha$ est une racine d'ordre $p$ de $P$
- $\overline{\alpha}$ est une racine d'ordre $p$ de $\overline{P}$

![[Maths/Preuve - Racine Conjuguée]]

## Dans $\mathbb{R}[X]$

### Factorisation unique

$$
P=\lambda \prod (X-\alpha_{k})^{n_{k}} \prod (X^{2}+\beta _{k}X+\gamma_{k})^{m_{k}}
$$

avec $\beta^{2}_{k}-4\gamma_{k}<0$

![[Preuve - Factorisation Polynômes R]]


### Irréductibles de $\mathbb{R}[X]$

Les irréductibles de $\mathbb{R}$ sont exactement les polynômes de degré $1$ ou $2$ au discriminant strictement négatif.

