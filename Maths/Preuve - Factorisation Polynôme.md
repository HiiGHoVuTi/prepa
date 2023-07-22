---
dg-publish: true
---

On fera par récurrence sur $n=\sum n_{i}$

Pour $n=1$ ok.

*Hérédité*: On suppose $Q$ avec racines $\beta_{1},\dots,\beta_{p}$ et $m_{1},\dots,m_{p}$ ordres avec $\sum m_{i}=n+1$

On suppose *SPDG* que $m_{1}\geq 1$ on a donc $Q=(X-\beta_{1})R$.
Montrons que $\beta_{k}$ est racine d'ordre au moins $m_{k}$ de $R$.
Pour $\ell \in \textlbrackdbl 0,m_{k}-1 \textrbrackdbl$

- On a $Q^{(\ell)}(\beta_{k})=0$

- Pour $\ell=0$, $Q(\beta_{k})=(\beta_{k}-\beta_{1})R(\beta_{k})$ donc $R(\beta_{k})= 0$
- Par récurrence rapide, $R^{(\ell)}(\beta_{k})=0$
> on fait $\ell\in \{ 1,2 \}$ puis on dit que ça se voit

On applique l'hypothèse de récurrence, ok.