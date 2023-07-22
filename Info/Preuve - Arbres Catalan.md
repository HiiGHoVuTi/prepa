On procède par récurrence
- Il existe un unique arbre sans noeuds internes
- Un arbre binaire à $n+1$ noeuds internes est constitué de
	- une racine
	- un arbre de gauche $k$ noeuds internes 
	- un arbre de droite de $n-k$ noeuds internes 
	on a bien
	$$
	c_{n+1} = \sum^{n}_{k=0} c_{k}c_{n-k}
	$$
