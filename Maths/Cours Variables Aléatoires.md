---
aliases: [Proba, Variables Aléatoires]
dg-publish: true
order: 17
active: true
---

#maths/cours 

Dans ce chapitre, on suppose $(\Omega,P)$ un espace probabilisé fini.

# Couple de Variables Aléatoires

## Couple

Soient $X,Y$ deux variables aléatoires réelles avec $X(\Omega)=\{ x_{1}\dots x_{n} \}$ et $Y(\Omega)=\{ y_{1}\dots y_{m} \}$.
La loi du couple $XY$ est l'application $\mathcal{L}:\Omega(X)\times \Omega(Y)\to [0,1]$
$$
\mathcal{L} (x_{i},y_{j})=P((X=x_{i})\cap (Y=y_{j}))
$$
C'est une probabilité.

## Information du couple

On peut déduire la loi de $X$ et $Y$ à partir de la loi du couple $XY$ mais pas la réciproque.

Preuve: $(Y=y_{i})$ est un système complet d'événements.
$$
P(X=x_{i})=\sum_{j}P((X=x_{i})\cap(Y=y_{j}))
$$

## Probabilité conditionnelle

On définit une loi conditionnelle telle que

$$
P(Y=y_{i}\mid X=x)=\frac{P((X=x)\cap(Y=y_{i}))}{P(X=x)}
$$

# Indépendance

>[!warning] Ne pas confondre incompatible et indépendant !

## Evénements Indépendants

Deux événements sont indépendants si et seulement si
$$
P(A\cap B)=P(A)P(B)
$$

Deux événements incompatibles sont indépendants si et seulement si l'un est impossible.

### Définitions d'indépendence

1. Deux à deux indépendants $P(A_{i}\cap A_{j})=P(A_{i})P(A_{j})$
2. Mutuellement indépendants $P(\bigcap A_{i})=\prod P(A_{i})$

### Indépendences de variables

$$
P((X=x)\cap(Y=y))=P(X=x)P(Y=y)
$$

### Indépendence d'issues de variables

Si $X$ et $Y$ sont indépendentes, alors $(X\in A)$ et $(Y\in B)$ le sont aussi.

![[Maths/Preuve - Indépendance issues]]

### Indépendence de fonctions

Si $X$ et $Y$ sont indépendantes, alors $f(X)$ et $g(Y)$ aussi.

>Preuve lourde, on introduit les images réciproques des parties de $f(X(\Omega))$

## Espérance et Variance de variables indépendantes

### Espérance Indépendante

$$
E(XY)=E(X)E(Y)
$$

![[Maths/Preuve - Espérance Indépendente]]

La condition est suffisante mais pas nécessaire.

### Variance Indépendante

Si $X$ et $Y$ sont indépendantes,

$$
V(X+Y)=V(X)+V(Y)
$$

![[Maths/Preuve - Variance indépendantes]]

### Centrée / Réduite

Une variable aléatoire $X$ est dite centrée si $E(X)=0$ et centrée réduite si de plus $V(X)=\sigma(X)=1$.

Pour toute variable aléatoire $X$, la variable $X^{\star}$ est centrée
$$
X^{\star}=\frac{X-E(X)}{\sigma(X)}
$$

### Covariance

La covariance de $X,Y$ notée $\text{cov}(X,Y)$ est définie par
$$
E\Big(\big(X-E(X)\big)\times\big(Y-E(Y)\big)\Big)
$$

>[!example] Covariances usuelles
>$\text{cov}(X,X)=V(X)$
>$\text{cov}(X,Y)=0$ si $X,Y$ indépendentes ($E(XY)=E(X)E(Y)$)

On dit que $X,Y$ sont *non-corrélées* si $\text{cov}(X,Y)=0$

### Coefficient de corrélation

On définit le *coefficient de corrélation* entre $X$ et $Y$ par
$$
\gamma_{X,Y}=\frac{\text{cov}(X,Y)}{\sigma(X)\sigma(Y)}
$$
On remarque que $\gamma_{X,X}=1$.

#### Intervalle de définition

Le coefficient de corrélation est défini dans l'intervalle $[-1,1]$.

![[Maths/Preuve - coefficient correlation]]

### Inégalité de Bienaymé - Чебышëв

#### Inégalité de Марков

Pour $Y\geq 0$, $\lambda> 0$,
$$
P(Y\geq\lambda)\leq \frac{E(Y)}{\lambda}
$$

![[Maths/Preuve - Inégalité de Markov]]

#### Bienaymé - Tchébychev

Soit $X$ une variable aléatoire réelle et $\lambda>0$,
$$
P(\left| X-E(x) \right|\geq \lambda)\leq \frac{V(X)}{\lambda^{2}}
$$

![[Preuve - Bienaymé]]

### Ecart à la moyenne

Soient $X_{1}\dots X_{n}$ des variables mutuellement indépendentes, identiqument distribuées.

$$
P\left( \left| \frac{1}{n}\sum X_{k} - E(X) \right| \geq \varepsilon \right) \leq \frac{V(X_{1})}{n\varepsilon^{2}}
$$

![[Maths/Preuve - Ecart à la moyenne]]

# Lois Usuelles

## Loi Uniforme

Soit $X$ telle que $X(\Omega)=(x_{1},\dots,x_{n})$, $X$ admet une loi uniforme si et seulement si
$$
P(X=x_{i})=\frac{1}{n}
$$
On écrit alors $X\hookrightarrow\mathcal{U}(X(\Omega))$ et on abrège parfois $\mathcal{U}(\textlbrackdbl 1,n \textrbrackdbl)=U(n)$
- $E(X)=\frac{n+1}{2}$
- $V(X)=\frac{n^{2}-1}{12}$

## Loi de Bernoulli

Soit $X$ une variable aléatoire réelle, on dit que $X$ suit une loi de Bernoulli de paramètre $p$ noté $X\hookrightarrow \mathcal{B}(p)$ si et seulement si $X(\Omega)=\{ 0,1 \}$ avec $P(X=1)=p$.
- $E(X)=p$
- $V(X)=p(1-p)$

### Lien avec événements

Il y a équivalence entre
1. $X\hookrightarrow\mathcal{B}(p)$
2. Il existe $A=X^{-1}(\{ 1 \})\in \Omega$ tel que $P(A)=p$ et $X=\chi_{A}$

## Loi Binomiale

On dit que $X$ suit une loi binomiale de paramètres $n,p$ noté $X\hookrightarrow \mathcal{B}(n,p)$ si et seulement si $X(\Omega)=\textlbrackdbl 0,n \textrbrackdbl$ et que
$$
P(X=k)={n\choose k}p^{k}(1-p)^{n-k}
$$
- $E(X)= np$
- $V(X)=n\times p(1-p)$

![[Maths/Preuve - Loi Binomiale]]

### Bernoulli indépendentes

Si $n$ variables aléatoires suivant la même loi de Bernoulli sont indépendentes (iid), leur somme suit une loi binômiale.

![[Maths/Preuve - Bernoulli Binomiale]]

#### Corollaire - Preuve Espérance Variance

On retrouve rapidement les résultats de [[Cours Variables Aléatoires#Loi Binomiale|la preuve ci-desssus]]. 

## Tableau Récapitulatif

| Loi                | Espérance       | Variance             |
| ------------------ | --------------- | -------------------- |
| $\mathcal{U}(n)$   | $\frac{n+1}{2}$ | $\frac{n^{2}-1}{12}$ |
| $\mathcal{B}(p)$   | $p$             | $p(1-p)$             |
| $\mathcal{B}(n,p)$ | $np$            | $n\times p(1-p)$                     |
