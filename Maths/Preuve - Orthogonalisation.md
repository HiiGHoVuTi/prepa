---
dg-publish: true
---

*Initialisation*: Pour $i=1$, ok.
*Hérédité*: On suppose avoir $(o_{1}\dots o_{i})$ orthogonale avec $\text{Vect }(o_{1}\dots o_{i})=\text{Vect }(e_{1}\dots e_{i})$.
La famille est libre (car générateur de bon cardinal).
Si $i<n$, on a $\text{Vect }(o_{1}\dots o_{i}, e_{i+1})=\text{Vect }(e_{1}\dots e_{i}, e_{i+1})$.
On pose $o_{i+1}=e_{i+1}-\sum\alpha_{k}o_{k}$.
On calcule le produit scalaire $\braket{ o_{j} | o_{i+1} }=\braket{ o_{j} | e_{i+1} }-\alpha_{j}\braket{ o_{j} | o_{j} }$.
On en déduit que pour $\alpha_{j}=\frac{\braket{ o_{j} | e_{i+1} }}{\braket{ o_{j} | o_{j} }}$, $o_{i+1}$ convient.