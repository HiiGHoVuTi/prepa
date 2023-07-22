---
dg-publish: true
---

On considère $f$ continue sur un intervalle
$$
\begin{align}
S_{n}-\int f &=\frac{b-a}{n}\sum_{k=0}^{n-1}f\left( a+k \frac{b-a}{n} \right)-\int_{a}^{b} f \\
  &=\frac{b-a}{n} \sum_{k=0}^{n-1}f\left( a + k \frac{b-a}{n} \right)- \sum_{k=0}^{n-1} \int_{a+k \frac{b-a}{n}}^{a+(k+1) \frac{b-a}{n}} f  \\
&= \sum_{k=0}^{n-1} \frac{b-a}{n} f\left( a+ k \frac{b-a}{n} \right) - \int_{a+k \frac{b-a}{n}}^{\dots} f \\
&=\sum_{k=0}^{n-1} \int _{\dots}^{\dots} f(t) - f\left( a+ k \frac{b-a}{n} \right) \, dt   \\
\end{align}
$$
Ainsi par inégalités triangulaires
$$
\begin{align}
A_{n}=\left| S_{n}-\int f(t) \, dt  \right|&\leq \sum_{k=0}^{n-1} \left|  \int f(t) - f\left( a + k \frac{b-a}{n} \right) \, dt  \right| \\
&\leq \sum_{k=0}^{n-1} \int \left| f(t) - f\left( a + k \frac{b-a}{n} \right) \right| \, dt 
\end{align}
$$

- Alors si $f$ est continue (donc uniformément continue) sur le segment $[a,b]$,
Pour tout $\varepsilon>0$ il existe $\eta>0$ tel que pour $\left| x-y \right|\leq \eta \implies \left| f(x)-f(y) \right|\leq \varepsilon$.
A partir d'un certain rang $\frac{b-a}{n}\leq \eta$ donc $\int \left| f(t)-f\left( a+k \frac{b-a}{n} \right) \right| \, dt \leq \int \varepsilon \, dt = \varepsilon\frac{(b-a)}{n}$.
Alors
$$
A_{n} \leq \sum_{k=0}^{n-1} \varepsilon \frac{(b-a)}{n} = \varepsilon (b-a)
$$
Donc la suite tend vers $0$.
- Si $f$ est de plus $\mathfrak{k}-$lipchitzienne,
$$
\begin{align}
A_{n} &\leq \sum \int  \mathfrak{k}\left| a+k \frac{b-a}{n} - t \right| \, dt \\
&=  \sum \int  \mathfrak{k}\left| \frac{b-a}{n} \right| \, dt \\
&= \sum \mathfrak{k}\left(\frac{b-a}{n}\right)^{2} \\
&= \mathfrak{k}\frac{(b-a)^{2}}{n} \\
A_{n}&= O\left( \frac{1}{n} \right)
\end{align}
$$
