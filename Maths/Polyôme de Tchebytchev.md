---
dg-publish: true
---

Montrons qu'il existe un unique polynôme $T_{n}$ tel que
$$
\cos(nx)=T_{n}(\cos(x))
$$

*Existance*:

On a $\cos(nx)=Re((\cos(x)+i\sin(x))^{n})$
Onn calcule
$$
(\cos(x)+i\sin(x))^{n}=\sum {n\choose k} (i\sin x)^{k}(\cos x)^{n-k}
$$
donc
$$
\begin{align}
\cos(nx)&=\sum_{2k\leq n} {n\choose 2k}(-1)^{k}(\sin x)^{2k}(\cos x)^{n-2k} \\
&= \sum_{2k\leq n}{n\choose 2k} (\cos ^{2}(x)-1)^{k}\cos^{n-k}(x)
\end{align}
$$
donc
$$
T_{n}=\sum_{2k\leq n}{n\choose 2k} (X^{2}-1)^{k}X^{n-k}
$$
convient

*Unicité*:

Soit $P_{n}$ un autre polynôme avec $\cos nx = P_{n}\cos x$. On a donc
$$
(P_{n}-T_{n})(\cos x)=0
$$
donc pour tout $x$ dans $\mathbb{R}$, on a $\cos x$ une racine. Or $\cos \mathbb{R}$ est infini, donc $P_{n}-T_{n}=0$.

*Racines*:

On a $\cos nx= 0 \iff nx \equiv \frac{\pi}{2} \text{mod } \pi \iff x \equiv \frac{\pi}{2n} \text{ mod} \frac{\pi}{n}$ donc on a toutes les racines. On a donc

$$
T_{n}=2^{n-1}\prod_{k=0}^{n-1} \left( X-\cos\left( \frac{2k+1}{2n} \right)\pi \right)
$$
