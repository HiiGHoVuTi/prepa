---
dg-publish: true
---


On raisonne par double inclusion.

# $\subset$

Soit $y_{1} \in S$. On a donc

$$
\begin{cases}
a(t)y_{1}'(t) + b(t)y_{1}(t) = c(t) \\
a(t)y_{0}'(t) + b(t)y_{0}(t) = c(t) \\
\end{cases}
$$
Par soustraction
$$
a(t)(y_{0}'(t)-y'_{1}(t))+b(t)(y_{0}-y_{1})b(t) = 0
$$
donc $y_{1}-y_{0} \in S_{H}$
$$
y_{1}=y_0+(y_1-y_0) ∈ \{ y_0 + y_h  ;  y_h ∈ S_h \}
$$

# $\supset$

Soit $f\in \{ y_{0}+y_{h} \;;\; y_{h} \in S_{h} \}$ donc il existe $g\in S_{h}$  tel que $f = y_{0}+g$
On a alors
$$
\begin{align}
f'(t) &= y_{0}'(t) + g'(t) \\
a(t)y'_{0}+f(t)y_{0}(t) &+ a(t)g'(t)+b(t)g(t) = c(t)
\end{align}
$$
ok !