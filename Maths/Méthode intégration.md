# $\int u'(t)v(t) \, dt = \Big[u(t)v(t)\Big]^{b}_{a} - \int _{a}^{b} u(t)v'(t) \, dt$

Appliquons une intégration par parties pour les fonctions de classe $\mathcal{C}_{1}$.
$$
\begin{cases}
u(t)=\dots \quad,\, u'(t)=\dots\\
v(t)=\dots \quad,\, v'(t)= \dots
\end{cases}
$$
$\dots$

On applique de nouveau une intégration par parties, $\dots$


# $P(x)e^{ax+b}$

On intègre l'exponentielle et dérive le polynôme.

- $\int xe^{x} \, dx = [t e^{t}] - \int e^{t} \, dt = [t e^{t}] - [e^{t}]$

donc $x e^{x} - e^{x}$ est une primitive.

- $x^{2} e^{2x}$
[[Méthode intégration par parties - Résolution.58.excalidraw]]

- $t\cos(t)=\text{Re}(t e^{it})$
[[Méthode intégration par parties - Résolution tcost.excalidraw]]

- $x\cos^{2}\left( \frac{x}{2} \right)$
[[Méthode intégration par parties xcos2x.excalidraw]]

- $x\sin(x)e^{2x}$
[[Méthode intégration par parties x2sinxe2x.excalidraw]]

## Cas général

$$
\begin{align}
\int P(t)e^{at} \, dt &= \left[ \frac{P(t)e^{at}}{a} \right] - \int \frac{P'(t)}{a} e^{at} \, dt  \\
\dots& \\
&=Q(x)e^{ax}
\end{align}
$$
- $x^{4}e^{2x}$
[[Méthode intégration par parties Pex.excalidraw]]

# $P(x)f(x)$ avec $f$ de "type $\log$"

- $\ln(x)$
[[Méthode intégration par parties lnx.excalidraw]]

- $\ln(x)^{2}$
[[Méthode intégration par parties lnx2.excalidraw]]

- $x²\arctan(x)$
[[Méthode intégration par parties x2arctanx.excalidraw]]

# Relation de récurrence

- Soit la suite $u$ définie par
$$
u_{n} = \int^{1}_{0} t^{n}e^{t} \, dt 
$$
![[Méthode intégration par parties Récur.excalidraw]]


# $\frac{ax+b}{cx²+dx+f}$


- Diviser de sorte à avoir $c=1$
- Se débarrasser de $a$

On remarque $(x²+dx+f)' = 2x+d$, on a donc
$$
\frac{ax+b}{x²+dx+f}=\frac{ \frac{a}{2}(2x+d)-\frac{ad}{2}+b }{x²+dx+f}=\frac{a}{2} \frac{2x+d}{x²+dx+f} + \left( f-\frac{ad}{2} \right) \frac{1}{x²+dx+f}
$$
Il faut donc distinguer selon le nombre de racines réelles de $X²+dX+f$

- Pour $2$ racines distinctes, **exemple**
$\frac{1}{x²-6x+8} = \frac{1}{(x-2)(x-4)}$

Le [[Théorème de développement en éléments simples]] nous donne l'existance et l'unicité de $A$ et $B$ dans $\mathbb{R}$.
Pour $x \in \mathbb{R}$,
$$
\frac{1}{(x-2)(x-4)} = \frac{A}{(x-2)} + \frac{B}{(x-4)}
$$
Pour les obtenir, on multiplie par $x-2$
$$
A = -\frac{1}{(x-4)} + \frac{B(x-2)}{x-4} \xrightarrow[]{x\to \, 2}A=-\frac{1}{2}
$$
De même en multipliant par $x-4$ avec la limite $x\rightarrow4$

On a donc
$$
\frac{1}{2}\ln|x-4| - \frac{1}{2} \ln|x-2|
$$
une primitive de $\frac{1}{(x-2)(x-4)}$

- Pour une racine réelle double
$\frac{1}{x²+10x+25}=\frac{1}{(x+5)²}$
et on a donc
$$
-\frac{1}{x+5}
$$
une primitive de $\frac{1}{x²+10x+25}$

- Si aucune racine réelle
ex: $\frac{1}{x²+4x+5}=\frac{1}{(x+2)²+1}$
donc on a 
$$
\arctan(x+2)
$$
une primitive de $\frac{1}{x²+4x+5}$ sur $\mathbb{R}$
ex: $\frac{1}{x²+2x+10}=\frac{1}{(x+1)²+9}=\frac{1}{3} \frac{\frac{1}{3}}{\left( \frac{x+1}{3} \right)² + 1}$
donc 
$$
\frac{1}{3}\arctan\left( \frac{x+1}{3} \right)
$$

[[Maths/Exercice Intégration Polynôme Quotient]]

# Changement de variable

## Exemple

$$
\begin{align}
&\int _{0}^{1/2} \sqrt{ 1-t² } \, dt, \quad t=\cos u  \\
&= \int_{\frac{\pi}{2} }^{\frac{\pi}{3} } \sqrt{ 1-\cos²(u) } \times-\sin(u)  \, du  \\
&= \int _{\frac{\pi}{3} }^{\ \frac{\pi}{2} } \sqrt{ 1-\cos²(u) } \sin(u) \, du  \\
&=\int ^{\ \frac{\pi}2 }_{\ \frac{\pi}{3} } \sin²(u) \, du \\
&= \int_{\ \frac{\pi}{3} }^{\frac{\pi}2 } \frac{1-\cos u}{2}  \, du   \\
&= \left[ x-\frac{1}{2}\sin u \right]_{t=\frac{\pi}{3}}^{\frac{\pi}2} \\
&= \frac{\pi}{12} - \frac{\sqrt{ 3 }}{8}
\end{align}
$$

[[Maths/Exercice Additionnel changement de variable]]
