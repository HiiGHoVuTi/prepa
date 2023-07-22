---
dg-publish: true
order: 10
aliases: [Cours Convexité]
---

#maths/cours

Dans la suite, sans précisions contraires, $I$ est un intervalle non-vide et $f$ est une fonction définie sur $I$.

# Fonction Convexe

## Définition

Une fonction $f$ est dite convexe sur $I$ si pour tout $\lambda\in [0,1]$ et tous $x,y\in I$, 
$$
f(\lambda x+(1-\lambda)y)\leq \lambda f(x)+(1-\lambda)f(y)
$$

Géométriquement, toute corde est au-dessus de la courbe.

Au contraire, on dit que $f$ est concave si $-f$ est convexe.

# Propriétés

## Bijection

Soient $x_{1},x_{2}\in I$ avec $x_{1}\neq x_{2}$ alors l'application suivante
$$
\begin{align}
\varphi: [0,1] &\to [x_{1},x_{2}]\\
\varphi= \lambda&\mapsto \lambda x_{1}+(1-\lambda x_{2})
\end{align}
$$

>Preuve par étude de fonction ou parachutage de réciproque.

## Inégalité des pentes

Soit $f$ une fonction convexe sur $I$ et $x_{1}<x_{2}<x_{3} \in I$, alors
$$
\frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}\leq \frac{f(x_{3})-f(x_{1})}{x_{3}-x_{1}}\leq \frac{f(x_{3})-f(x_{2})}{x_{1}-x_{2}}
$$
Si pour tous triplets une des inégalités est vraie, on a la réciproque.

![[Maths/Preuve - Inégalité des pentes]]

## Moyenne Pondérée

Soient $(x_{1},\dots ,x^{n})\in I^{n}$ et $(\lambda_{1},\dots,\lambda_{n})\in  \mathbb{R}_{+}^{n}$ avec les $\lambda_{i}$ non tous nuls, on a
$$
\frac{\sum\lambda_{k}x_{k} }{\sum\lambda_{k}} \in I
$$

![[Maths/Preuve - Moyenne Pondérée]]

> On peut toujours normaliser les $\lambda_{i}$

## Barycentre

Soit $(M_{k}\in \mathbb{R}^{m})_{k\in\textlbrackdbl 1,n \textrbrackdbl}$ et $(\lambda_{k}\in \mathbb{R})_{k\in \textlbrackdbl 1,n \textrbrackdbl}$ avec $\sum\lambda_{k}\neq 0$. Alors le barycentre est l'unique point tel que
$$
\sum\lambda_{k}\vec{GM_{k}} = \vec{0}
$$

## Inégalité de Jensen

Soient $f$ convexe, $(x_{1},\dots,x_{n})\in I$, $(\lambda_{1},\dots,\lambda _{n})\in [0,1]^{n}$ avec $\sum\lambda_{i}=1$.
On a alors
$$
f\left( \sum\lambda_{k}x_{k} \right)\leq \sum\lambda_{k}f(x_{k})
$$

![[Maths/Preuve - Inégalité de Jensen]]

## Position par rapport à une sécante

Soient $f$ une fonction convexe sur $I$, et $a<b\in I$, avec $D$ la droite reliant $(a,f(a))$ et $(b,f(b))$. 
Alors pour $x\in I$, on a $M(x,f(x))$ en-dessous de la droite $D$ si $x\in [a,b]$, au-dessus sinon.

## Continuité

Soit $f$ une fonction convexe sur $I$ et $a$ un point (pas une borne) de $I$, alors $f$ est continue en $a$.

![[Maths/Preuve - Continuité Convexe]]

# Convexité et dérivée

Soit $f$ dérivable, alors elle est convexe si et seulement si $f'$ est croissante.

![[Maths/Preuve - Convexité Dérivée]]

## Tangentes

Soit $f$ dérivable convexe sur $I$ alors la courbe de $f$ est au-dessus de ses tangentes

$$
f(a)+f'(a)(x-a) \leq f(x)
$$

![[Maths/Preuve - Convexité Tangentes]]

## Dérivée Seconde

Si $f$ est dérivable deux fois, elle est convexe si et seulement si $f'' \geq 0$

# Résultats de Convexité

## Inégalités usuelles

- $\sin x\leq x$ dans $\mathbb{R}_{+}$
- $\ln(1+x)\leq x$
- $1+x\leq e^{x}$
- $x\leq \tan x$
($\tan''(x)=2\tan x$)
- $\frac{2}{\pi}x\leq \sin x$ pour $x\in [0, \frac{\pi}{2}]$
(eq de la sécante)

## Deux inégalités classiques

### Inégalité Arithmético-géométrique

Pour $a_{i}\in \mathbb{R}_{+},$

$$
\left(\prod a_{i}\right)^{1/n} \leq \frac{1}{n}\sum a_{i}
$$

> Pour $n=2$, on obtient
$$
0\leq \frac{a_{1}-2\sqrt{ a_{1}a_{2} }+a_{2}}{2}
$$

![[Maths/Preuve - Inégalité arithmético géométrique]]

### Inégalité de [[Hölder]]

Soient $p,q\in \mathbb{R}_{+}^{*}$ tels que $\frac{1}{p}+\frac{1}{q}=1$, on a

$$
\sum x_{i}y_{i}\leq \left( \sum x_{i}^{p} \right)^{1/p}\left( \sum y_{i}^{q} \right)^{1/q}
$$

![[Maths/Preuve - Inégalité Hölder]]

## Concavité, convexité et points d'inflexion

### Inflexion

Soient $f$ dérivable sur $I$, $a<b<c\in I$, si $f$ est convexe sur $[a,b]$ et concave sur $[b,c]$ alors la courbe de $f$ traverse sa tangente en $b$. On dit que la courbe de $f$ admet un point d'inflexion en $b$.

 