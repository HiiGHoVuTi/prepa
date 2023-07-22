---
dg-publish: true
---

On suppose:
$f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n} + o(x^{n}) = b_0+b_{1}x+\dots+b_{n}x^{n} + o(x^{n})$


Il existe donc $\epsilon_{1},\epsilon_{2}$ des fonction de limite nulle au voisinage de $0$ telle que:

$$
\begin{cases}
L_{1}&: f(x)=a_{0}+a_{1}+\dots+a_{n}x^{n}+\epsilon_{1}(x)x^{n} \\
L_{2}&: f(x)=b_{0}+b_{1}+\dots +a_{n}x^{n}+\epsilon_{2}(x)x^{n}
\end{cases}
$$

On a donc $L_{1}-L_{2}=0$.

Soit $A$ un ensemble tel que
$$
A = \{ i ; \;i\in [0,n]\cap \mathbb{N}, \;a_{i-b_{i}} \neq 0 \}
$$

Supposons $A\neq \emptyset$. Soit $j=\text{min}A$
On divise notre expression par $x^{j}$, et obtient une fonction qui tend vers $a_{j}-b_{j} \neq 0$, on a donc une contradiction.