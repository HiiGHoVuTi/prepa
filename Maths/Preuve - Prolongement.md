---
dg-publish: true
---

# Analyse

Supposons $g$ prolongement de $f$, on a
$$
g(x)=\begin{cases}
\beta&\text{si } x=a \\
f(x)&\text{sinon}
\end{cases}
$$
Or $f$ admet une limite $b$ en $a$ et $g$ est continue en $a$, on a
$$
x\in I\setminus \{ a \}, \left| x-a \right|\leq \eta \implies \left| f(x)-b \right|\leq\varepsilon
$$

$$
x \in I, \left| x-a \right|\leq \delta \implies \left| g(x)-\beta \right|\leq\varepsilon
$$
Alors pour $\lambda\leq \text{min}\{ \eta,\delta \}$
$$
\left| g(x)-\beta \right|\leq \varepsilon \quad \left| f(x)-b \right|\leq\varepsilon
$$
Comme $x\neq a$,
$$
\left| g(x)-\beta \right|=\left| f(x-b) \right| \implies \left| b-\beta  \right|\leq 2\varepsilon
$$
ainsi $b-\beta=0$

# Synthèse

On fait une disjonction de cas et ok.