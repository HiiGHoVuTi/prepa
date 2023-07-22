---
dg-publish: true
---

# Unicité

Supposons:
$$
\begin{cases}
L_{1}: a = bq_{1}+r_{1} \\
L_{2}: a=bq_{2} +r_{2}
\end{cases}
$$
En considérant la soustration $L_{1}-L_{2}$, on a:
$$
b\mid r_{2}-r_{1}
$$
donc
$$
\left| b \right|\leq \left| r_{2} -r_{1} \right|
$$

Or on a:
$$
\left| r_{2} -r_{1}\right| \leq \left| b \right|-1
$$

absurde :luc_zap:

# Existance

> uniquement le cas $b>0$

Si $0\leq a < b$, finito 🕺
Sinon, 
$$
a = b + a - b
$$
avec $0 \leq a_{1} =a - b < a$

On itère ainsi, on a
$$
a = q_{n}b + a_{n}
$$
avec $q_{n+1} = q_{n}+1$ et $a_{n+1}=a_{n}-b$

Fini par variant de boucle $(a_{n})$ décroissant dans les entiers. 
