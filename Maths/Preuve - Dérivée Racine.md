---
dg-publish: true
---

# $\implies$

On a $P=(X-\alpha)^{n}Q$ et $Q(\alpha)\neq 0$
On dérive $k$ fois
$$
P^{(k)}=((Q-\alpha)^{n}Q)^{(k)}=\sum_{\ell=0}^{k} {k\choose \ell}((X-\alpha)^{n})^{(\ell)}Q^{(k-\ell)}
$$
or on a
$$
((X-\alpha)^{n})^{(\ell)}=\frac{k!}{(k-\ell)!}(X-\alpha)^{n-\ell}
$$
et évalué en $\alpha$, on obtient $0$ **pour $\ell<n$.**

Donc pour $n$
$$
P^{(n)}(\alpha)= {n\choose n} ((X-\alpha)^{n})^{(n)}(\alpha)Q^{(0)}(\alpha) = Q(\alpha) \neq 0
$$
et pour $k$ on obtient $0$.

# $\impliedby$

Par la formule de Taylor polynômiale, on a
$$
\begin{align}
P&=\sum_{k=0}^{+\infty}P^{(k)}(\alpha) \frac{(X-\alpha)^{k}}{k!} \\
&= \sum_{k=n}^{+\infty} P^{(k)}(\alpha) \frac{(X-\alpha)^{k}}{k!} \\
&= \sum_{\ell=0}^{+\infty-\ell} P^{(\ell+n)}(\alpha) \frac{(X-\alpha)^{n+\ell}}{(n+\ell)!} \\
&= (X-\alpha)^{n} \sum_{k=0}^{+\infty} \dots
\end{align}
$$
donc racine d'ordre au moins $n$ de $P$

Supposons par l'absurde qu'elle est d'ordre supérieur
On aurait $P=(X-a)^{n+1}Q$
$$
P=(X-\alpha)^{n+1}Q=(X-\alpha)^{n}\sum \dots
$$
par intégrité, on a
$$
(X-\alpha)Q = \sum \dots
$$
on a alors $\alpha$ racine de $\sum\dots$ mais c'est contradictoire car $Q$ ne diviserait pas $P$.