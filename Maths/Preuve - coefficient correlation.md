---
dg-publish: true
---


$$
\begin{align}
\text{cov}(X,Y)&=E((X-E(X))(Y-E(Y))) \\
&=\sum_{\omega} (X(\omega)-E(X))(Y(\omega)-E(Y))P(\{ \omega \})
\end{align}
$$

On pose $x_{k}=(X(\omega)-E(X))\sqrt{ P(\{ \omega \}) }$, idem pour $Y$
On utilise l'inégalité de [[Maths/Cauchy - Schwartz|Cauchy-Schwartz]],
$$
\text{cov}(X,Y)^{2}= \sum_{k} x_{k}y_{k}\leq V(X)V(Y)
$$
donc
$$
0\leq \frac{\text{cov}(X,Y)^{2}}{V(X)V(Y)}\leq 1
$$
et ainsi
$$
-1 \leq \frac{\text{cov}(X,Y)}{\sigma(X)\sigma(Y)}\leq 1
$$

