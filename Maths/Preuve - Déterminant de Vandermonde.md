---
dg-publish: true
---

*Initialisation* Pour $n=1$, $\Delta_{1}=\det (1)=1=\prod_{i,j\in \emptyset} a_{j}-a_{i}$
*Hérédité*
On raisonne sur les colonnes et on fait $C_{n+1}\leftarrow C_{n+1}+\sum_{i=1}^{n} \lambda_{k}C_{k}$
La dernière colonne est alors $P(x_{i})$ avec $P=X^{n}+\sum_{i=1}^{n} \lambda_{k}X^{k-1}$.
Alors, avec $P=\prod_{i=1}^{n} X-a_{i}$ bien choisi
$$
\begin{align}
\Delta_{n+1}&=\det \begin{pmatrix}
1 & a_{1} & \dots & a^{n-1}_{1} & P(a_{1})\\
\vdots & && & \vdots \\
1 & a_{n+1} & \dots & a^{n-1}_{n+1}&P(a_{n+1})
\end{pmatrix} \\
&= \Delta_{n}P(a_{n+1}) \\
&= \prod_{1\leq i<j\leq n+1} a_{j}-a_{i}
\end{align}
$$

