---
dg-publish: true
---

# $1.$

![[Maths/Lemme - décomposition p-adique]]

Preuve triviale avec le lemme.

# $2.$

Par la première propriété,

$$
xy = \prod_{p \in \mathcal{P}} p^{\text{val}_{p}(x)+\text{val}_{p}(y)} = \prod_{p\in \mathcal{P}}p^{\text{val}_{p}(xy)}
$$
par unicité de la décomposition, ok.

# $3.$

## $\implies$

On a $p^{\text{val}_{p}(x)}\mid y$, donc $\text{val}_{p}(x)\in \{ k \;;\; p^{k}\mid y \}$ donc ok.

## $\impliedby$

On a alors $p^{\text{val}_{p}(x)}\mid p^{\text{val}_{p}(y)}$ donc $p^{\text{val}_{p}(x)}\mid y$, puis par produit de premiers, $x \mid y$.