---
dg-publish: true
---

#cours #review 

# $\implies$

Soit $f(t)=\lambda e^{-A(t)}$

$$
\begin{align}
f'(t)&=\lambda(-A(t))'e^{-A(t)} \\
&=-\lambda A'(t)e^{-A(t)} \\
&=-\frac{\lambda b}{a}(t) e^{-A(t)} \\
&= -\frac{b}{a}f(t)
\end{align}
$$
donc $f$ est solution de l'équation homogène

# $\Longleftarrow$

Soit $f$ une solution de l'équation homogène, on définit $\phi$ par
$$
\phi(t) = f(t)e^{A(t)}
$$
$$
\begin{align}
\phi'(t) &= f'(t)e^{A(t)} + f(t)A'(t)e^{A(t)} \\
&= (f'(t)+f(t)A'(t))e^{A(t)} \\
&= \frac{a(t)f'(t)+b(t)f(t)}{a(t)}e^{A(t)} = 0
\end{align}
$$
donc $\phi$ est de dérivée nulle sur $I$ donc une fonction constante sur $I$ donc $\phi(t)=\lambda \in \mathbb{K}$. On en conclut que
$$
f(t)=\lambda e^{-A(t)}
$$
