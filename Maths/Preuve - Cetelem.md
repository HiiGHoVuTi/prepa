---
dg-publish: true
---

1. Méthode sans base

On a $\text{dim}F\cap G\leq \text{dim}F$. 

De plus, il existe $H$ un supplémentaire de $F\cap G$ dans $F$ avec $\text{dim}H=\text{dim}F-\text{dim}F\cap G$.

- Montrons que $F+G=H\oplus G$.
	- Montrons $F+G=H+G$
		- $\supset$ trivial
		- $\subset$ on décompose et ok
	- Montrons que $H\oplus G$, en montrant $H\cap G=\{ 0 \}$

2. Méthode avec base

$F\cap G$ est un sev de $F$ et $G$. Soit $\mathfrak{H}$ une base de $F\cap G$, on pose $\mathfrak{h}=\text{dim}F\cap G$.
Par le théorème de la base incomplète, on peut compléter en base de $F$ et de $G$, respectivement $\mathfrak{H\cup F_{1}},\mathfrak{H\cup G_{1}}$ de dimensions $\mathfrak{h+f,h+g}$. 

Montrons que  $\mathfrak{W=H\cup F_{1}\cup G_{1}}$ est base de $F+G$.

*Génératrice* ok par décomposition
*Libre* On passe ce qui appartient à $F$ et à $G$ de chaque côté, on décompose alors dans $F\cap G$. On a donc une combinaison linéaire dans $\mathfrak{H\cup G_{1}}$ libre, donc par ricochet tous les coefficients sont nuls.

$\text{dim}E+F=\mathfrak{h+f+g}=\mathfrak{(h+f)+(h+g)-h}=\text{dim}F+\text{dim}G+\text{dim}F\cap G$

