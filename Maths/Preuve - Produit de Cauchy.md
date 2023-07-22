---
dg-publish: true
---

*Convergence*

$$
\begin{align}
\sum \left| c_{k} \right|&= \sum \left| \sum u_{k}v_{n-k} \right| \\
&\leq \sum \sum \left| u_{k}v_{n-k} \right| \\
&= \sum_{i,j\in \textlbrackdbl 0,n \textrbrackdbl ,i+j \leq n} \left| u_{i}v_{j} \right| \\
&\leq \sum_{i,j\in  \textlbrackdbl 0,n \textrbrackdbl } \left| u_{i}v_{j} \right|  \\
&= \left( \sum \left| u_{i} \right| \right) \left( \sum \left| v_{j} \right| \right) \\
\end{align}
$$

Les sommes partielles absolues sont majorées donc la série converge absolument.

*Limite*

Considérons $S_{2n}$,
$$
\begin{align}
S_{2n}&= \sum_{i+j=2n} u_{i}v_{j} \\
&= \sum_{i,j\leq n} u_{i}v_{j} + \sum_{i>n,j\leq n, i+j \leq 2n} u_{i}v_{j} + \sum_{i>n, j\leq n,i+j\leq 2n}u_{i}v_{j}
\end{align}
$$
Montrons que les termes additionnels tendent vers $0$.
$$
\begin{align}
\left| \sum_{i>n,j\leq n,i+j\leq 2n} u_{i}v_{j} \right| &\leq \sum_{i>n,j\leq n, i+j \leq 2n} \left| u_{i}v_{j} \right| \\
&\leq \sum^{2n}_{i=n+1} \left| u_{i} \right| \times\sum_{j=0}^{n} \left| v_{j} \right| \\
&\leq \sum_{i=n+1}^{2n} \left| u_{i} \right| \times \sum^{\infty} \left| v_{j} \right| \\
&\leq \left( \sum^{\infty}\left| v_{j} \right| \right)\times \sum_{i=n+1}^{\infty} \left| u_{j} \right| \\
& \quad \quad\in \mathbb{R} \quad\quad\quad \xrightarrow[n \to +\infty]{} 0
\end{align}
$$
