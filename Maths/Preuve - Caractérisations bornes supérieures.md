---
dg-publish: true
---

# $a. \implies b.$

Par l'absurde, on suppose qu'il existe $\varepsilon>0$ tel qu'il n'existe aucun $x_{0} \geq M-\varepsilon$
Donc pour $x \in A$, on a $x < M - \varepsilon$
Mais alors $M-\varepsilon$ est aussi majorant, absurde.

# $b. \implies c.$

On construit la suite suivante:
On sait que pour $\varepsilon = \frac{1}{n}$ il existe $x_{n}\geq M - \frac{1}{n}$, on construit alors cette suite des $u_{n}=x_{n+1}$ (pour ne pas diviser par $0$).

Elle tend vers $M$ par le [[Maths/Preuve - Théorème des Gendarmes|théorème des gendarmes]].

# $c. \implies a.$

On appelle la suite en question $u_{n} \to M$ un majorant.

Par l'absurde, on suppose qu'il existe un autre majorant $M' < M$ avec $M'$ majorant aussi.
Or pour tout $n$, $x_{n} \in A$ donc $x_{n} \leq M'$. On [[Preuve - Passage de l'inégalité à la limite|passe à la limite]], et on obtient $M \leq M'$ absurde.