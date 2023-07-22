---
dg-publish: true
---

1. $f$ continue

Fixons $\varepsilon>0$,

Par le théorème d'approximation, il existe $\left| f-\varphi \right|\leq \varepsilon$ avec $\varphi$ en escalier, donc 
$$
\begin{align}
\int f(t) \, dt &=\int f(t)-\varphi(t) \, dt + \int \varphi (t) \, dt \\
\left| \int f(t) \, dt  \right| &\leq \int \left| f(t)-\varphi(t) \right| \left| e^{i\lambda t} \right| \, dt + \left| \int \varphi(t)e^{i\lambda t} \, dt  \right| \\
&\leq  \varepsilon(b-a) + \int \varphi(t)e^{i\lambda t} \, dt \\ 
\end{align}
$$
avec $\varphi(t)$ en escaliers, on calcule alors
$$
\int \varphi(t)e^{i\lambda t} \, dt = \sum_{k} \left[ \frac{a_{k}}{\lambda i} \right]_{x_{k}}^{x_{i+1}} \xrightarrow[\lambda \to \infty]{} 0
$$

2. Si $f$ continument dérivable
On peut faire une IPP,
$$
\begin{align}
I &=\int _{a}^{b} f(t) e^{i\lambda t} \, dt \quad \begin{cases}
u(t) = f(t), u'(t)=f'(t) \\
v'(t) = e^{i\lambda t}, v(t)=\frac{e^{i\lambda t}}{i\lambda}
\end{cases}  \\
&= \left[f(t) \frac{e^{i\lambda t}}{i\lambda}\right]_{a}^{b} - \frac{1}{i\lambda}\int f'(t)e^{i\lambda t} \, dt  \\
&= \frac{1}{i\lambda}\left( e^{i\lambda t} (f(b)-f(a)) - \int f'(t)e^{i\lambda t} \, dt  \right)  \\
\left| I\right| &\leq \frac{1}{\lambda}\left| e^{i\lambda t}(f(b)-f(a)) - \int _{a}^{b} f'(t)e^{i\lambda t} \, dt  \right| \\
&\leq \frac{1}{\lambda}\left( \left| f(b) - f(a) \right| + \left|\int f'(t)e^{i\lambda t} \, dt \right| \right) \\
&\leq \frac{1}{\lambda}\left( \left| f(b) \right|+\left| f(a) \right|+\int_{a}^{b} \left| f'(t) \right| \, dt  \right)  \\
&= O_{\lambda\to \infty} \left( \frac{1}{\lambda} \right) 
\end{align}
$$

