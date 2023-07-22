---
dg-publish: true
chapitres: Tas, Complexité
difficulté: ⭐⭐
---

On considère la structure de données nommée *Skew Heap* (abrégée en SH ici).
Le but de celle-ci est de fournir une file de priorité avec une structure moins ordonnée qu'un tas binaire (complet gauche).

Cas Basiques
---

1. Rappeler le fonctionnement d'un tas-min binaire
2. Rappeler l'utilité de sa stucture "complet gauche"

Nous étudierons une manière de supprimer le minimum d'un arbre binaire (satisfiant la propriété de tas) sans qu'il soit complet gauche.

On suppose disposer d'une fonction $\text{merge}: \mathcal{Sh}^{2} \to \mathcal{Sh}$ une fonction combinant deux SH en conservant la propriété de tas-min.

3. Implémenter $\text{insert} : \mathbb{Z} \to \mathcal{Sh}\to \mathcal{Sh}$ et $\text{extract-min} : \mathcal{Sh}\to \mathcal{Sh}\times \mathbb{Z}$
4. Donner leur complexité selon celle de $\text{merge}$

Merge
---

Implémentons alors $\text{merge}$ de manière efficace

1. Donner le cas où l'un des SH est vide

On a alors $p$ le SH avec la plus petite racine et $q$ l'autre.

2. Implémenter $\text{merge}$ de manière naïve, en plaçant tous les enfants à droite. Quelle problème de complexité a-t-on ?
3. On propose que le nouveau fils gauche soit le fils droit de $p$. Implémenter l'algorithme correspondant.

> on a alors "inversé" les enfants droits et gauches


Analyse amortie
---

On dit d'un enfant qu'il est lourd (sinon léger) si la taille de son sous-arbre est plus grand que la moitié du sous-arbre de son parent

1. Montrer qu'on rencontre au plus $\log n$ enfants légers lors d'une descente de l'arbre.

 On note $\ell$ et $L$ le nombre d'enfants légers et lourds sur le chemin de droite de l'arbre.

2. Montrer que $\text{merge}$ s'effectue en $\mathcal{O}(\ell+L)$ opérations.

On pose le potentiel $\Phi = L$

3. Montrer que $\Delta\Phi \leq \ell-L$ lors de $\text{merge}$.
4. En déduire que la complexité amortie est $\mathcal{O}(\log n)$, avec $n$ la taille de l'arbre.