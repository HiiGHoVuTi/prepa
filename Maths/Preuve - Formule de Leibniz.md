---
dg-publish: true
---

On montrera le cas $f,g\in \mathcal{C}^{n}$ par récurrence sur $\mathbb{N}$

# Initialisation

Pour $n=1$, on a bien $(fg)' = f'g + fg'$

# Hérédité 

> On montre la régularité des objets


On a
$$
\begin{align}
(fg)^{(n+1)} &= f^{(n)}g^{(n+1)}+ f^{(n+1)}g^{(n)} \\
&= \sum_{k=0}^{n} {n\choose k}f^{(k+1)}g^{(n-k)} + \sum_{k=0}^{n}{n\choose k}f^{(k)}g^{(n+1-k)} \\
&= \sum_{k=1}^{n+1} {n\choose k-1} f^{(k)}g^{(n+1-k)} + \sum{n\choose k}f^{(k)}f^{(n+1-k)} \\
&= f^{n+1}g + \sum_{k=1}^{n} {n\choose k}f^{(k)}g^{(n+1-k)} + fg^{(n+1)} \\
&= \sum_{k=0}^{n+1} {n\choose k}f^{(k)}g^{(n+1-k)} 
\end{align}
$$


