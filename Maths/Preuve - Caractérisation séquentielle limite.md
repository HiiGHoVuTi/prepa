---
dg-publish: true
---

# $1. \implies 2.$

Soit $\varepsilon>0$, comme $f(x)\xrightarrow[x \to a]{}\ell$ il existe un $\eta-$voisinage avec $\left| f(x)-\ell \right|<\varepsilon$.

Or $u_{n}\xrightarrow[n \to +\infty]{}a$ donc il existe $N$ tel que pour $n\geq N$ on a $\left| u_{n}-a \right|\leq \eta$.

Donc $u_{n}$ est dans le $\eta-$voisinage, ok.

# $2. \implies 1.$

On raisonne par contraposée. Supposons que la fonction ne tend pas vers $\ell$, soit
$$
\exists \varepsilon>0, \forall \eta>0, \exists x\in I, \left| x- a \right|\leq \eta\text{ et } \left| f(x)-\ell \right|>\varepsilon
$$
On cherche à construire une suite $u_{n}\xrightarrow[n \to +\infty]{}a$ avec $f(u_{n})\not \xrightarrow[n \to +\infty]{}n$ 

- Comme $1>0$, il existe $u_{0}$ dans $I$ tel que $\left| u_{0} -a \right|\leq 1$ et $\left| f(u_{0})-\ell \right|>\varepsilon$

- En général, on a $\frac{1}{n+1}>0$ donc il existe $u_{n}$ tel que $\left| u_{n}-a \right|\leq \frac{1}{n+1}$ et $\left| f(u_{n})-\ell \right|> \varepsilon$

Par le théorème des gendarmes, $u_{n}\xrightarrow[n \to +\infty]{}a$, et si $f(u_{n})\to \ell$, par opération sur les limites, on obtient
$$
0 \geq \varepsilon > 0
$$
donc $f(u_{n})\not\to \ell$

