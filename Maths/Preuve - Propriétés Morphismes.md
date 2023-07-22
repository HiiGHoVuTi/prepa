---
dg-publish: true
---

1. $$
\begin{align}
e_{G}&= e_{G} \cdot e_{G} \\
f(e_{G}) &= f(e_{G} \cdot e_{G}) \\
f(e_{G}) &= f(e_{G}) * f(e_{G}) \\
f(e_{G}) * (f(e_{G}))^{-1} &= f(e_{G}) * (f(e_{G}) * (f(e_{G}))^{-1})
\end{align}
$$
2. $$
\begin{align}
e_{G} &= x \cdot x^{-1} \\
f(e_{G}) &= f(x) * f(x^{-1}) \\
(f(x))^{-1} &= f(x^{-1})
\end{align}
$$
3. Inclusion ok par définition, non-vide car $e_{G} \in H$ donc $f(e_{G}) \in f(H)$, stabilité par produit et par l'inverse:
Par la définition de l'image directe, $y_{1},y_{2} \in f(H)$ donc il existe $x_{1}, x_{2}$ antécédents, 
$$
f(x_{1}) * f(x_{2}) = f(x_{1} \cdot x_{2})
$$
Inverse par propriété $2.$ démontrée ci-dessus.
4. Inclusion ok par définition, non-vide car $e_{G} \in f^{-1}(H)$, stabilité par produit et par l'inverse:
$$
f(x_{1} \cdot x_{2}) = f(x_{1}) * f(x_{2}) \in H
$$
donc $x_{1} \cdot x_{2} \in f^{-1}(H)$ par définition de l'image réciproque
Inverse par propriété $2.$ démontrée ci-dessus.
