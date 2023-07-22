---
dg-publish: true
---

Soit $\mathcal{F}=(e_{1}\dots e_{n})$ finie et génératrice.

*Algorithme*:
- Entrée: $\mathcal{F}$ une telle famille
- Sortie: $\mathcal{B}$ une base de $E$
- Procédure:
	- Si $\mathcal{F}$ est libre, fini (et on remarque que le singleton est libre).
	- Sinon, appel récursif sur $(e_{1}\dots e_{n-1}) \to \mathfrak{B}$ libre.
		- Si $e_{n}\in \text{Vect}\mathfrak{B}$, alors on a $\mathfrak{B}$ génératrice et libre.
		- Sinon, $\mathfrak{B}\cup e_{n}$ est génératrice et libre.
- Terminaison: Variant de boucle