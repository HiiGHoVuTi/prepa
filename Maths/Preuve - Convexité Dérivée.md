---
dg-publish: true
---

# $\implies$

Prenons $x<t<y$, on a 
$$
\frac{f(t)-f(x)}{t-x}\leq \frac{f(y)-f(x)}{y-x}\leq \frac{f(y)-f(t)}{y-t}
$$
En passant à la limite $t\to x^{+}$, on obtient
$$
f'(x)\leq \frac{f(y)-f(x)}{y-x}
$$
En passant à la limite $t\to y^{-}$, on obtient
$$
f'(y)\geq \frac{f(y)-f(x)}{y-x}
$$
Donc $f'(y)> f'(x)$ ok

# $\impliedby$

Fixons $x<y\in I$, montrons pour tout $\lambda\in[0,1]$ que
$$
f(\lambda x+(1-\lambda)y)\leq \lambda f(x)+(1-\lambda)f(y)
$$

On définit $\varphi(x)=f(\lambda x+(1-\lambda)y)-\lambda f(x)-(1-\lambda)f(y)$,
On a
$$
\varphi'(x)=\lambda f'(\lambda x+(1-\lambda)y)-\lambda f'(x)=\lambda(f'(\lambda x+(1-\lambda)y)-f'(x))
$$

Si $x\leq y$ alors $\lambda x(1-\lambda)y \geq x$ donc $f'(\lambda x+(1-\lambda)y)\geq f'(x)$

Sinon, on a $\varphi(x)\leq 0$ donc ok.