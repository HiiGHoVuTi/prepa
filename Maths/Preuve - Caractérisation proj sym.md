---
dg-publish: true
---

Projecteur
---

- $\implies$
	Trivial
- $\impliedby$
	Montrons que $p$ projette sur $\text{Im}p$ parallèle à $\text{Ker}p$
	- On a bien $p$ linéaire par hypothèse
	- Montrons que $E=\text{Im}p\oplus \text{Ker}p$
		- Analyse: On suppose $x=x_{\text{Im}p}+x_{\text{Ker}p}\in E$, on a donc $p(x)=x_{\text{Im}p}$ et $x-p(x)=x_{\text{Ker}p}$
		- Synthèse ok
	- Soit $q$ le projecteur sur $\text{Im}p$ parallèle à $\text{Ker}p$, on a $x=p(x)+(x-p(x))$ donc $p(x)=q(x)$ pour tout $x$


Symétrie
--

- $\implies$
Trivial
- $\impliedby$
	Montrons que $s$ est symétrie sur $\text{Ker}(s-\text{id})$ parallèle à $\text{Ker}(s+\text{id})$
	- On a bien $s$ linéaire par hypothèse
	- Montrons que $E=\text{Ker}(s-\text{id})\oplus \text{Ker}(s+\text{id})$
		- Analyse: On suppose $x=x_{1}+x_{-1}\in E$, on a donc $x_{1}=\frac{s(x)+x}{2}$ et $x_{-1}=\frac{x-s(x)}{2}$
		- Synthèse ok
	- Soit $s$ la symétrie, ok

