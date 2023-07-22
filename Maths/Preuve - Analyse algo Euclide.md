---
dg-publish: true
---

Soient $a,b\in \mathbb{Z}$, on pose $a_{0}=a$ et $b_{0}=b$

Supposons avoir construit $a_{n} \land b_{n}=a\land b$.

- Si $b_{n}\mid a_{n}$ on a $a\land b=a_{n}\land b_{n}=b_{n}$.
- Sinon, on a $a_{n}=b_{n}+q_{n}+r_{n}$ avec $0 < r_{n} < \left| b_{n} \right|$
Donc $a_{n}\land b_{n}=(a_{n}-q_{n}b_{n})\land b_{n}=b_{n}\land r_{n}$
On pose alors $a_{n+1}=b_{n}$ et $b_{n_+1}=r_{n}$.

L'algorithme est donc correct.
De plus, $(b_{n})$ est strictement décroissante dans $\mathbb{N}$ donc on atteint forcément $0$.