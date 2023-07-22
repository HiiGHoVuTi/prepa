---
dg-publish: true
---

On montrera la limite à gauche, il en va de même pour la limite à droite.
Comme $a$ n'est pas borne, on a $a_{1}<a$ avec $a_{1}\in I$.
Soit $x\in ]a_{1},a[$, comme $a_{1}<x<a$ on a
$$
\frac{f(x)-f(a)}{x-a}\leq \frac{f(a)-f(a_{1})}{a-a_{1}}\leq \frac{f(x)-f(a_{1})}{x-a_{1}}
$$
On a donc
$$
\frac{f(a)-f(a_{1})}{a-a_{1}}(a-x)\leq f(a)-f(x)
$$
De la même manière, comme $a$ n'est pas une borne, on a $a<a_{2}$ avec $a_{2}\in I$.
Donc comme $x<a<a_{2}$
$$
\frac{f(a)-f(x)}{a-x}\leq \frac{f(a)-f(a_{2})}{a-a_{2}}\leq \dots
$$
Donc
$$
f(a)-f(x)\leq \frac{f(a_{2})-f(a)}{a_{2}-a}
$$
On fait tendre $x$ vers $a$, on a $f(a)-f(x)\to 0$


