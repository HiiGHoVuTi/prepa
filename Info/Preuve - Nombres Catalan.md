On a 
$$
{2n\choose n+1} = \frac{n}{n+1}{2n\choose n}
$$
# $1. \implies 2.$

On procède par récurrence sur $\mathbb{N}$:
- init ok
- Par la première formule:
	$$
	\begin{align}
c_{n+1}&=\frac{2(2n+1)}{n+2}\times \frac{1}{n+1}{2n\choose n} \\
&= \frac{2(2n+1)2n!}{(n+2)(n+1)(n!)^{2}} \\
&= \frac{1}{n+2} \times \frac{(2n+2)!}{(n+1)!^{2}}
\end{align}
$$
# $1.$ est vraie

- Gauche
$c_{n+1}$ nombre d'arbres avec $n+1$ noeuds internes 
$(n+2)$ nombre de feuilles d'un tel arbre

- Droite
$2$ un sens
$2n+1$ nombre total de noeuds d'un tel arbre 
$c_{n}$ nombre d'abres à $n$ noeuds internes 

- On cherche une bijection entre 
	- les couples $(A,f)$ où $A$ est un arbre à $n+1$ noeuds et $f$ une feuille de $A$
	- les triplets $(B,x,\varepsilon)$ où $B$ est un arbre à $n$ noeuds internes, $x$ est un noeud quelconque de $B$ et $\varepsilon\in \{ \to,\leftarrow \}$

On propose les bijections réciproques:
- ==efface== qui à un couple $(A,f)$ associe $(B,x,\varepsilon)$
	- $B$ est obtenu en supprimant $f$ et son père, le frère de $f$ est remonté d'un cran
	- $x$ est le noeud remonté 
	- $\varepsilon$ est donné par la côté (gauche/droite) de $f$
- ==insère== qui à un triplet $(B,x,\varepsilon)$ associe le couple $(A,f)$
	- $A$ est obtenu à partir de $B$ en créant un nouveau noeud à la place de $x$
		- Si $\varepsilon = \;\leftarrow$, le fils gauche de ce nouveau noeud est une feuille, le fils droit est $x$
		- Sinon, l'autre côté
	- $f$ est la nouvelle feuille 


