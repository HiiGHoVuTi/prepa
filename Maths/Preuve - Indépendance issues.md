---
dg-publish: true
---

$$
\begin{align}
P((X\in A)\cap(X\in B)) &=P\left(\left(\bigcup X=x_{i}\right)\cap\left(\bigcup Y=y_{i}\right)\right) \\
&=P\left(\bigcup_{i,j}(X=x_{i})\cap(Y=y_j)\right) \\
&=\sum_{i,j} P((X=x_{i})\cap(X=y_{j})) \\
&= \sum_{i,j} P(X=x_{i})P(Y=y_{j}) \\
&= \left( \sum_{i} P(X=x_{i}) \right)\times\left( \sum_{j}P(Y=y_{i}) \right) \\
&= P(X\in A)P(X\in B)
\end{align}
$$
