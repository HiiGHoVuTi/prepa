---
dg-publish: true
---

Raisonnons par récurrence sur $\mathbb{N}$.

# Initialisation

Pour $n=1$, $f$ dérivable en $a$ donc $f(x)=f(a)+f'(a)(x-a)+o(x-a)$
[[Preuve - Développement Limité]]

# Hérédité

Supposons la propriété vraie au rang $\mathbb{N}$.
Considérons $g$ une fonction $n+1$-fois dérivable, on a donc $g'$ $n-$fois dérivable.
Par HR,
$$
g'(x)= \sum_{k=0}^{n} g'^{(k)}(a) \frac{(x-a)^{k}}{k!}
$$
Par le [[Preuve - Primitive de DL|corollaire précédent]], on a
$$
g(x) = g(a)+\sum_{k=0}^{n} g^{(k+1)}(a) \frac{(x-a)^{k+1}}{(k+1)!} + o((x-a)^{n+1})
$$
ok