---
dg-publish: true
order: 8
---
#info/cours

Un arbre est une structure de donnée qui représente des données hiérarchiques
![[Cours Arbres 2023-01-09 10.16.33.excalidraw|100%]]

Un arbre est constitué de noeuds qui contiennent une valeur.
- Chaque noeud a un certain nombre d'enfants appelé son **arité**
- Un noeud d'arité $0$ s'appelle une feuille, sinon c'est un noeud interne
- Si $x$ est un enfant de $y$, alors $y$ est le père de $x$
- Le seul noeud sns père s'appelle racine
- Les ancêtres sont tous les noeuds "au-dessus"
- Les enfants d'un même père sont dits frères
- La profondeur est la longueur du chemin reliant à la racine 

>On va travailler principalement sur des arbres binaires, c'est-à-dire dont tous les noeuds internes sont d'arité $2$

>[!example]- Exemples
>
>>[!tip]- Expressions
>>On représente souvent des expressions par des arbres dont les feuilles sont les opérandes ![[Cours Arbres 2023-01-09 10.37.13.excalidraw]]
>
>>[!summary]- Partitions d'un entier
>>Le nombre de partitions d'un entier $p$ en au plus $q$ parties
>>```ocaml
>>let rec nb_partitions p q = 
>>if p = 0 then 1
>>else if q = 0 then 0
>>else if q > p then nb_partitions q p
>>else np_partitions (p-q) q + nb_partitions p (q-1)
>>```
>>On peut alors traçer un arbre d'appels

# Définitions

## Arbres Binaires Stictes

On considère un ensemble $\mathcal{F}$ des étiquettes des feuilles et un ensemble $\mathcal{N}$ des étiquettes des noeuds internes. On définit $\mathcal{A(N, F)}$ des arbres binaires stricts comme le plus petit ensemble qui vérifie:
- les feuilles sont des arbres $\mathcal{F} \subset \mathcal{A(N, F)}$
- si $g$ et $d$ sont deux arbres et $x \in \mathcal{N}$, alors $N(x, g, d)\in \mathcal{A(N, F)}$

>[!help]- Qu'est-ce que $N$
>Ici, $N(a,b,c)$ représente
>![[Cours Arbres 2023-01-09 10.55.50.excalidraw|100%]]
>où $b$ et $c$ sont deux arbres

En $\text{OCaml}$, on a:
```ocaml
type ('n, 'f) arbre_bin = 
	| Feuille of 'f
	| Noeud of 'n * ('n, 'f) arbre_bin * ('n, 'f) arbre_bin
```

>[!tip]- Hors Programme Catégorique
>Par la somme des [[Cours Dénombrement et Ensembles Finis#Coéfficients Binomiaux|coéfficients binomiaux]], on peut démontrer
>$$
>A(x) = (2^{n}-1)x
>$$

## Induction structurelle

Dans le cas des arbres binaires, on peut faire une preuve par [[Info/Induction Structurelle|induction structurelle]]:
Soit $P$ prédicat,
 $$
\begin{align}
 &\forall f\in \mathcal{F}, P(f) {\huge \land} \forall g,d\in \mathcal{N}, P(g) ∧ P(d) \implies P(N(x, g, d)) \\
&{\huge \implies} \\
 &\forall a\in \mathcal{A(N, F)}, P(a)
\end{align}
$$

>[!example] Programme pour la hauteur
>```ocaml
>let rec hauteur t = match t with
>| Feuille f -> 0
>| Noeud (x, g, d) -> 1 + max (hauteur g) (hauteur d)
>```

### Arbre Binaire Parfait

Un arbre parfait est:
- Une feuille 
- De la forme $N(x, g, d)$ tel que $g$ et $d$ sont des arbres parfaits de même hauteur

>[!tip] Caractérisation 
>Un arbre est parfait si toutes les feuilles ont la même profondeur
>![[Info/Preuve - Perfection de l'arbre binaire]]

## Arbres binaires non stricts

On considère un ensemble $\mathcal{E}$. L'ensemble $\mathcal{A(E)}$ des arbres binaires non-stricts est défini par:
- $\bot \in \mathcal{A(E)}$
- $g,d \in \mathcal{A(E)} \land x\in \mathcal{E} \implies N(x, g, d) \in \mathcal{A(E)}$

>[!help] Différence avec l'arbre strict
>En d'autres termes, toutes les feuilles sont identiques, d'où $\mathcal{F}= \{ \bot \}$
>On dira alors que les feuilles sont "vides"

Alors l'arité d'un noeud est son nombre d'enfants non-vides

>[!warning] Subtilité
>Si un noeud n'a qu'un seul fils, il faut quand même choisir s'il est placé à gauche ou à droite

## Parcours d'un arbre binaire 

Il faut choisir un ordre dans lequel traverser l'arbre. Au début du parcours, on passe la racine au programme.

Décrivons des parcours de gauche à droite.

### DFS - Parcours en profondeur 

Deux remarques importantes
1. Ce parcours est naturellement récursif
2. Il existe $3$ ordres, les permutations de $\{ g,r,d \}$ avec $g$ avant $d$, on les dit
	1. préfixe
	2. infixe
	3. postfixe

### BFS - Parcours en largeur

On parcourt tous les fils dans l'ordre de profondeur.

### En OCaml 

```ocaml
let rec preorder = function
	| Feuille x -> Printf.printf "%d\n" x
	| Noeud (x, g, d) -> Printf.printf "%d\n" x ; preorder g ; preorder d
```

# Dénombrement 

>[!warning] Il manque un cours ici

## Nombres de Catalan

Il y a $c_{n}$ arbres binaires stricts avec $n$ noeuds internes 


![[Info/Preuve - Arbres Catalan]]

### Formule explicite

1. $(n+2)c_{n+1}=2(2n+1)c_{n}$
2. $c_{n}=\frac{1}{n+1}{2n\choose n}={2n \choose n}-{2n \choose n+1}$

![[Info/Preuve - Nombres Catalan]]

On a $c_{n}\sim \frac{4^{n}}{\sqrt{ \pi }n^{3/2}}$


# Arbres non-binaires (Rose Trees)

```ocaml
type 'a rose_tree = N of 'a * 'a arbre liste
```

$\dots$

En tous points d'une suite commence un unique facteur équilibré

## Transformation en arbre binaire 

LCRS


# Arbres Binaires de recherche

## Détour, Dictionnaires

>[!bug]- Exercice
>Implémenter une fonction `antécédents` qui renvoie un dictionnaire des antécédents de chaque image d'une fonction $f : \textlbrackdbl 0, n \textlbrackdbl \to \text{'}a$
> ```ocaml
>antécédents f = let
> update map x = let
>		y = f x
>	in Map.set y (match Map.get y map with
>		| None      -> [x]
>		| Some (xs) -> (x:xs)) map
> in List.fold_left update Map.empty (List.range 0 n)
> ```

## Définitions 

On travaille avec un ensemble $\mathcal{E}$ d'étiquettes muni d'une relation d'ordre et des arbres binaires non-stricts. Un arbre binaire satisfait la propriété suivante:
$$
\forall N(n,g,d) \in A, n > \text{max}\{ \varphi(g) \cup \varphi(d) \}
$$
avec $\varphi(A)$ l'ensemble des noeuds de $A$ 

> la propriété n'est pas locale

En C, on implémente un arbre binaire comme

```c
...
```

$\dots$

## Complexité

### Recherche

La recherche prend au plus $h+1$ étapes

### Suppression

```ocaml
let rec supprime_max = function
	| V -> failwith "ratio"
	| N (x,g,V) -> x, g
	| N (x,g,d) -> let m, d' = supprime_max d
		in x, N (g,d')

let rec supprime y = function
	| V -> V
	| N (x,g,d) when x < y -> N (x, g, supprime y d)
	| N (x,g,d) when x > y -> N (x, supprime y g, d)
	| N (x,g,d) -> let m,g' = supprime_max g
		in N (m, g', d)
```

## Arbres équilibrés

### Arbres $2-3$
