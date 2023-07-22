---
dg-publish: true
---

# Négligeabilité

Soit $x\in I\setminus \{ a \}$, il existe alors $\mathfrak{x}$ par le [[Preuve - Accroissements Finis|TAF]] que
$$
\frac{f(x)-f(a)}{x-a}=f'(\mathfrak{x})
$$
d'où
$$
f(x)-f(a)=(x-a)f'(\mathfrak{x})
$$
On traite SPG le cas $x > a$, on a donc
$$
a < \mathfrak{x}< x
$$
par le [[Preuve - Théorème des Gendarmes (fonctions)|théorème des gendarmes]], 
$$
\mathfrak{x} \xrightarrow[x \to a]{} a
$$

Or $f'(x)=(x-a)^{n}\varepsilon(x)$ avec $\varepsilon(x)\xrightarrow[x \to a]{}0$, donc $\varepsilon(\mathfrak{x})\to 0$
ainsi on a
$$
\begin{align}
f(x)-f(a) &= (x-a)(\mathfrak{x}-a)^{n}\varepsilon(\mathfrak{x}) \\
&= (x-a)^{n+1}\left( \frac{\mathfrak{x}-a}{x-a} \varepsilon(\mathfrak{x}) \right)
\end{align} 
$$

or on a bien $0 < \frac{\mathfrak{x}-a}{x-a}<1$ donc ok.

# Primitive

On considère $g$ définie sur $I$ par $g=f(x)-f(a)-\sum \alpha_{k} \frac{(x-a)^{k+1}}{k+1}$.
Par les règles usuelles, on a:
$$
g'(x)= f'(x)-\sum \alpha _{k}(x-a)^{k} = o((x-a)^{n})
$$
ainsi on a
$$
g(x)-g(a) = o((x-a)^{n+1})
$$
or $g(a)=0$
$$
g(x) = f(x)-f(a) - \sum\alpha_{k} \frac{(x-a)^{k}}{k+1} = o((x-a)^{n+1})
$$
ok