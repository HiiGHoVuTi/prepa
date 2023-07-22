---
dg-publish: true
---

# $\ell\in \mathbb{R}$

On revient à la définition de la dérivée en traîtant SPG le cas $x>c$
$$
\frac{f(x)-f(c)}{x-c}
$$
Or $f$ est continue sur $[c,x]$ et dérivable sur $[c,x[$ donc il existe par le [[Preuve - Accroissements Finis|théorème d'accroissements finis]] un $\mathfrak{x}\in ]c,x[$ tel que
$$
\frac{f(x)-f(c)}{x-c}=f'(\mathfrak{x})
$$
comme $c<\mathfrak{x}<x$, on peut utilise rle théorème des gendarmes
$$
\mathfrak{\mathfrak{x}}\xrightarrow[x \to c]{} c
$$
par compositions de limites, on a
$$
\frac{f(x)-f(x)}{x-c} =f(\mathfrak{x})\xrightarrow[x \to c]{} \ell
$$

# $\ell \not \in \mathbb{R}$

La limite du taux d'accroissement est donc infinie, c'est-à-dire que la fonction est non-dérivable en $c$, et la courbe admet une pente "infinie", soit verticale.