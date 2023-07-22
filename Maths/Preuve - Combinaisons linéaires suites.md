---
dg-publish: true
---

1. Inégalité triangulaire
$$
\left| u_{n}-\ell_{1} \right| + \lambda \left| v_{n} - \ell_{2} \right| \geq \left| u_{n}-\ell_{1} + \lambda v_{n}- \lambda\ell_{2} \right|
$$
on choisir $\varepsilon_{1}=\frac{\varepsilon}{1+\lambda}$ et $\varepsilon_{2}=\frac{\lambda\varepsilon}{1+\lambda}$

2. Inégalité triangulaire 
$$
\left| u_{n}-\ell_{1} \right| \left| v_{n} \right| + \left| \ell_{1} \right| \left| v_{n} - \ell_{2} \right| \geq \left| u_{n}v_{n} - \ell_{1}\ell_{2} \right|
$$

Donc on a 
$$
\left| u_{n}v_{n} - \ell_{1}\ell_{2} \right| \leq \left| v_{n} \right| \varepsilon_{1} + \left| \ell_{1} \right| \varepsilon_{2}
$$
Or $v$ est bornée (car converge), donc 
$$
\left| u_{n}v_{n} - \ell_{1}\ell_{2} \right| \leq M \varepsilon_{1} + \left| \ell_{1} \right|\varepsilon_{2} 
$$
On prend alors $\varepsilon_{1} = \frac{\varepsilon_{1}}{2M}$ et $\varepsilon_{2} = \frac{\varepsilon}{2(\left| \ell_{1} \right|+1)}$

3. On suppose $\ell_{2} > 0$ spg
$$
\left| \frac{1}{v_{n}} - \frac{1}{\ell_{2}} \right| = \left| \frac{\ell_{2} - v_{n}}{\ell_{2}v_{n}} \right| = \frac{\left| v_{n}-\ell_{2} \right|}{\left| \ell_{2}v_{n} \right|}
$$
On sait qu'il existe un rang tel que $v_{N}\geq \frac{\ell_{2}}{2}>0$, d'où $\frac{1}{v_{n}} \leq \frac{2}{\ell_{2}}$
donc,
$$
\left| \frac{1}{v_{n}} - \frac{1}{\ell_{2}} \right| \leq \frac{2}{\ell_{2}^{2}} \left| v_{n}-\ell_{2} \right| \leq \frac{2}{\ell_{2}^{2}} \varepsilon_{2}
$$
on choisit alors $\varepsilon_{2} = \frac{\varepsilon \ell_{1}^{2}}{2}$ ok