---
dg-publish: true
---

Preuve par récurrence sur $n$

# Initialisation

Pour $n< 2$ on vérifie à la main et à coups de lemme.

# Hérédité

Si $(\lambda_{i})_{i\neq n+1}=(0)$, on est bon.

Sinon, on a $\sum\lambda_{k}>0$.
Donc on a 
$$
\begin{align}
\frac{\sum_{k=1}^{n+1}\lambda_{k}x_{k}}{\sum\lambda_{k}} &= \frac{\left(\sum^{n}_{k=1} \lambda_{k}x_{k}\right) + \lambda_{n+1}x_{n+1}}{\lambda_{n+1}+\sum_{k=0}^{n}\lambda_{k}} \\
&= \frac{\left( \sum \lambda_{k} \right)\left( \frac{\left( \sum\lambda_{k}x_{k} \right)}{\sum\lambda_{k}} \right)+\lambda _{n+1}x_{n+1}}{\sum\lambda_{k}+\lambda_{n+1}}
\end{align}
$$

Comme la propriété est vraie au rang $2$, on a fini