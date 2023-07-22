---
dg-publish: true
---

# Initialisation

Pour $n=1$, ok.
Pour $n=2$, par définition de la convexité.

# Hérédité

Pour $n\geq 2$, par le lemme précédent, on a
$$
\sum\lambda_{k}x_{k}\in I
$$

Si $\lambda_{n+1}=1$, on est ok
Sinon, on a $\sum_{k=1}^{n} \lambda_{k}=1-\lambda_{n+1}$ donc
$$
f\left( \sum \lambda_{k}x_{k} \right)=f\left( \lambda_{n+1}x_{n+1}+(1-\lambda_{n+1})\left( \frac{\sum_{k=1}^{n}\lambda _{k}x_{k}}{\sum_{k=1}^{n}\lambda_{k}} \right) \right)
$$
La propriété étant vrait au rang $2$ et au rang $n$, ok.