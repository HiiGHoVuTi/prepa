---
dg-publish: true
---

#category-theory 

Dans cette leçon nous commençons à aborder des notions importantes: les $n$-cellules (foncteurs, transformations naturelles).

# Motivation

En $CT$ certaines notions généralisent des idées très abstraites voire non-mathématiques *à priori*.
- [[Objets Terminaux et Initiaux#Construction Universelle|Construction Universelle]]: "meilleure représentation de X", "le X idéal"
	parmi tous les candidats, un seul est parfait et représente l'*essence* du concept de X

- Catégorie: "structure", "relations", "composabilité", "compatibilité"

- Foncteurs: "un motif", "pattern-recognition", "conservation de structure"
	lors des constructions universelles, on a été flou sur la manière dont on cherche le motif depuis notre diagramme dans notre catégorie donnée. En réalité, on choisit un foncteur de $\mathcal{D}$ vers $\mathcal{C}$, et la définition du foncteur garantit que la structure du motif sera conservée

# Concept

Considérons une petite catégorie $\mathcal{C}$. On veut que le foncteur $F$ appliqué à $\mathcal{C}$ donne une autre catégorie $\mathcal{D}$. 
Comme $\mathcal{C}$ est petite, ses objets forment un ensemble, alors $F$ contient une fonction qui à chaque objet $a$ de $\mathcal{C}$ associe un objet $Fa$ de $\mathcal{D}$.
De plus, on veut que $F$ "conserve la structure" de $\mathcal{C}$. Il faut donc que $F$ traduise les morphismes de $\mathcal{C}$ dans $\mathcal{D}$.
Pour tout morphisme $a \xrightarrow[]{f} b$ dans $\mathcal{C}$, on a alors $Fa\xrightarrow[]{Ff} Fb$. 
$F$ contient donc également une fonction pour tous $a$, $b$ de forme $(a\to b) \to (Fa \to Fb)$.

![[Foncteurs - Illustration Mapping.excalidraw|100%]]
De plus, il faut que la composition soit conservée, donc
$$
Fg \circ Ff = F(g\circ f)
$$

![[Foncteurs 2022-11-03 11.51.38.excalidraw|100%x300]]
Ainsi que l'identité:

$$
F\text{id}_{a} = \text{id}_{Fa}
$$

# Définition

Un **foncteur** de $\mathcal{C}$ dans $\mathcal{D}$:
- A tout objet $a$ associe un objet $Fa$
- A tout morphisme $f$ associe un morphisme $Ff$
- $F\text{id}_{a} = \text{id}_{Fa}$
- $Fg \circ Ff = F(g\circ f)$

![[Foncteurs Illustration Finale.excalidraw|100%]]

Un foncteur induit donc une fonction pour chaque paire $a$, $b$
$$
F_{a,b} : \mathcal{C}(a,b) \to \mathcal{D}(Fa, Fb)
$$
Si cette fonction est:
- surjective, le foncteur est **plein**
- injective, le foncteur est **fidèle**
- bijective, le foncteur est **pleinement fidèle**

> ici on ne parle pas d'objets, juste des ensembles de morphismes entre chaque objet

Un foncteur $F:\mathcal{C}\to \mathcal{C}$ est appelé **endofoncteur**.

# Exemples

## Foncteur Unité

Comme on a vu pour "choisir un élément" avec un morphisme $\mathcal{1} \to a$, on peut "choisir un objet" avec un morphisme $\mathbb{1} \to \mathcal{C}$.

> $\mathbb{1}$ est l'objet terminal dans $\mathbf{Cat}$

## Foncteur Constant

De manière similaire, pour chaque objet $c$ de $\mathcal{D}$ on peut créer un foncteur constant $\Delta_{c}$ tel que:
 - $\Delta _c (a) =c$
 - $\Delta_{c}(f) = \text{id}_{c}$
 
> Ce foncteur est très important et sera utilisé souvent pour les constructions universelles

 ## En programmation

Ici, on s'intéresse aux endofoncteurs dans $\mathcal{Hask}$.

> en `haskell` un endofoncteur est appelé `Functor`

```haskell
class Functor f where
	fmap :: (a -> b) -> (f a -> f b)
```

En clair, un constructeur de type est un `Functor` si et seulement si il définit aussi la convertions de fonctions.

### `Maybe a`

```haskell
data Maybe a = Nothing | Just a 
```

> on rappelle que ceci est équivalent à $a + 1$

Pour tout objet $a$, on a déjà un objet $\texttt{Maybe}(a)$ grâce au constructeur de type. Il ne nous manque plus que la convertion de fonctions, pour tout $f:a\to b$, un $\texttt{Maybe} f : \texttt{Maybe}(a) \to \texttt{Maybe}(b)$.
C'est l'instance `Functor`

```haskell
instance Functor Maybe where
	fmap :: (a -> b) -> (Maybe a -> Maybe b)
	fmap f (Just a) = Just (f a)
	fmap f Nothing  = Nothing 
```

On constate que cette définiton respecte les lois des foncteurs.

> La raison pour laquelle on est forcés à utiliser `Nothing` dans la dernière ligne provient de ce qu'on appelle les "conditions de naturalité" qu'on reverra dans la leçon sur les Transformations Naturelles.
> Ceci est vrai en haskell mais pas en général, et rien n'empêcherait notre foncteur de se comporter différemment pour chaque paire $a$, $b$, avec `fmap f Nothing = Just 0` uniquement pour `b ~ Int`.

