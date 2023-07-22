---
dg-publish: true
---

- Si $y=f(a)$, alors $c=a$ convient
- Si $y=f(b)$ alors $c=b$ convient 


On suppose désormais une inclusion stricte. On étudie $f(x)-y$ et recherche son annulation.

Sans perte de généralité, on suppose $g(a)< 0 < g(b)$

# Méthode $\mathfrak{1.}$

On pose $A=\{ x\;;\; x\in [a,b], f(x)\leq 0 \}$, majorée et non-vide donc il existe $c=\text{sup}(A)$.
Montrons que $f(c)=0$.
Il existe une suite $(u_{n})\to c$ avec $f(u_{n})\leq 0$ mais comme $f$ est continue on a $f(u_{n})\to f(c)$ donc $f(c)\leq 0$

On en déduit $c\neq b$ car $f(b) > 0$.
On considère $v_{n}=c+\frac{1}{n}$, on a $v_{n}\not \in A$ mais $v_{n}\in [a,b]$ à partir d'un certain rang, donc $f(v_{n}) > 0$
et comme $f$ est continue,
$f(v_{n})\to f(c)$ donc $f(c) \geq 0$


# Méthode $\mathfrak{2.}$

On pose $a_{0}=a$ et $b_{0}=b$. On construit deux suites par récurrence $a_{n}$ et $b_{n}$ telles que 
$$
f(a_{n})\leq 0 \leq f(b_{n})
$$
__Terme suivant__:
On pose $\mu=\frac{a_{n}+b_{n}}{2}$
- Si $f(\mu)< 0$, alors $a_{n} =\mu$
- Sinon, $b_{n}=\mu$

On a $b_{n}-a_{n}$ géométrique de raison $\frac{1}{2}$, or $b_{n}\geq a_{n}$ donc [[Preuve - Suites Adjacentes|adjacentes]], tendent vers la même limite. 
On appelle les [[Preuve - Théorème des Gendarmes|gendarmes]].


