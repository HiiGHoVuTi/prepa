---
dg-publish: true
---

Soient $U,V,C$ les matrices d'intérêt. Montrons que $VU=C$.
Alors pour tout $j$,
- $\mathfrak{(v\circ u)}(e_{j})=\sum c_{ij}g_{i}$
- $\mathfrak{(v\circ u)}(e_{j})=\sum u_{kj}\mathfrak{v}(f_{k})=\sum u_{kj} \left( \sum v_{ik}g_{i} \right)=\sum g_{i}\left( \sum v_{ik}u_{kj} \right)$

donc par unicité de la décomposition,
$$
c_{ij}=\sum v_{ik}u_{kj}
$$
vrai pour tous $i,j$ donc $C=VU$.