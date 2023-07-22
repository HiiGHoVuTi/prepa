---
dg-publish: true
---

# Initialisation

$\alpha_{1}=1, \beta_{1}=-q_{0}$

# Hérédité

Supposons avoir $\alpha_{n}a+\beta_{n}b=b_{n}$
Si $n=n_{0}$, on a terminé.
Sinon on fait la division euclidienne:
$$
a_{n}=b_{n}q_{n}+r_{n}
$$
avec 
$$
\begin{align}
b_{n+1}&=a_{n}-b_{n}q_{n}=a_{n}-(\alpha _{n}a+\beta_{n}b)q_{n} \\
&=b_{n-1}-(\alpha_{n}a+\beta_{n}b)q_{n} \\
&= (\alpha_{n-1}-\alpha _{n}q_{n})a + (\beta_{n-1}-q_{n}\beta_{n})b \\
&= \alpha_{n+1}a + \beta_{n+1}b
\end{align}
$$
