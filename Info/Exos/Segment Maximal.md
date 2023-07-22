---
dg-publish: true
chapitres: Listes, Algèbre
difficulté: ⭐⭐
---

Implémentation Naïve
---

On considère le problème du segment maximal.
Soit $L=[L_{0}, L_{1}, \dots, L_{n-1}]$ une liste de $n$ entiers relatifs, on cherche la sous-liste contigue avec la somme maximale.
$$
\text{max}_{i,j} \sum_{i\leq k \leq j} L_{k}
$$

0. Donner le segment maximal de $[1, -2, 3, 4, -1, 4, -2]$
1. Implémenter un algorithme naïf calculant cette somme
2. Donner sa complexité, expliquer en quoi la plupart des calculs sont redondants

Une approche locale
---

On introduit un type $\mathcal{S}$ qui stockera toutes les informations nécessaires pour résoudre le problème sur une sous-liste.
L'objectif est de déterminer une fonction $\oplus : \mathcal{S}^{2} \to \mathcal{S}$ telle que si $a,b:\mathcal{S}$ représentent la solution pour deux sous-listes, alors $a\oplus b$ représente la solution pour l'union des deux sous-listes.

1. ⭐ Déterminer le type $\mathcal{S}$
> on pourra demander une indication
2. Déterminer une fonction $\text{singleton} : \mathbb{Z} \to \mathcal{ S}$
3. Déterminer la fonction $\oplus : \mathcal{ S}^{2} \to \mathcal{S}$
4. Exprimer alors une solution de complexité $\mathcal{O}(n)$

Des propriétés mathématiques
---

1. Démonter que $(\mathcal{S}, \oplus)$ est un monoïde, en particulier que $\oplus$ est associative
> un monoïde est un groupe sans inverses
2. Expliquer ce que signifie l'associativité en termes d'ordre de calculs
3. Considérons travailler sur une machine moderne, proposer un algorithme plus rapide
4. Un compilateur pourrait-il optimiser le code écrit automatiquement ?
> rechercher "list homomorphisms" et "loop fusion"

