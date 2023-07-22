---
dg-publish: true
---

$$
\int_{2}^{n+1}  \frac{dt}{t} \leq H_{n} \leq \int _{1}^{n} \frac{dt}{t}  
$$
Soit 
$$
\ln(n+1)-\ln(2)+1 \leq H_{n} \leq \ln(n)+1
$$
On pose $u_{n}=H_{n}-\ln(n)$.
On a $u_{n+1}-u_{n}=\frac{1}{n+1}-\frac{1}{n}+O\left( \frac{1}{n^{2}} \right)\sim -\frac{1}{n^{^{2}}}$ donc la série de terme $u_{n+1}-u_{n}$ converge.
Donc la suite converge vers une limite $\gamma$, et on a
$$
H_{n}=\ln(n)+\gamma+o(1)
$$
