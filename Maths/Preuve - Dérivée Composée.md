---
dg-publish: true
---

$f$ est dérivable en $a$ donc
$$
f(a+h) = f(a)+hf'(a)+o(h)
$$
et $g$ dérivable en $f(a)$ donc
$$
g(f(a)+k)=g(f(a))+kg'(f(a))+o(k)
$$
or
$$
(g\circ  f)(a+h)=g(f(a)+hf'(a)+o(h))
$$
on choisit $k=hf'(a)+o(h) \to 0$

$$
\begin{align}
&= g(f(x))+g'(f(x))(hf'(a)+o(h)) + o(k)  \\
&= g(f(a)) + g'(f(a))f'(a)h + o(h)
\end{align}
$$
tout est ok, on a même l'expression du DL en cadeau :fas_gift:.



