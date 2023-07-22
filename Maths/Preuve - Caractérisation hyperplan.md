---
dg-publish: true
---

$1\implies 3$
Il existe $f\in L(E, \mathbb{K})$ avec $H=\text{Ker}f$ donc
$$
\begin{align}
x&=\sum_{k=1}^{n}a_{k}e_{k} \in H \\
\iff f(x)&=f\left( \sum\dots \right)=0 \\
\iff 0&=\sum_{k=1}^{n} a_{k}f(e_{k})
\end{align}
$$
On pose $\lambda_{i}=f(e_{i})$ et on sait qu'ils ne sont pas tous nuls car $f$ n'est pas identiquement nulle.

$3 \implies 2$

On introduit $\varphi_{k}=\sum_{i=1}^{n} a_{i}e_{i}\mapsto a_{k}$ (bien définie car base), $φ_{k}$ est linéaire.

Alors $f=\sum_{k=1}^{n}\lambda_{k}\varphi_{k}$. Comme $(\lambda_{i})\neq(0)$ on a $f$ non-nulle.

Alors

$$
\begin{align}
x = \sum a_{k}e_{k} &\in \text{Ker}f \\
\iff f(x) &= 0 \\
\iff \sum a_{k}\lambda_{k}&=0
\end{align}
$$

donc $H=\text{Ker}f$.
