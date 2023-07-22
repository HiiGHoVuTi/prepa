---
dg-publish: true
---

$f$ continue et $F$ une primitive de $f$ sur $I$.
On a donc
$$
\int  ^{\phi(b)}_{\phi(a)}f(x) \, dx = F(\phi(b)) - F(\phi(a)) 
$$

On remarque
$$
F(\phi(t))' = f(\phi(t))\phi'(t)
$$
donc $F \circ\phi$ est une primitive de $(f\circ\phi) \times \phi'$
On a alors
$$
\int _{a}^{b} f(\phi(t))\phi'(t) \, dt = F(\phi(b)) - F(\phi(a)) 
$$

Les deux membres sont égaux, ok !