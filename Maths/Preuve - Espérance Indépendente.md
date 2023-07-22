---
dg-publish: true
---

$$
\begin{align}
E(XY)&=\sum_{\omega} X(\omega)Y(\omega)P(\{ \omega \}) \\
&= \sum_{i}\sum_{j} \sum_{\omega\in (X=x_{i})\cap(Y=y_{j})} X(\omega)Y(\omega)P(\{  \omega \}) \\
&=\sum_{i}\sum_{k} x_{i}y_{j} \sum_{\omega\in(X=x_{i})\cap(Y=y_{j})} P(\{  \omega \}) \\
&= \sum_{i}\sum_{k} x_{i}y_{j}P((X=x_{i})\cap(Y=y_{j})) \\
&=\sum_{i}\sum_{k} x_{i}y_{j}P(X=x_{i})P(Y=y_{j}) \\
&= \left( \sum_{i}x_{i}P(X=x_{i}) \right)\times\left( \sum_{j}y_{j}P(Y=y_{j}) \right) \\
&= E(X)E(Y)
\end{align}
$$