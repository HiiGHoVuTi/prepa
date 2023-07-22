---
dg-publish: true
---

#category-theory

C'est un des domaines les plus abstraits des mathématique et pourtant est aussi très utile en programmation fonctionnelle.

# $\dots$ un peu d'histoire de la programmation

## Modèles de calcul

- Machine de Turing
	-> ASM
	-> Procédures
	-> Abstractions orientées objet
- Church 
	-> $\lambda$-calcul
	-> $\dots$

En programmation, on remarque que les innovations consistent souvent en:
	-> Abstractions
	-> Composabilité (diviser pour ~~régner~~ recomposer)

## Pourquoi pas d'objets ?

Ils cachent les mauvaises choses par l'abstraction:
- mutabilité
- partage de références

Cela les rend non-composables, et créent des "data races".

> Les programmes concurrents mettent en lumière que les abstractions objets ne sont pas les plus efficaces

## Et donc ?

La *programmation fonctionnelle* fut inventée avant l'orientée objet mais n'a gagné en popularité que longtemps après.

> par exemple: Lisp (1958), Haskell (1990), OCaml (1996), Idris (2007)

## Pourquoi du Haskell dans ces cours ?

Haskell est le meilleur mix entre abstraction et lisibilité. Il a une syntaxe plus lisible que LISP, sans les détails techniques complexes d'Idris, tout en permettant une relativement grande abstraction (une seule catégorie $\mathcal{Hask}$ cependant).

# Pourquoi $CT$ ?
$CT$ est un niveau d'abstraction au-dessus des autres langages fonctionnels. Elle aide à unifier des disciplines des mathématiques très variées telles que la logique, théorie des ensembles, géométrie, théorie des types, $\dots$

La théorie des ensembles est souvent considérée comme la base des mathématiques, mais elle révèle de nombreux paradoxes.
> Par exemple, le paradoxe du barbier. Un barbier ne doit tailler la barbe que de ceux qui ne se la taillent pas eux-mêmes. Doivent-ils se la tailler ?
> Ceci semble anodin, mais on se rend vite compte qu'il peut être traduit en théorie des ensembles.
$$
\begin{align}
\mathcal{B} &= \{ x \big| x \not\in x \} \\
\mathcal{B} &\in \mathcal{B} \quad?
\end{align}
$$
> De même, il n'y a pas d'ensemble de tous les ensembles.

Et donc au bout d'un moment, on s'est rendus compte des similarités entre les différents domaines des mathématiques.
> Par exemple la correspondance de Curry-Howard qui crée une équivalence entre chaque proposition logique et un élément d'un type (th. des types).
> L'équivalence de Curry-Howard-**Lambek** dit que *toute* catégorie cartésienne correspond exactement à la logique, aux types, et à la programmation.

On se rend donc compte que $CT$ est une abstraction immense sur la plupart des mathématiques modernes (orientés informatique). On en serait presque à se demander si les mathématiques sont inventées ou découvertes.

De plus, on observe qu'une approche majeure pour faire face à la complexité, on divise la situation complexe en plusieurs sous-parties puis on recompose la solution. *On ne sait que diviser pour régner*.
> Parfois ce n'est pas la bonne méthode, par exemple, les molécules->atomes->quarks->$\dots$  (deviennent des champs, des ondes, pas juste des points).
> Ces théories semblent difficiles à comprendre **car elles ne suivent pas de modèle de décomposition**

Ainsi, $CT$ est une manière de formaliser l'approche de composabilité.