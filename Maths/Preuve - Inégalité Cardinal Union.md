---
dg-publish: true
---

# Initialisation

Pour $\left| A  \right| = 1$,

$$
\left| A \right| \leq \left| A \right|
$$
ok, avec cas d'égalité

# Hérédité

Si on a
$$
\left| {\huge \cup}^{n} A_{i} \right| \leq \sum^{n} \left| A_{i} \right|
$$
avec égalité ssi les ensembles sont 2 à 2 disjoints

Considérons ${\huge \cup}^{n+1}A_{i}$
$$
\begin{align}
\left| {\huge \cup}^{n+1} A_{i} \right| &= \left| {\huge \cup}^{n} A_{i} \right| + \left| A_{n+1} \right| - \left| {\huge \cup}^{n}A_{i} \cap A_{n+1} \right| \\
& \leq \left| {\huge \cup}^{n} A_{i} \right| + \left| A_{n+1} \right| \\
& \leq \sum^{n} \left|  A_{i} \right| + \left| A_{n+1} \right| \\
& = \sum^{n+1}A_{i}
\end{align}
$$

Egalité si 
- $A_{n+1}$ disjoint avec tous les autres ensembles
- tous les autres ensembles sont disjoints 2 à 2
$\iff$
tous les $A_{i}$ sont disjoints 2 à 2