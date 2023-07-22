---
dg-publish: true
aliases: [TAF]
---

On construit la fonction auxiliaire $g$ définie par:
$$
g(x)= f(x)-\left( \frac{f((b)-f(a))}{b-a}(x-a)+f(a) \right)
$$

On a donc $g(a) = g(b) = 0$
On applique alors le [[Preuve - Théorème de Rolle|Théorème de Rolle]] pour obtenir qu'il existe $c\in ]a,b[$ tel que $g'(c)=0$ or on a $g'(c) = f'(c)-\frac{f(b)-f(a)}{b-a}$

Ainsi on obtient l'égalité escomptée.