---
aliases: [Fractions rationnelles]
dg-publish: true
order: 20
active: true
---

On supposera que $\mathbb{K}\in \{ \mathbb{R}, \mathbb{C} \}$ dans ce cours :(

# Généralités

## Corps des fractions rationnelles

$$
\mathbb{K}(X) = \left\{  \frac{P}{Q} \;\;;\;\ P\in \mathbb{K}[X],Q \in \mathbb{K}[X]^{\times}  \right\}
$$

$$
\frac{P}{Q}=\frac{R}{S} \iff PS - RQ = 0
$$

$$
\frac{P}{Q}+\frac{R}{S}=\frac{PS+RQ}{QS}
$$

$$
\frac{P}{Q} \times \frac{R}{S} = \frac{PR}{QS}
$$

On vérifiera bien avoir une structure de corps.

$$
\text{deg} \frac{P}{Q}=\text{deg} P-\text{deg} Q
$$

On vérifiera la cohérence de cette défiinition

# $\mathbb{K}=\mathbb{C}$

## Décomposition en éléments simples

Pour $F\in \mathbb{C}(X)$, il existe une unique décomposition de la forme

$$
F=P_{1}+ \sum_{i,j} \frac{\alpha_{ij}}{(X-\beta_{i})^{j}}
$$

où $P_{1}\in \mathbb{C}[X]$, $\beta_{i}\in \mathbb{C}$ deux à deux distincts et $\alpha_{ij}\in \mathbb{C}$.
Si le $\alpha_{i,j_{max}}\neq 0$, on dit que $\beta_{i}$ est un pôle d'ordre $j_{max}$

![[Maths/Preuve - Décomposition en éléments simples]]

### Pôle Simple

Si $\alpha$ est un pôle simple, la partie polaire associée à $\alpha$ est
$$
\frac{\lambda_{\alpha}}{X-\alpha}
$$
où $\lambda_\alpha= \frac{P(\alpha)}{Q'(\alpha)}$

![[Maths/Preuve - Pole simple]]

### Quotient Dérivée

$$
\frac{P'}{P}=\sum_{\alpha \text{ racine de }P} \frac{n\alpha}{X-\alpha}
$$

![[Maths/Preuve - Fraction Rationnelle Dérivée]]

### Théorème de Gauss-Lucas

Les racines de $P'$ sont dans l'enveloppe convexe des racines de $P$.

![[Maths/Preuve - Lucas]]

# Développements en éléments simples sur $\mathbb{R}$

Soit $F\in \mathbb{R}(X)$, il existe une unique décomposition de la forme
$$
F = P_{1}+\sum \sum \frac{a_{ij}}{(X-b_{i})^{j}} + \sum \sum \frac{c_{ij}X + d_{ij}}{(X^{2}+b_{i}X+g_{i})^{j}}
$$
avec $f_{i},g_{i}$ deux à deux distincts, et $b_{i}^{2}-4g_{i}< 0$
> preuve: pas à savoir

