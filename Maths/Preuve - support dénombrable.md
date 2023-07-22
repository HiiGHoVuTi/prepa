---
dg-publish: true
---

Si le support est fini, ok
Si le support est infini, on considère $A_{n}=\left\{  i \;;\; i\in I, u_{i}\geq \frac{1}{n}   \right\}$ un ensemble fini.
On construit $B_{n}=A_{n+1}\setminus A_{n}$.
Par construction les ensembles $B_{n}$ sont disjoints, comme $B_{n}\subset A_{n+1}$, $B_{n}$ est fini.
Alors le support est
$$
\begin{align}
\mathfrak{S}&=\bigcup_{k=1}^{+\infty} A_{k} \\
&=A_{1} + \bigcup^{+\infty}_{k=1} B_{k}
\end{align}
$$
Avec une union disjointe, on peut alors créer une surjection depuis $\mathbb{N}$.