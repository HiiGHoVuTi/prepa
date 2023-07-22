---
dg-publish: true
---

Supposons que la suite admette deux limites $\ell$ et $l$ avec $\ell<l$ spg.
On a pout tout $\varepsilon$ il existe des rangs $N_{1},N_{2}$ tels que 
$$
\forall n \geq max(N_{1},N_{2}),\quad\left| u_{n} -\ell \right| < \varepsilon \land \left| u_{n} - l \right| < \varepsilon
$$

Prenons $\varepsilon = \frac{\ell - l}{3}$, on a 
$$
[\ell -\varepsilon, \ell+\varepsilon] \cap [l -\varepsilon, l+\varepsilon] = \emptyset
$$
donc impossible

> $\left| \ell-l \right| = \left| \ell-u_{n} + u_{n} - l \right| \leq \left| \ell-u_{n} \right| + \left| u_{n}-l \right| \leq \frac{2}{3} \left| \ell -l \right|$
> absurde pour ce choix de $\varepsilon$

