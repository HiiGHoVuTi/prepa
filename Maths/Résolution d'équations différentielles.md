---
dg-publish: true
---

#maths #cours #équation-différentielle 

# Equations différentielles linéaires d'ordre $1$

On considère l'équation d'inconnue $y\in\mathbb{K}^I$ avec $a,b,c\in \mathbb{K}^I$
$$
a(t)y'(t) + b(t)y(t) = c(t)
$$
Elle est d'ordre $1$ et linéaire.

Exemples:

|                                | Linéaire | Ordre |
| ------------------------------ | -------- | ----- |
| $y'(t)-y(t)=0$                 | oui      | $1$   |
| $y'(t)y(t) + y(t)^{3} = 0$     | non      | $1$   |
| $y''(t)+y(t)=0$                | oui      | $2$   |
| $\ddot{\theta} + \sin(\theta)$ | non      | $2$     |
 

## Equation homogène

Une équation différentielle linéaire est dite *homogène* si son second membre est nul.
$$
a(t)y'(t) + b(t)y(t)=0
$$

## Proposition - Sous-Espace Vectoriel

L'ensemble des solutions d'une équation différentielle linéaire homogène est un sous-[[Cours Espaces Vectoriels|espace vectoriel]] des fonctions dans $\mathbb{K}^{I}$. On note $S$ l'ensemble des fonctions.
![[Maths/Preuve - Solutions sous-espace vectoriel]]

## Proposition - Solutions Primitive

Soient $a,b \in \mathbb{K}^{I}$ continues, $a \neq 0$ sur $I$, on note $A$ la primitive de $\frac{b}{a}$. Les solutions de l'équation
$$
a(t)y'(t) + b(t)y(t) = 0
$$
sont l'ensemble
$$
S = \{ y(t)=\lambda e^{-A(t)} \,;\, \lambda \in \mathbb{K} \}
$$
![[Maths/Preuve - Solutions Equation Homogène]]

On utilisera [[Quelques Résultats de base sur les Intégrales et Primitives]] pour trouver $A$.

Exemple:
- Déterminer des solutions de
$$
(1+t²)y'(t) + 2ty(t) = 0
$$
$$
\frac{b}{a} = \frac{2t}{1+t²} \implies A(t)=\ln(1+t^{2})
$$
donc
$$
S=\{ t \to \lambda e^{-\ln(1+t^{2})} \,;\, \lambda \in \mathbb{R} \}
$$

- $e^{x}y'(t) + \cosh(t)y(t) = 0$
[[Résolution d'équations différentielles - Exemple 2 Homogène.excalidraw]]

## Théorème d'annulation

Soient $a,b \in \mathbb{K}^{I}$ continues et $a \neq 0$ sur $I$, $f$ une solution sur $I$ de
$$
a(t)y'(t)+b(t)y(t) = 0
$$
et $t_{0} \in I$

On a alors l'équivalence suivante
$$
f(t_{0}) = 0 \iff f = \Delta_{0}
$$

![[Maths/Preuve - Théorème annulation équation homogène]]

## Equation différentielle linéaire d'ordre $1$ avec second membre

On considère
$$
a(t)y'(t)+b(t)y(t)=c(t)
$$
Et on lui associe une équation homogène où $c(t)=0$

## Proposition - Ensemble Solution

Soit $y_{0}$ une solution sur $I$, alors on a
$$
S = \{ y_{0}+y_{h} \;;\; y_{h} \in S_{H} \}
$$

![[Preuve - Ensemble solution premier ordre]]

Grâce à cette proposition il suffit de trouver une solution particulière et de résoudre l'équation homogène.

Exemple:
[[Résolution d'équations différentielles - Exercice Résolution HP.excalidraw]]

## Principe de superposition

Soient $y_{i}$ une solution  de $a(t)y'(t)+b(t)y(t) = c_{i}(t)$ et $\lambda_{1}, \lambda_{2} \in \mathbb{K}$ alors
$$
\lambda_{1}y_{1} + \lambda_{2}y_{2}
$$
est solution de
$$
a(t)y'(t) + b(t)y(t) = \lambda_{1}c_{1}(t)+\lambda_{2}c_{2}(t)
$$

![[Maths/Preuve - Equation différentielle combinaison linéaire solutions]]

> exemple: Résoudre  
$$
y'(t) + y(t) = e^{t} +1
$$
Solution de l'équation homogène:
$$
y'(t)+y(t)=0 \implies y(t)=\lambda e^{-t}
$$
Solution particulière ? On sépare l'équation
$$
\begin{cases}
y'(t)+y(t)=e^{t} \implies y(t)=\frac{e^{t}}{2} \\
y'(t)+y(t)=1 \;\implies y(t)=1
\end{cases}
$$
On a alors
$$
y(t) = \lambda e^{-t}+\frac{e^{t}}{2}+1
$$

## Variation de la constante

Soient $a,b,c \in \mathbb{K}^{I}$ continues avec $a$ ne s'annulant pas sur $I$ et $y_{0}$ une solution non triviale sur $I$ de l'équation homogène associée à  $E: a(t)y'(t)+b(t)y(t)=c(t)$.
On peut trouver une solution de $E$ de la forme:
$$
y_{\lambda}=\lambda(t)y_{0}(t)
$$

> [[Résolution d'équations différentielles - Explication variation constante.excalidraw|Explication]]
> [[Résolution d'équations différentielles - Exemple variation constante.excalidraw|Exemple]]
> [[Résolution d'équations différentielles - Exercice variation constante.excalidraw]]

## Unicité de la solution au problème de Cauchy

On considère le problème
$$
E: \begin{cases}
a(t)y'(t)+b(t)y(t)=c(t) \\ 

y(t_{0}) = y_{0}
\end{cases}
$$
avec $a,b,c \in \mathbb{K}^{I}$, $t_{0} \in I$ et $y_{0}\in \mathbb{K}$.

Alors ce système $E$ a une unique solution.

![[Preuve - Problème Cauchy]]

## _Un cas particulier important_

Pour $a,b \in \mathbb{K}$ et $c\in\mathbb{K}^{I}$ continue.
$$
ay'(t)+by(t)=c(t)
$$

### Solution homogène

$$
y_{H}(t)=e^{-t\times b/a} \\
$$

> on appelle $a\alpha+b=0$ l'équation caractéristique

### Solution particulière

#### $c(t) = P(t)e^{\beta t}$

On peut chercher une solution particulière de $E$ sous la forme $Q(t)e^{\beta t}$
 où 
$$
\text{deg}Q=\text{deg}P+\begin{cases}
1 \text{ si } \beta \text{ solution du polynôme caractéristique} \\
0 \text{ sinon}
\end{cases}
$$
[[Maths/Preuve - Solution particulière polynôme exponentielle]]
[[Résolution d'équations différentielles Exemples.excalidraw]]

# Equations différentielle linéaire à coéfficients constants du second ordre

On considère
$$
ay''(t)+by'(t)+cy'(t)=d(t)
$$
avec $a,b,c \in \mathbb{K}$ et $d \in \mathbb{K}^{I}$ continue.

## Equation homogène

On considère le cas où $d(t)=0$, et son équation caractéristique
$$
a\alpha^{2}+b\alpha+c=0
$$

1. Si l'équation caractéristique a deux racines distinctes $\alpha_{1}$ et $\alpha_{2}$, on a alors
$$
y(t) = \lambda_{1}e^{\alpha_{1}t}+\lambda_{2}e^{\alpha_{2} t}
$$
2. Si la racine $\alpha$ est double
$$
y(t)= (\lambda_{1}t+\lambda_{2})e^{\alpha t}
$$

![[Preuve - Solutions Equation Homogène Ordre 2]]
[[Résolution d'équations différentielles - Exemples Equadiff 2deg constants.excalidraw]]

### Ensemble solution

![[Preuve - Solutions Eq Diff 2 coefficients réels]]

### Forme de pulsation amortie

Soient $a,b,c \in \mathbb{R}$ avec $a\neq 0$ et $b²-4ac<0$, les solutions ==réelles== de 
$$
ay'' + by' + cy = 0
$$
sont de la forme
$$
y(t)=\lambda \cos(\omega t+\phi)e^{At} \text{ avec } \begin{cases}
\omega = \text{Im}(\alpha) \\
A = \text{Re}(\alpha) \\
\lambda,\phi \in \mathbb{R}
\end{cases}
$$
![[Preuve - Forme solution pulsation amortie]]

### Visualisation


```functionplot
---
title: 
xLabel: 
yLabel: 
bounds: [-1,5,-10,10]
disableZoom: false
grid: false
---
f(x)=10*exp(-0.5*x)*cos(5x)
```

[[Résolution d'équations différentielles - Exercice amortissement.excalidraw|Exercice]]

## Equation avec second membre

### Ensemble solutions

Soit $y_{0}$ une solution particulière de $(E)$ et $S_{E_{h}}$ l'ensemble des solutions de l'équation homogène. L'ensemble des solutions de $E$ est
$$
S_{E} = \{ y_{h} + y_{0} \;;\; y_{h} \in S_{E_{h}} \}
$$
![[Maths/Preuve - Solutions Equation Ordre 2]]

### Cas polynômial

Soient $a,b,c \in \mathbb{C}$, $a \neq 0$, $\beta\in \mathbb{C}$, $P \in \mathbb{C}[X]$ et l'équation
$$
ay''+by'+cy=P(t)e^{\beta t}
$$
on cherche des solutions de forme $Q(t)e^{\beta t}$ avec
$$
\text{deg}Q=\text{deg}P + \Phi_{aX^{2}+bX+c}(\beta)
$$
avec $\Phi_{R}(x)$ la multiplicité de la racine $x$ dans le polynôme $R$

> les $\Phi(\beta)$ premier coefficients sont nuls ($x^{0},\,\dots\,$)

[[Résolution d'équations différentielles - Exercice Membre Droit Polynôme 2 ordre.excalidraw|Résolutions]]

## Problème de Cauchy

### Cauchy

Soient $a,b,c \in\mathbb{K}$ avec $a=0$ et $d \in \mathbb{K}^{I}$ continue, $t_{0} \in I$ et $y_{0},y_{1} \in \mathbb{K}$, alors le système d'inconnue $y$ 
$$
\begin{cases}
ay''+by'+cy=d \\
y(t_{0})=y_{0} \\
y(t_{0})=y_{1}
\end{cases}
$$
admet une unique solution sur $I$.

![[Preuve - Cauchy Problème de Cauchy 2]]
