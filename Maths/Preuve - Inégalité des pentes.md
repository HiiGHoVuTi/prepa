---
dg-publish: true
---

Il existe $\lambda \in [0,1]$ avec $x_{2}=\lambda x_{3}+(1-y)x_{1}$, on a $\lambda=\frac{x_{2}-x_{1}}{x_{3}-x_{1}}$.
Par inégalité de convexité, on a
$$
f(x_{2})\leq \lambda f(x_{3})+(1-\lambda)f(x_{1})
$$
Donc
$$
f(x_{2})\leq \frac{x_{2}-x_{1}}{x_{3}-x_{1}}f(x_{3})+\left( 1-\frac{x_{2}-x_{1}}{x_{3}-x_{1}} \right)f(x_{1})
$$
Pour l'inégalité de gauche, 
$$
f(x_{2})-f(x_{1})\leq \frac{x_{2}-x_{1}}{x_{3}-x_{1}}f(x_{3})-\frac{x_{2}-x_{1}}{x_{3}-x_{1}}(f(x_{3})-f(x_{1}))
$$
Donc
$$
\frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}\leq \frac{f(x_{3})-f(x_{1})}{x_{3}-x_{1}}
$$
Pour l'inégalité de droite,
$$
0\leq \frac{x_{2}-x_{1}}{x_{3}-x_{1}}f(x_{3})+\frac{x_{3}-x_{2}}{x_{3}-x_{1}}f(x_{1})-f(x_{2})
$$
d'où
$$
f(x_{3})\leq \frac{x_{2}-x_{1}}{x_{3}-x_{1}}f(x_{3})+\frac{x_{3}-x_{2}}{x_{3}-x_{1}}f(x_{1})+f(x_{3})-f(x_{2})
$$
donc
$$
\frac{x_{3}-x_{2}}{x_{3}-x_{1}}f(x_{3})-\frac{x_{3}-x_{2}}{x_{3}-x_{1}}f(x_{1})\leq f(x_{3})-f(x_{2})
$$
donc 
$$
\frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}\leq \frac{f(x_{3})-f(x_{2})}{x_{3}-x_{2}}
$$