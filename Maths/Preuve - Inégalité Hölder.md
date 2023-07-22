---
dg-publish: true
---

# Lemme

$$
\ln(xy)\leq \ln\left( \frac{1}{p}x^{p}+\frac{1}{q}y^{q} \right)
$$

Vrai car concavité de $\ln$.
On a $\ln\left( \frac{1}{p}x^{p}+\frac{1}{q}y^{q} \right)\geq \frac{1}{p}\ln(x^{p})+\frac{1}{q}\ln(x^{q})$

# Preuve

Grâce au lemme on a $xy\leq \frac{1}{p}x^{p}+ \frac{1}{q}y^{q}$
On prend 
$$
\begin{cases}
x = \frac{x_{k}}{\left( \sum x_{i}^{p} \right)^{1/p}} \\
y = \frac{y_{k}}{\left( \sum y_{i}^{q} \right)^{1/q}}
\end{cases}
$$

L'inégalité donne alors
$$
\frac{x_{k}y_{k}}{\left( \sum x_{i}^{p} \right)^{1/p}\left( \sum y_{i}^{q} \right)^{1/q}}\leq \frac{1}{p} \frac{x_{k}}{\sum x_{i}^{p}}+\frac{1}{q} \frac{x_{k}}{\sum x_{i}^{q}}
$$

Et en faisant la somme sur $k$, on a fini