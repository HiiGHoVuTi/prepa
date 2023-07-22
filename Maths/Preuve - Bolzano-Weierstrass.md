---
dg-publish: true
---

# $\mathcal{I.}$ Par borne sup'

On définit $A_{n} = \{ u_k\;;\; k \geq n \}$. 
$A_{n}$ est bornée et $A_{n+1} ⊂ A_n$.
On définit $s_{n} = \text{sup}(A_{n})$. 
On remarque que $s_{n}$ est décroissante et minorée par $\text{inf}(A_{0})$.

Construisons la suite $(v_{n})$.
$s_{0}$ est la borne sup de $A_{0}$ donc il existe $u_{n_{0}}\in A_{0}$ avec $s_{0}-1 \leq u_{n_{0}} \leq s_{0}$
On pose alors $v_{0}=u_{n_{0}}$.
Pour $v_{k+1}$, on suppose avoir construit jusqu'à $v_{k}=u_{n_{k}}$ tel que 
$$
s_{n_{k-1}}-\frac{1}{k+1}\leq u_{n_{k}} \leq s_{n_{k-1}+1}
$$
On a $s_{n_{k}+1}$ la borne sup de $A_{n_{k}+1}$ donc il existe $u_{n_{k+1}} \in A_{n_{k}+1}$ tel que: 
$$
s_{n_{k}+1} - \frac{1}{k+2} \leq u_{n_{k+1}} \leq s_{n_{k}+1}
$$
On pose $v_{k+1}=u_{n_{k+1}}$.

On prouve la convergence par le [[Preuve - Théorème des Gendarmes|théorème des gendarmes]] car une suite extraite de $(s_{n})$ converge aussi.

# $\mathcal{II}.$ Par dichotomie

$(u_{n})$ est bornée donc il existe $a,b\in \mathbb{R}$ bornes. Construisons deux suites auxiliaires.
On pose $a_{0} = a$ et $b_{0}=b$ puis
1. Si il existe une infinité d'entiers $k$ tels que $\frac{a_{n}+b_{n}}{2}\leq u_{k}\leq b_{n}$, on pose $b_{n+1}=b_{n}$ et $a_{n+1}=\frac{a_{n}+b_{n}}{2}$
2. Si il existe une infinité d'entiers $k$ tels que $a_{n} \leq u_{k} \leq \frac{a_{n}+b_{n}}{2}$, on fait dans l'autre sens
3. Sinon, contradition :luc_zap:.

On remarque que $(a_{n}-b_{n})$ est géométrique de raison $\frac{1}{2}$ et converge vers $0$. De plus $(a_{n})$ est croissante et $(b_{n})$ est décroissante donc elles sont adjacentes et convergent vers $\ell$.

On choisit un $v_{0}=u_{0}$ et pour $v_{n+1}$, on a une infinité de $u_{k}$ avec $a_{n+1}\leq u_{k} \leq b_{n+1}$, on choisit un $k_{n+1}>k_{n}$ et on pose $v_{n+1} = u_{k_{n+1}}$

On prouve la convergence par le [[Preuve - Théorème des Gendarmes|théorème des gendarmes]].
