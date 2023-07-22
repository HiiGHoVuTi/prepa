---
dg-publish: true
---

Par l'absurde, supposons que
$$
\exists \varepsilon>0,\forall \eta>0,\exists(x,y)\in [a,b]^{2},\quad \left| x-y \right|\leq \eta \text{ et } \left| f(x)-f(y) \right|\geq \varepsilon
$$
Pour $\eta=\frac{1}{n}$, il existe $x_{n},y_{n}$ convenant.
On extrait de $x_{n}$ une suite $x_{\varphi(n)}$ qui converge car $x_{n}\in [a,b]$ segment.
Par passage à la limite,
$$
\begin{align}
\left| y_{\varphi(n)}-\ell \right|&=\left| y_{\varphi(n)}-x_{\varphi(n)}+x_{\varphi(n)}-\ell \right|\\
&\leq \left| y_{\varphi(n)}-x_{\varphi(n)} \right| + \left| x_{\varphi(n)}-\ell \right| \\
&\leq \frac{1}{\varphi(n)}+\left| x_{\varphi(n)}-\ell \right| \\
& \longrightarrow 0 \\
& ^{n\to +\infty}
\end{align}
$$
Donc $0\geq \varepsilon > 0$ contradictoire.