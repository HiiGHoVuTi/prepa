---
dg-publish: true
---

# $\implies$

Supposons qu'il existe $f'(0)=\alpha$, on  a donc
$$
\frac{f(x)-f(0)}{x} \xrightarrow[x \to 0]{} \alpha
$$
soit
$$
\frac{f(x)-f(0)}{x} - \alpha = \epsilon(x)
$$
avec
$$
\epsilon(x) \xrightarrow[x \to 0]{} 0
$$
d'où
$$
f(x) - f(0) = \alpha x+x\epsilon(x)
$$

d'où
$$
f(x) = f(0) + \alpha x + o(x)
$$

# $\impliedby$

Supposons $\alpha,\beta \in \mathbb{R}$ avec $f(x)=\alpha +\beta x+o(x)$, on a donc
$$
f(x) = \alpha x+\beta x+x\epsilon(x)
$$
avec
$$
\epsilon(x) \xrightarrow[x \to 0]{} 0
$$
on a donc
$$
f(x)-\alpha=\beta x-x\epsilon (x) \xrightarrow[x \to 0]{}0 
$$
alors
$$
\frac{f(x)-f(0)}{x} = \frac{\alpha-\beta x+x\epsilon(x)-f(0)}{x} = \frac{\beta x+x\epsilon(x)}{x} \xrightarrow[x \to 0]{} \beta
$$
