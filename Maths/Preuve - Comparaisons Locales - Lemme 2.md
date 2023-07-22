---
dg-publish: true
---


![[Maths/Logique - équivalence de plusieurs propriétés]]


# $1. \implies 2.$

On suppose $f(x) \sim g(x)$, on définit $a=\frac{f}{g}$ et on a bien $a \xrightarrow[x \to c]{} 1$

# $2. \implies 3.$

On a $f = a g$ donc on a 
$$
\frac{f(x)-g(x)}{g(x)} = \frac{a(x)g(x)-g(x)}{g(x)} = a(x) - 1 \xrightarrow[x \to c]{} 0
$$
Donc $f(x)-g(x) = o_{x\to c}(g(x))$

# $3. \implies 1.$

Grâce aux magnifiques [[Maths/Formules de Bel|formules de Bel]], on a
$$
\frac{f(x)}{g(x)} = \frac{f(x) - g(x) + g(x)}{g(x)} = 1+\frac{f(x)-g(x)}{g(x)}
$$
or grâce à $2.$, ça tend vers $1$ donc $f \sim g$
