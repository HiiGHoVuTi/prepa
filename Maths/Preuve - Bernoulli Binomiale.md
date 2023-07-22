---
dg-publish: true
---

On pose $X=\sum X_{k}$, alors $X(\Omega)\subset \textlbrackdbl 0,n \textrbrackdbl$.
$$
\begin{align}
P(X=k)&=P\left(\bigcup_{I \subset \textlbrackdbl 1,n \textrbrackdbl,\, \left| I \right| =k } (X_{i\in I}=1) \cap (X_{i \not \in I}=0) \right) \\
&= \sum_{I\subset \textlbrackdbl 1,n \textrbrackdbl } P((X_{i\in I}=1) \cap (X_{i \not \in I}=0)) \\
&= \sum_{I\subset \textlbrackdbl 1,n \textrbrackdbl } \prod_{k\in I} P(X_{i}=1) \prod_{i\not\in I} P(X=0) \\
&= \sum_{I\subset \textlbrackdbl 1,n \textrbrackdbl } p^{\left| I \right|}(1-p)^{n-\left| I \right|} \\
&= {n \choose k} p^{k}(1-p)^{n-k}
\end{align}
$$
