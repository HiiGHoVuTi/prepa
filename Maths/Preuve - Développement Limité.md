---
dg-publish: true
---

# $1. \implies 2.$

On suppose $f$ dérivable donc
$$
\frac{f(x)-f(a)}{x-a}\to f'(a)
$$
donc
$$
\frac{f(x)-f(a)}{x-a} = f'(a)+\varepsilon(x) ,\quad \varepsilon(x)\to 0
$$

On manipule l'égalité et obtient
$$
f(x)=f(a)+f'(a)(x-a)+\varepsilon(x)(x-a)
$$

# $2. \implies 1.$

On a 
$$
f(x)-\alpha = \beta(x-a) + o(x-a)
$$
comme $f$ est définie en $a$ et le membre de droite admet une limite (donc de gauche aussi) en $a$, on obtient $\alpha=f(a)$

Donc
$$
\frac{f(x)-f(a)}{x-a}=\beta + \varepsilon(x)
$$
De même, le membre de droite admet une limite donc celui de gauche aussi, donc $f$ est dérivable.