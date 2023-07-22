---
dg-publish: true
---

# Unicité

On suppose qu'il existe deux couples $(Q_{1},R_{1})$ et $(Q_{2},R_{2})$, on remarque que $B(Q1-Q2)=R2-R1$.

Si $Q_{1}\neq Q_{2}$ on a $\text{deg}B(Q_{1}-Q_{2})=\text{deg}B+\text{deg}(Q_{1}-Q_{2})\geq \text{deg}B$
or $\text{deg}B(Q_{1}-Q_{2})=\text{deg}(R_{2}-R_{1})\leq \text{max}\{ \text{deg}R_{1},\text{deg}R_{2} \}<\text{deg}B$
contradictoire.

# Existance

Initialisation: $Q_{0}=0, R_{0}=A$

Hérédité: si $\text{deg}R_{n}<\text{deg}B$ finito
Sinon,
Soient $\gamma$ le coefficient dominant de $B$ et $\delta$ de $R_{n}$
On a alors
$$
\begin{align}
A&=Q_{n}B+R_{n}-\frac{\delta}{\gamma}BX^{\text{deg} R_{n}-\text{deg} B}+\frac{\delta}{\gamma}X^{\text{deg} R_{n}-\text{deg} B} \\
&= (\dots)B+\dots
\end{align}
$$
On pose $Q_{n+1} = \frac{\delta}{\gamma}X^{\text{deg}R_{n}-\text{deg}B}+R_{n}$ et $R_{n+1}=R_{n}-\frac{\delta}{\gamma}BX^{\text{deg}R_{n}-\text{deg}B}$