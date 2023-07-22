---
dg-publish: true
---


Soit $\varepsilon> 0$, on cherche $\left| v_{n}-\ell \right|\leq\varepsilon$.
Il existe $N$ tel que si $n>N$, $u_{n} \leq v_{n} \leq w_{n}$.
Il existe $M$ tel que pour $n>M$, $\ell-\varepsilon \leq u_{n}$
Il existe $P$ tel que pour $n>P$, $\ell+\varepsilon \geq w_{n}$

Alors pour $n > \text{max}\{ M, N, P \}$, on a:
$$
\begin{align}
\ell-\varepsilon \leq &v_{n} \quad\;\,\leq \ell+\varepsilon  \\
-\varepsilon \leq &v_{n}-\ell\leq \varepsilon
\end{align}
$$
