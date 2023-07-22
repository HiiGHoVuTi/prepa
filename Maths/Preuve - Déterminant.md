---
dg-publish: true
---

*Analyse*

Supposons $f$ convenante.
On a
$$
\begin{align}
f(u_{i}\dots u_{n})&=f\left( \sum x_{i,1}e_{i}, u_{2}\dots u_{n} \right) \\
&= \sum_{i} x_{i,1} f(e_{i}, u_{2}\dots u_{n}) \\
&=\sum_{i} \sum_{j} x_{i,1}x_{j,2}f(e_{i}, e_{j}\dots u_{n}) \\
&= \sum_{i} \sum_{j}\dots \sum_{z} x_{i,1}x_{j,2}\dots x_{z,n} f(e_{i}, e_{j}\dots e_{z}) \\
&\qquad\qquad \qquad\qquad\qquad\qquad \text{nul si non-distincts} \\
&= \sum_{\sigma\in S_{n}} \varepsilon(\sigma) \prod x_{\sigma(i),i} 
\end{align}
$$

*Synthèse*

- Antisymétrie ? ok, on compose par $\tau$
- Linéarité ? ok, par rapport à la première variable, puis ttes les autres par antisymétrie !