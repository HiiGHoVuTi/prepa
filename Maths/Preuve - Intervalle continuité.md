---
dg-publish: true
---

# $1. \implies 2.$

conséquence du [[Preuve - TVI|TVI]]


# $2. \implies 1.$

Supposons $f(I)$ un intervalle, soit $\kappa\in I$, montrons que $f$ est continue en $\kappa$.
Sans perte de généralité, $f$ est croissante.

Fixons $\varepsilon>0$, trouvons un $\eta-$voisinage où $\left| f(x)-f(\kappa) \right|\leq\varepsilon$.

On peut choisir $f(\kappa)-\varepsilon,f(\kappa)+\varepsilon \in f(I)$. On choisit donc $\alpha,\beta$ tel que $f(\alpha)=\kappa-\varepsilon,f(\beta)=\kappa-\varepsilon$.

$f$ est croissante donc on a $f(\alpha)\leq f(x)\leq f(\beta)$ donc $\left| f(x)-f(\kappa) \right|\leq \varepsilon$.

On choisit donc $\eta=\text{min}\{ \beta-\kappa, \kappa-\alpha \}$.

> erreur potentielle de recopiage