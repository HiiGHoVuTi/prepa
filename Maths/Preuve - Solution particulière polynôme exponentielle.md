---
dg-publish: true
---

Soit $\alpha=-\frac{b}{a}$ solution de l'équation caractéristique

$$
\begin{align}
y(t)&=\lambda(t)e^{\alpha t} \\
y'(t)&=\lambda'(t)e^{\alpha t} + \lambda(t)\alpha e^{\alpha t} \\
ay'(t)+by(t)&=\lambda'(t)e^{\alpha t}+(a\alpha+b)\lambda(t)e^{\alpha t} \\
&= \lambda(t)e^{\alpha t}
\end{align}
$$

Donc
$$
\begin{align}
a\lambda'(t)e^{\alpha t}&=P(t)^{n}e^{\beta t} \\
\lambda'(t)&=\frac{P(t)}{a}e^{(\beta-\alpha)t}
\end{align}
$$
Si $\beta-\alpha \neq 0$ on cherche une primitive avec $Q$ du même degré que $P$
Sinon, le degré augmente de $1$.