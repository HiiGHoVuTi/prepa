---
dg-publish: true
---

$\implies$

Soit $x=\frac{p}{q}$ avec $p\land q=1$
Il n'y a que $q$ éléments dans l'intervalle $\textlbrackdbl 0,q-1 \textrbrackdbl$ donc les restes des divisions euclidiennes successives doivent boucler.

$\impliedby$

Supposons $(x_{n})$ ultimement périodique. Alors il existe $N_{0}$ tel que $n\geq N_{0}\implies x_{n}=x_{n+\mathfrak{T}}$.
$$
\begin{align}
x&= \sum^{+\infty} 10^{-k}x_{k} \\
&= \sum_{k=1}^{N_{0}-1} 10^{-k}x_{k} + \sum_{k=N_{0}}^{+\infty} 10^{-k}x_{k} \\
&= \sum_{k=1}^{N_{0}+\mathfrak{T}-1} 10^{-k}x_{k}+\sum_{k=n_{0}+\mathfrak{T}}^{+\infty} 10^{-k}x_{k-\mathfrak{T}} \\
10^{\mathfrak{T}}x&= 10^{\mathfrak{T}} \sum_{k=1}^{N_{0}+\mathfrak{T}-1} 10^{-k}x_{k} + \sum_{k=N_{0}}^{+\infty} 10^{-k}x_{k} \\
10^{\mathfrak{T}}x-x&= 10^{\mathfrak{T}}\sum^{N_{0}+\mathfrak{T}-1}_{k=1} 10^{-k}x_{k}-\sum^{N_{0}-1}_{k=1} 10^{-k}x_{k} \\
x(10^{\mathfrak{T}}-1)&\in\mathbb{Q}  \\
x &\in \mathbb{Q}
\end{align}
$$

