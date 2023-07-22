---
dg-publish: true
---

Soit $\varphi$ définie sur $I$ avec
$$
\varphi = \int_{a}^x  f(t)   dt
$$
et $F$ une primitive de $f$ sur $I$.
On a $\varphi$ la primitive de $f$ s'annulant en $a$.
Il existe donc $\alpha\in \mathbb{K}$ avec $\varphi - F = \alpha$.
$$
\begin{align}
\varphi(b) &= \int_{a}^b f(t) \, dt  \\
\varphi(a) &= \int_{a}^a f(t) \, dt = 0 \\ \\

\varphi(b) - \varphi(a) &= F(b) + \alpha - F(a) - \alpha \\ \\

\int_{a}^b f(t) \, dt &= F(b) - F(a)
\end{align}
$$
