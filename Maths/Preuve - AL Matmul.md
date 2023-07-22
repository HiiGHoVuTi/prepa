---
dg-publish: true
---

Soient $X,M,Y$ les trois matrices d'intérêt. Montrons que $Y=MX$.
On a:
$$
\begin{align}
f(x)&=\sum_{k} x_{k}f(e_{k}) \\
&=\sum_{k} x_{k} \left( \sum_{i} m_{ik}f_{i} \right) \\
&= \sum_{i} \sum_{k} x_{k}m_{ik}f_{i} \\
&= \sum_{i} f_{i} \left( \sum_{k} m_{ik}x_{k} \right) \\
&= \sum_{i} (MX)_{i}f_{i}
\end{align}
$$
Par unicité de la décomposition, on a bien $y_{i}=(MX)_{i}$ donc $Y=MX$.