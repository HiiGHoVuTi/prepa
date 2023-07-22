---
dg-publish: true
---

- On suppose qu'il existe une sous-matrice carrée $\hat{M}$ extraite de $M$ inversible d'ordre $q>r$.
On pose $M=(C_{1}\dots C_{p})$, montrons que $(C_{\psi(1)}\dots C_{\psi(p)})$ est libre. Comme $\hat{M}$ est inversible, ses colonnes sont libres donc en particulier, en écrivant la combinaison linéaire, on obtient tous les coefficients sont nuls (rien qu'avec les $q$ coefs).
Alors on a $\text{rg}(C_{1}\dots C_{p})\geq \text{rg}(C_{\psi(1)}\dots C_{\psi(q)})=q>r$ contradiction.

- Comme $\text{rg}M=r$, on peut choisir $r$ colonnes $(C_{\psi(1)}\dots C_{\psi(r)})$ libres. C'est donc une base de $\text{Vect}M$. On construit la matrice $\hat{M}$ (sans les lignes qui dépassent) qui est inversible.