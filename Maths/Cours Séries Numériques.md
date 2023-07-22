---
aliases: [Séries]
dg-publish: true
order: 20
active: true
---

#maths/cours 

# Généralités

## Série

On appelle série une suite de forme $S_{n}= \sum^{n} u_{k}$ avec $u\in \mathbb{K}^{\mathbb{N}}$.
Le terme $u_{k}$ est appelé le terme général de la série. On appelle $S_{n}$ une somme partielle.
On dit que la série converge si $S_{n}$ converge, on écrit alors
$$
\sum^{+\infty}u_{k}
$$
On appelle reste d'une série la suite
$$
R_{n} = \left(\sum^{+\infty}_{k=0} u_{k}\right) - S_{n} = \sum_{k=n+1}^{+\infty} u_{k}
$$

## Série géométrique

Soit $\alpha\in \mathbb{C}$, on pose $u_{k}=\alpha^{k}$. Pour $\left| \alpha \right|< 1$,
$$
\sum^{+\infty}_{k=1} \alpha^{k}=\frac{1}{1-\alpha}
$$
Et on a le reste suivant
$$
\frac{\alpha^{n+1}}{1-\alpha}
$$

## Propriétés

### Convergence de la série

Soit $u_{n}$ le terme général d'une série convergente, on a $u_{n}\to 0$.

### Convergence de la suite

Il y a équivalence entre
- $u_{n}$ converge
- $\sum u_{n+1}-u_{n}$ est une série qui converge

# Séries à termes positifs

## Critères de convergence

### Majoration

Il y a équivelence entre

- La série converge
- La suite des sommes partielles est majorée

### Majoration

Si $u_{n}\leq v_{n}$ alors si la série de terme $v_{n}$ converge, alors celle de $u_{n}$ aussi.

## Comparaison Série-Intégrale

- Si $f$ décroissante
$$
\int_{1}^{n+1} f(t) \, dt \leq \sum_{k=1}^{n}f(k)\leq \int _{0}^{n}f(t) \, dt 
$$

- Si $f$ croissante
$$
\int _{0}^{n} f(t) \, dt \leq \sum_{k=1}^{n} f(k)\leq \int _{1}^{n+1}f(t) \, dt 
$$

![[Maths/Preuve - Comparaison Série Intégrale]]

#### Corollaire

Soit $f$ continue, monotone et positive sur $\mathbb{R}^{+}$, il y a équivalence entre
- La série de terme général $f(k)$ converge
- La suite $\int _{0}^{n} f(t) \, dt$ converge

### Série de Riemann

La série de terme général $\frac{1}{n^{\alpha}}$ converge si et seulement si $\alpha>1$.

![[Maths/Preuve - Série de Riemann]]

### Comparaison des termes généraux

Soient $u_{n},v_{n}$ positives
- Si $u_{n}=O(v_{n})$ et la série de $v_{n}$ converge alors la série de $u_{n}$ converge
- Si $u_{n}=o(v_{n})$ et la série de $v_{n}$ converge alors la série de $u_{n}$ converge
- Si $u_{n}\sim v_{n}$ et la série de $v_{n}$ congerge alors la série de $u_{n}$ converge

On montre la première qui implique les autres.

### Série Harmonique

$$
H_{n}=\sum \frac{1}{k}=\ln(n)+\gamma+o(1)
$$

![[Maths/Preuve - Convergence Harmonique]]

#### Corollaire - Convergence

- Si $u_{n}=o\left( \frac{1}{n^{\alpha}} \right)$ avec $\alpha>1$, $\sum u_{n}$ converge
- Si $\alpha\leq 1$, et $\frac{1}{n^{\alpha}}=o(u_{n})$, $\sum u_{n}$ diverge

## Développement Décimal d'un Réel

### Développement Décimal

Pour $x\in [0,1[$, il existe une unique suite $(x_{k})_{k\in\mathbb{N}^{\star}}$ de $\textlbrackdbl 0,9 \textrbrackdbl^{\mathbb{N}^{\star}}$ non stationnaire à $9$ telle que
$$
x= \sum^{+\infty} 10^{-k}x_{k}
$$

![[Maths/Preuve - Développement Décimal]]

#### Corollaire - $\mathbb{R}$ plus grand que $\mathbb{N}$

Il n'existe pas de surjection de $\mathbb{N}$ dans $[0,1[$.

![[Maths/Preuve - surjection nr]]

#### Corollaire

Soit $x\in[0,1[$, alors $x\in \mathbb{Q}\iff$ le développement de $x$ est ultimement périodique
![[Maths/Preuve - Critère de rationalité]]

# Séries Absolument Convergentes

## Série Absolument Convergente

Soit $u\in \mathbb{C}^{\mathbb{N}}$, on dit que la série de terme général est absolument convergente si la série de terme général $\left| u_{n} \right|$ converge.


## Propriétés

### Implication

La série est absolument convergente $\implies$ la série est convergente

![[Maths/Preuve - Convergence et aconvergence]]

>[!warning] Pas de réciproque
>$\sum \frac{(-1)^{k}}{k+1}$


### Sous-Espace Vectoriel

L'ensemble des séries absolument convergentes est un sous-espace vectoriel des séries convergentes noté $\ell^{1}(\mathbb{N})$.
Le $1$ indique la puissance de la valeur absolue, $\left| u_{k} \right|^{\alpha}$

# Quelques outils supplémentaires

##  Théorème des Séries Alternées

Soit $(u_{n})$ une suite décroissante de limite nulle. La série de terme général $(-1)^{n}u_{n}$ converge et le reste est inférieur à $u_{n+1}$ en valeur absolue.

![[Maths/Preuve - Séries Alternées]]

>[!Warning] Ne pas utiliser d'équivalents, ça marche pas
>$u_{n}=\frac{(-1)^{n}}{\sqrt{ n }}+\frac{1}{n} \sim \frac{(-1)^{n}}{\sqrt{ n }}$ mais on ne peut pas appliquer le critère

## Produit de Cauchy

Pour deux séries de termes généraux $u_{n},v_{n}$,
$$
c_{n}=\sum_{k=0}^{n} u_{k}v_{n-k}
$$

### Convergence

Si les deux séries sont absolument convergentes, alors le produit de Cauchy est le terme d'une série abolument convergente et $\sum c_{n}= \left( \sum u_{n} \right)\left( \sum v_{n} \right)$.

![[Maths/Preuve - Produit de Cauchy]]

>[!warning] Il faut la CVA
>$u_{n}=\frac{(-1)^{n}}{\sqrt{ n+1 }}$

## Exponentielle Complexe

Soit $z\in \mathbb{C}$,
$$
e^z= \sum_{k=0}^{+\infty} \frac{z^{k}}{k!}
$$

![[Maths/Preuve - Exponentielle Complexe]]

### Propriété Exponentielle

![[Maths/Preuve - Exponentielle Produit]]

### Imaginaires Purs

En se plaçant sur $i\mathbb{R}$, on définit
$$
\begin{cases}
\cos(x)=\text{Re}(e^{ix}) \\
\sin (x)=\text{Im}(e^{ix})
\end{cases}
$$
On retrouve directement $\cos ^{2}x+\sin ^{2}x=1$ et la (im)parité des fonction.

# Exemples de développements asymptotiques


## Problème de Bâle

Soit $u_{n}=\frac{1}{n^{2}}$, on peut montrer que la série tend vers $\frac{\pi^{2}}{6}$.
Par comparaison somme intégrale,

$$
\frac{1}{k}-\frac{1}{k+1}\leq \frac{1}{k^{2}}\leq \frac{1}{k-1}-\frac{1}{k}
$$
puis pour le reste
$$
\frac{1}{n+1}-\frac{1}{m+1} \leq \sum_{k=n+1}^{m} \frac{1}{k^{2}} \leq \frac{1}{n}-\frac{1}{m}
$$
et à la limite en $m$,
$$
\frac{1}{n}\leq \sum^{+\infty}_{k=n+1} \frac{1}{k^{2}} \leq \frac{1}{n}
$$
donc le reste est équivalent à $\frac{1}{n}$ en $+\infty$.

## Un exemple divergent

Soit $u_{n}=\frac{1}{\sqrt{  n }}$,
$$
\begin{align}
\int^{k+1}_{k} \frac{dt}{\sqrt{ t }} &\leq \frac{1}{\sqrt{ k }}\leq \int ^{k}_{k-1} \, \frac{dt}{\sqrt{ t }} \\
1-2\sqrt{ 2 }+\sqrt{ n+1 }&\leq \sum_{k=1}^{n} \frac{1}{\sqrt{ k }} \leq 2\sqrt{ n }-1
\end{align}
$$
Donc la somme est équivalente à $2\sqrt{ n }$ par le th des gendarmes.
On pose $\mathfrak{v}_n$ = $S_{n}-2\sqrt{ n }$.
Alors
$$
\begin{align}
\mathfrak{v}_{n+1}-\mathfrak{v}_{n} &= \frac{1}{\sqrt{ n+1 }}-2\sqrt{ n+1 }+2\sqrt{ n } \\
&= \frac{1}{\sqrt{ n }} \left( 1+\frac{1}{n} \right)^{-1/2}-2n^{1/2}\left( 1+\frac{1}{n} \right)^{1/2}+2n^{1/2} \\
&= n^{-1/2} \left( 1-\frac{1}{2n}+o\left( \frac{1}{n} \right) \right)-2n^{1/2}\left( 1+\frac{1}{2n}+o\left( \frac{1}{n} \right) \right)+2n^{1/2} \\
&= -\frac{1}{2}n^{-3/2} +o\left( \frac{1}{\sqrt{ n }} \right) \\
&= o\left( \frac{1}{\sqrt{ n }} \right)
\end{align}
$$
On remplace alors les $o$ par des $O$ et on obtient
$$
-\frac{1}{2n\sqrt{ n }}+O\left( \frac{1}{n\sqrt{ n }} \right) \text{ converge}
$$
Donc $\mathfrak{(v_{n})}=(S_{n}-2\sqrt{ n })$ converge.
Enfin $\sum^{+\infty}u_{n}=2\sqrt{ n }+\ell+o(1)$

## Stirling

On a $\ln(n!)=\sum\ln k$
$$
\begin{align}
\int ^{k}_{k-1} \ln(t) \, dt &\leq \ln(k)\leq \int _{k}^{k+1}\ln(t) \, dt  \\
n\ln(n)-n+1 &\leq \sum_{k=2}^{n}\ln(k) \leq \dots\sim n\ln(n)
\end{align}
$$
Donc $\sum_{k=2}^{n}\ln(k)\sim n\ln(n)$

On pose $v_{n}= (\sum^{n} \ln(k)) - n\ln(n)$.
$$
\begin{align}
v_{n+1}-v_{n}&=\sum^{n+1}\ln(k)-(n+1)\ln(n+1)-\sum^{n}\ln(k)-n\ln(n) \\
&=-n\ln(n+1)+n\ln(n) \\
&=-n\left( \ln\left( 1+\frac{1}{n} \right) \right) \\
&\sim -1
\end{align}
$$
Donc la série diverge grossièrement, $v_{n+1}-v_{n}+1 \to 0$
$$
\begin{align}
v_{n+1}-v_{n}=-1+\frac{1}{2n}+&O\left( \frac{1}{n^{2}} \right) \\
&\quad\text{CVA}
\end{align}
$$
Donc $\sum^{m-1} v_{k+1}-v_{k}= \sum (-1) + \sum \frac{1}{2k}+\ell + o(1)$.
Donc $v_{n}-v_{1}=-(n-1)+\frac{1}{2}H_{n-1}+\ell + o(1)$.
Et $v_{n}=-n+\frac{1}{2}H_{n-1}+\ell+1+v_{1}+o(1)$.

Enfin, 
$$
\begin{align}
\ln(n!)&=n\ln(n)-n+\frac{1}{2}\ln(n)+\frac{1}{2}\gamma+\ell +1+o(1) \\
n! &= e^{n\ln n}e^{-n}e^{1/2 \ln n} e^{\gamma/2+\ell +1}e^{o(1)} \\
n! &\sim e^{\gamma/2+\ell+1} \times n^{n}e^{-n}\sqrt{ n }
\end{align}
$$
On rappelle
$$
I_{n}=\int ^{\pi/2}_{0}\cos(t)^{n} \, dt \quad\quad\quad I_{n} \sim \sqrt{ \frac{\pi}{2n} } 
$$
Or $I_{n}$ s'exprime avec des factorielles, $I_{2p}=\frac{(2p)!}{2^{2p}} \frac{\pi}{2} \sim \frac{1}{2} \sqrt{ \frac{\pi}{p} } \sim e^{\gamma/2+\ell+1} \dots$
Et donc par une simplification divine,
$$
e^{\gamma/2+\ell+1}= \sqrt{ 2\pi }
$$
*enfin*,
$$
n! \sim \sqrt{ 2\pi n }\,n^{n}e^{-n}
$$

# Familles Sommables

## Familles sommables de réels positifs

### Définition d'une famille sommable

On étend les règles de l'addition à $\mathbb{R}_{+}\cup \{ +\infty \}$.

Soit $(u_{i})_{i\in I}$ avec $I$ un ensemble et $u_{i}\in \mathbb{R}_{+}\cup \{ +\infty \}$, on définit la somme de la famille comme
$$
\sum_{i\in I} u_{i}= \text{sup}_{F \subset I, F \text{ finie}} \sum_{i\in F} u_{i}
$$

Si $I$ est fini, on fait directement la somme.
Si $I=\mathbb{N}$, on a une série.
La somme ainsi définie ne prend pas en compte l'ordre (cohérent car tout est positif).

Une famille de réels positifs est dite sommable si sa somme est finie ($\in \mathbb{R}$).

### Stabilité

Les familles sommables de réels positifs sont stables par combinaison linéaires de réels positifs

![[Maths/Preuve - sommables stable]]

### Support

Soit $u_{i}$ sommable, le support de $u_{i}$ est fini ou dénombrable

![[Maths/Preuve - support dénombrable]]

### Sommation par Paquets

Si $I=\underline\bigcup_{j\in \mathfrak{J}} I_{j}$ est une union disjointe et $(u_{i})_{i\in I}$ est sommable, alors $(u_{i})_{i\in I_{j}}$ est sommable aussi, et 
$$
\sum_{i\in I} u_{i}= \sum_{j\in \mathfrak{J}} \sum_{i\in I_{j}} u_{i}
$$

![[Maths/Preuve - Sommation par Paquets]]

## Familles sommables de nombres complexes

Une famille $(u_{i}\in \mathbb{C})_{i\in I}$ est sommable si la famille $(\left| u_{i} \right|)_{i\in I}$ l'est. On note $\ell^{1}(I)$ l'ensemble des familles sommables indexées par $I$.

### Critère de somme

Si $(u_{i})_{i\in I}$ est une famille de complexes avec $\left| u_{i} \right|\leq v_{i}$ et $(v_{i})_{i\in I}$ sommable réelle, alors $(u_{i})$ est sommable.

### Borne Sup'

Si $(u_{i})_{i\in I}$ est une famille sommable sur $\mathbb{C}$. Pour tout $\varepsilon>0$ il existe $\mathfrak{I}$ tel que 
$$
\left| \sum_{i\in I} u_{i} - \sum_{i\in \mathfrak{I}} u_{i} \right|\leq \varepsilon
$$

>Preuve: on pose $u^{\mathbb{R},+},u^{\mathbb{R},-},u^{i\mathbb{R},+}$,$u^{i\mathbb{R},-}$.
>on prend alors des parties telles que les distances sont $\leq \frac{\varepsilon}{4}$. 
>puis l'union des parties ok

### Somme par paquets

pareil


### Théorème Fubini

Soient $(a_{i})_{i\in I},(b_{i})_{i\in J}$, alors $(a_{i}b_{j})_{(i,j)\in I\times J}$ est sommable et le produit est le produit.

![[Maths/Preuve - Fubini]]

Par récurrence immédiate, on a autant de variables que voulu


