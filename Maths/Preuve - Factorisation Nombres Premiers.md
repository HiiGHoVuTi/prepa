---
dg-publish: true
---
# Existance

Preuve par récurrence forte pour l'existance

## Initialisation

Pour $n=2$ ok.

## Hérédité

Si $n+1$ est premier, ok.
Sinon, on a $n+1 = \alpha\beta$. Or on sait que $\alpha$ et $\beta$ sont décomposables:
$$
\alpha=\prod_{p\in A\subset \mathcal{P}} p^{\alpha_{p}}, \beta=\prod_{p\in B \subset \mathcal{P}}p ^{\beta_{p}}
$$
Alors,
$$
n+1 = \alpha\beta = \prod_{p\in A\cup B\subset \mathcal{P}} p^{\alpha_{p}+\beta_{p}}
$$
## Conclusion $\huge🕺$

ok.


# Unicité

On suppose 
$$
n = \prod_{p\in A \subset \mathcal{P}} p^{\alpha_{p}} = \prod_{q\in B \subset \mathcal{P}} q^{\beta_{q}}
$$
Soit $p\in A$, on a $p\mid n$ donc il existe $q\in B$ tel que $p \mid q$. 
**SPDG** on a $\alpha_{p}$ < $\beta_{q}$, on considère $\frac{n}{p^{\alpha_{p}}}$ et on obtient une contradiction car $p$ divise le produit de droite mais pas de gauche.
On a alors $p=q$ et $\alpha_{p} = \beta_{q}$

