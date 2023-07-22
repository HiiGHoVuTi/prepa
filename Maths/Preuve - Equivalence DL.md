---
dg-publish: true
---

par troncature
$$
f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}+o(x^{n})
= 0+0+\dots+a_{p}x^{p}+o(x^{p})
$$

donc
$$
\begin{align}
\frac{f(x)}{a_{p}x^{p}} &= \frac{1+o(x^{p})}{a_{p}x^{p}} \\
&= \frac{1+x^{p}\epsilon(x)}{a_{p}x^{p}} \\
&= 1+o(1) \\
&\xrightarrow[x \to 0]{} 1
\end{align}
$$
