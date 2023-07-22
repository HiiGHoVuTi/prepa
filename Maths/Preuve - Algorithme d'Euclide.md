---
dg-publish: true
---

Cela revient à démontrer:
$$
a\mathbb{Z} + b\mathbb{Z} = (a-bq)\mathbb{Z} + b\mathbb{Z}
$$

>[!Warning]- On ne peut pas simplifier !
>Ici $+ : \mathcal{P}(G)^{2} \to \mathcal{P}(G)$ est une LCI non-inversible

# $\subset$

On utilise une [[Formules de Bel|formule de Bel]].

Soit $x\in a\mathbb{Z} + b\mathbb{Z}$ 
Il existe $k,\ell$ tels que 
$$
\begin{align}
x &= ka+\ell b \\
&= k(a-bq)+kbq+\ell b \\
&= k(a-bq)+(kq+\ell)b \\
&\in \mathbb{Z}(a-bq)+\mathbb{Z}b
\end{align}
$$

# $\supset$

Soit $x \in \mathbb{Z}(a-bq)+\mathbb{Z}b$
Il existe $k,\ell$ tel que
$$
\begin{align}
x &=k(a-bq)+\ell b \\
&= ka+(\ell-qk)b \\
&\in a\mathbb{Z}+b\mathbb{Z} 
\end{align}
$$
