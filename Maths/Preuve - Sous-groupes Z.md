---
dg-publish: true
---

# Premier sens

Si $a=0$, on a $a\mathbb{Z}=\{ 0 \}$ idéal trivial.
Sinon, on pose 
$$
\begin{align}
\varphi : \mathbb{Z} &\to \mathbb{Z}/a\mathbb{Z}  \\
k & ↦ \mathcal{C\ell}_{\equiv[a]}(k)
\end{align}
$$
est un morphisme de $(\mathbb{Z},+)$ dans $(\mathbb{Z}/n\mathbb{Z},+)$.
On a $\text{Ker}\varphi$ un sous-groupe de $\mathbb{Z}$, or $\text{Ker}\varphi =a\mathbb{Z}$.

# Deuxième sens

Soit $(H,+)$ est un sous-groupe de $(\mathbb{Z},+)$
Si $H=\{ 0 \} =0\mathbb{Z}$, ok.
Sinon, on a quand même $0\in H$ donc il existe $\alpha \in H$.
Soit $A=H\cap \mathbb{N}^{*}$, alors on a $A$ non-vide car $\alpha$ ou $-\alpha$ est positif. 
Alors $A$ admet un plus petit élément $a$. On en déduit que $a\mathbb{Z} \subset H$.
Réciproquement, soit $m=aq+r$ avec $0 < r <a$ 
d'où $r=m-aq \in H$ avec $0 \leq r < a$ donc $r=0$. Ainsi $a\mid m$ ok.