---
dg-publish: true
---

On a:
$$
A = (A\setminus A \cap B) \cup (A \cap B)
$$
donc
$$
\left| A  \right| = \left| A \setminus A \cap B \right| + \left| A \cap B \right|
$$

de plus, on a
$$
A \cup B = (A \setminus A \cap B) \cup B
$$
par double inclusion
- $\subset$: disjonction de cas selon si $x \in B$
- $\supset$: disjonction de cas selon si $x \in A \setminus A \cap B$

Les deux ensembles sont-ils disjoints ?
- par l'absurde
$$
\begin{align}
\left| A \right| &= \left| (A \setminus A \cap B) \cup B \right| = \left| A \setminus A \cap B \right| + \left| B \right| \\

&=\left| A \right| + \left| B  \right| - \left| A \cap B \right|
\end{align}
$$
