---
dg-publish: true
---

$$
\begin{align}
E(X)&=\sum k{n\choose k} p^{k}(1-p)^{k} \\
&= n\sum {n-1\choose k-1} p^{k}(1-p)^{k} \\
&= np \sum p^{\ell}(1-p)^{n-1+\ell} \\
&= np \times (p+(1-p))^{n-1} \\
&= np
\end{align}
$$

$$
\begin{align}
V(X) &= E(X^{2})-E(X)^{2} \\
&= \sum k^{2}{n\choose k}p^{k}(1-p)^{n-k} -(np)^{2}\\
&= \sum kn{n-1 \choose k-1} p^{k}(1-p)^{k} -(np)^{2}\\
&= \sum n(n-1) {n-2 \choose k-2}p^{k}(1-p)^{n-k}+ \sum n{n-1\choose k-1}p^{k}(1-p)^{n-k} - (np)^{2}\\
&=n(n-1)p^{2}\times(p+(1-p))^{n-2}+ np\times (p+(1-p))^{n-1}-(np)^{2} \\
&= n\times p(p-1)
\end{align}
$$
