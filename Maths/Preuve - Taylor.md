---
dg-publish: true
---

On introduit
$$
\varphi(P)=\sum P^{(k)}(a) \frac{X-a}{k!}
$$

Montrons que $\varphi$ est linéaire
$$
\begin{align}
\varphi(P+\lambda Q) &= \dots = \varphi(P)+\lambda\varphi(Q)
\end{align}
$$
On peut alors étudier un monôme.
Montrons que $\varphi=\text{id}$
$$
P_{k}^{(\ell)} = \frac{k!}{(k-\ell)!}X^{(k-\ell)} 
$$
donc
$$
\begin{align}
\varphi(X^{k})&=\sum_{k=0}^{+\infty} (P_{k})^{(k)}(a) \frac{(X-a)^{\ell}}{\ell!} \\
&= \sum_{\ell=0}^{k} \frac{k!}{(k-\ell)!}a^{k-\ell} \frac{(X-a)^{\ell}}{\ell!} \\
&=\sum^{k}_{\ell=0} {k\choose \ell} a^{k-\ell}(X-a)^{\ell} \\
&=(a+X-a)^{k} \\
&=X^{k}
\end{align}
$$
donc $\varphi$ est l'identité.
