---
dg-publish: true
order: 4
---
#info/cours 

# Abstraction

Soit $E$ un ensemble isomorphe à une partie de $\mathbb{N}$. On souhaite travailler avec une relation d'équivalence sur $E$ pour le partionner. On besoin de:
- définir une partition sur $E$
- indiquer une relation entre éléments
- trouver un représentant *canonique* pour une classe d'équivalence donnée

En `OCaml` ans un fichier `.mli`
```ocaml
type partition
val create : int -> partition
val union : partition -> int -> int -> partition
val find : partition -> int -> int
```

En `C`, dans un fichier `.h`
```c
typedef struct partition_s partition;
partition* create(int n);
void union(partition* p, int a, int b);
int find(partition* p, int a);
```

On a alors abstrait la structure de données. On parle alors de type abstrait de données. Pour compiler le programme il faut lui fournir une implémentation concrète de ces méthodes.

![[Structures de données 2022-11-07 10.53.02.excalidraw|100%]]

> Les fichiers d'interface ont souvent complétés avec de la documentation

```ocaml
val length : 'a list -> int
(** Return the length (number of elements) of the given list **)
```

## Mutable ou persistant

Une structure de données est dite fonctionnelle ou persistante si elle ne peut pas être modifiée en place ; dans le cas contraire, elle est dite impérative ou mutable.
- Les structures impératives ont une efficacité $\geq$
- Les structures fonctionnelles sont plus correctes et moins risquées

# Listes et Vecteurs

Une liste `OCaml`, 

| Opération | Type                       | Effet                                       | Complexité |
| --------- | -------------------------- | ------------------------------------------- | ---------- |
| `[]`      | `'a list`                  | liste vide                                  | $\mathcal{O}(1)$           | 
| `cons`    | `'a -> 'a list -> 'a list` | ajoute une tête de liste                    | $\mathcal{O}(1)$           |
| `tail`    | !`'a list -> 'a list`       | renvoie la liste  privée du premier élément | $\mathcal{O}(1)$           |
| `head`    |! `'a list -> 'a`            | renvoie le premier élément                  | $\mathcal{O}(1)$           |

Un vecteur `C`,

| Opération                    | Effet                                                     | Complexité |
| ---------------------------- | --------------------------------------------------------- | ---------- |
| `t* create(int n, t x)`      | création d'un vecteur de taille $n$, toutes valeurs à $x$ | $\mathcal{O}(n)$           |
| `t get(t* v, int i)`         | renvoie le $i$-ème élément de $v$                         |  $\mathcal{O}(1)$          |
| `void set(t* v, int i, t x)` | modifie la $i$-ème valeur de $v$ avec $x$                 | $\mathcal{O}(1)$           |

# Pile

## Fonctionnelle


| Opération | Type                          | Effet                                   | Complexité       |
| --------- | ----------------------------- | --------------------------------------- | ---------------- |
| `empty`   | `'a stack`                    | pile vide                               | $\mathcal{O}(1)$ |
| `push`    | `'a -> 'a stack -> 'a stack`  | ajoute au sommet de la pile             | $\mathcal{O}(1)$ |
| `pop`       | !`'a stack -> ('a, 'a stack)` | sépare le sommet de la pile et le reste | $\mathcal{O}(1)$ |

## Impérative
```c
struct stack_s {
	int capacity;
	int size;
	int* data;
}
typedef struct stack_s stack;
```


| Opération                        | Effet                                  | Complexité       |
| -------------------------------- | -------------------------------------- | ---------------- |
| `stack* create(int s)`           | réserve `s` cases mémoire pour la pile | $\mathcal{O}(1)$ |
| `void push(stack* s, A a)`       | ajoute un élément à la pile            | $\mathcal{O}(1)$ |
| `A pop(stack* s)`                | renvoie le sommet de la pile           | $\mathcal{O}(1)$ |
| $\dots$ et opérations de tableau | $\dots$                                | $\dots$          |

```c
int pop(stack* s){
	-- s->size; 
	return s[size];
}
```


# Files

## Abstraite

| Opération        | Type                       | Effet                                | Complexité |
| ---------------- | -------------------------- | ------------------------------------ | ---------- |
| `empty`          | `Queue a`                  | file vide                            | $\mathcal{O}(1)$           |
| `push`/`enqueue` | `a -> Endo (Queue a)`      | ajoute au sommet de la file          |      $\mathcal{O}(1)$      |
| `pop`            | !`Queue a -> (a, Queue a)` | sépare le bas de la file et le reste | $\mathcal{O}(1)$           |


Les interfaces des langages sont identiques.

## OCaml

On utilise deux listes:
- une liste entrante
- une liste sortante

```ocaml
(* todo *)
```

L'intérêt est que la complexité est amortie

#### Démo:
Le potentiel d'une file $f=(e,s)$ est $\phi(f)=2|e|$. On mesure la complexité par le nombre d'utilisations de $(::)$.
On note $\mathcal{C}_{op}(f)$ le coût de $op$ sur $f$ et $f'$ la file obtenue. 
On donne une majoration de $\mathfrak{V}(f) = C_{op}(f) + \phi(f') - \phi(f)$.

- Pour l'extraction:
$$
\begin{cases}
\begin{cases}
\mathcal{C}_{ex}(f) &= 1 \\
\phi(f') &= \phi(f) 
\end{cases} & \text{ si } f \text{ non vide} \\

\begin{cases}
\mathcal{C}_{ex}(f) &= \phi(f)+1 \\
\phi(f') &= 0
\end{cases} & \text{ sinon}
\end{cases}
$$
Donc $\mathfrak{V}(f) = 1 = \mathcal{O}(1)$


- Pour l'insertion
$$
\begin{cases}
\mathcal{C}_{in}(f) &= 1 \\
\phi(f') &= \phi (f) + 2
\end{cases}
$$

donc $\mathfrak{V}(f) = 3 = \mathcal{O}(1)$

On cherche alors $\mathcal{C}_{tot}(f)$:
$$
\begin{align}
\mathcal{C}_{tot}(t) &= \phi(f_{n+1}) - \phi(f_{0}) + \sum^{n}_{i=0} \mathcal{C_{op_{i}}}(f_{i}) +\phi(f_{i+1})- \phi(f_{i}) \\
&= \mathcal{O}(n) + \sum^{n}_{i+1} \mathfrak{V}(f_{i}) = \mathcal{O}(n) + \sum_{i=0}^{n}\mathcal{O}(n) \\
&= \mathcal{O}(n)
\end{align}
$$

## C

```c
struct queue_s {
	int capacity;
	int size;
	int exit;
	int* data;
}
typedef struct queue_s queue;
```
