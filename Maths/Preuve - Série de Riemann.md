---
dg-publish: true
---

Si $\alpha<0$, $\frac{1}{n^{\alpha}}\not\to 0$ donc la série diverge grossièrement

Soit $\alpha>0$, l'application associée est décroissante sur $\mathbb{R}^{\star}_{+}$.
On a
$$
\begin{align}
\int_{k}^{k+1} \frac{dt}{t^{\alpha}} &\leq \frac{1}{k^{\alpha}}\leq \int_{k-1}^{k} \frac{dt}{t^{\alpha}} \\
\int  \frac{1}{t^{\alpha}} \, dt &\leq \sum \frac{1}{k^{\alpha}} \leq \int \frac{1}{t^{\alpha}} \, dt \\
\frac{1}{1-\alpha}((n+1)^{1-\alpha}-2^{1-\alpha})&\leq \sum \frac{1}{k^{\alpha}}\leq \frac{1}{1-\alpha}(n^{1-\alpha}-1)  
\end{align}
$$
Si $\alpha<1$, le membre de gauche diverge
Sinon, le membre de droite est majoré par $\frac{1}{\alpha-1}$ ok.
Pour $\alpha=1$, suite harmonique, on encadre par $\ln$ qui diverge
