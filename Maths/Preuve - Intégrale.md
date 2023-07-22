---
dg-publish: true
---

On montre $A,B$ non-vides et majoré (resp minoré).
Montrons que les deux quantités sont égales
$$
\int \varphi \leq \int f \leq \int  \psi  
$$
donc $\text{sup}A \leq \int \psi$ puis $\text{sup}A \leq \text{inf}B$
Par le théorème d'approximation, pour une $\varepsilon>0$ choisi, il existe $\varphi$ et $\psi$ tels que $\psi-\varphi \leq \varepsilon$ d'où
$$
\int \psi-\varphi \leq \int\varepsilon  \implies \int \psi\leq (b-a)\varepsilon + \int \varphi
$$
Puis en passant au sup et inf, $\text{sup}A\leq (b-a)\varepsilon + \text{sup}B$ et par passage à la limite ok.

