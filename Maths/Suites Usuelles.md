# Arithmétique

$$
\begin{cases}
u_{0} \in \mathbb{K} \\
u_{n+1} = u_{n} + r
\end{cases}
$$
On a 
$$
u_{n} = u_{0} + nr
$$

et
$$
\sum_{k=0}^{n} k = \frac{n(n+1)}{2} 
$$

# Géométrique

$$
\begin{cases}
u_{0} \in \mathbb{K} \\
u_{n+1}=qu_{n}
\end{cases}
$$
On a
$$
u_{n} = q^{n}u_{0}
$$
et
$$
\sum_{k=0}^{n} q^{k} = \frac{1-q^{n+1}}{1-q}
$$
et
$$
\sum_{k=0}^{n} u_{k} = \frac{u_{0}-u_{n+1}}{1-q}
$$

# Arithmético-Géométrique

$$
\begin{cases}
u_{0} \in \mathbb{K} \\
u_{n+1} = au_{n}+b
\end{cases}
$$

Unique point fixe $\ell$ tel que $\ell = a\ell+b$ et on pose $v_{n}=u_{n}-\ell$.
On a $v$ géométrique de raison $a$ et donc
$$
u_{n}=(u_{0}-\ell)^{n}+\ell
$$

# Suite récurrente linéaire d'ordre $2$

$$
\begin{cases}
u_{0},u_{1}\in \mathbb{K}  \\
u_{n+2}=au_{n+1}+bu_{n}
\end{cases}
$$

On associe à cette suite une équation caractéristique $\alpha^{2}=a\alpha+b$

- Cas avec deux racines distinctes
$$
u_{n} = A\alpha_{1}^{n}+B\alpha_{2}^{n}
$$
- Cas avec une racine double
$$
u_{n}= (An+B)\alpha^{n}
$$

![[Maths/Preuve - Suite récurrente linéaire d'ordre 2]]

