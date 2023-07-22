---
dg-publish: true
---

Montrons que $F'(x_{1})=f(x_{1})$
$$
\begin{align}
&\frac{F(x+h)-F(x)}{h} - f(x) \\
&= \frac{ \int_{x_{0}}^{x+h} f(t)+ \, dt -\int _{x_{0}}^{x}f(t) \, dt -hf(x) }{h} \\
&=\frac{1}{h} \int_{x}^{x+h} f(t)-f(x) \, dt \\ 
\end{align}
$$
Fixons $\varepsilon>0$, Si $0\leq h \leq \eta$ on a $\left| t-x \right|\leq \eta$
$$
\begin{align}
\left| \frac{1}{h}\int_{x}^{x+h} f(t)-f(x) \, dt  \right| &\leq \frac{1}{h}\int _{h}^{x+h}\left| f(t)-f(x) \right| \, dt  \\
&=\frac{1}{h}\int \varepsilon \, dt  \\
&= \varepsilon
\end{align}
$$
Donc $\to 0$
