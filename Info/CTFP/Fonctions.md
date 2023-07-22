---
dg-publish: true
---

#category-theory 

# Intro

Dans cette leçon, on va étudier $\mathbf{Ens}$.
> $\mathbf{Ens}$ et $\mathcal{Hask}$ se comportent de manière quasiment identiques, on peut donc les étudier de manière interchangeable pour le moment.

- Une fonction est dite "partielle" si elle n'est pas définie pour toutes les valeurs de son ensemble de départ.
- Une fonction est dite "pure" si elle peut être mémoïsée (càd stockée entièrement en mémoire de manière fixe)
> `isUppercase` est pure, `rollDice` ne l'est pas

On n'étudiera que les fonctions pures pour le moment, et on les choisit comme morphismes dans $\mathbf{Ens}$.

# Relations et Fonctions

Une relation $R_{\Gamma}$ entre $A$ et $B$ est définie par $\Gamma \subset A \times B$. On a
$$
xR_{\Gamma}y \iff (x,y) \in \Gamma
$$
Une relation est une fonction si et seulement si:
- $\forall x\in A, \exists! (x,y) \in \Gamma$

Une fonction $f$ est alors $\{ (x, f(x)) \,\big|\, x\in A \}$.
On remarque qu'une fonction est asymétrique, elle a une direction avec $\text{Dom}(f)=A$, $\text{Cod}(f)=B$.

Une fonction $f$ est inversible d'inverse $g$ si et seulement si:
- $\text{Dom}(f) = \text{Cod(g)}$
- $\text{Cod}(f) = \text{Dom}(g)$
- $f \circ g = \text{id} = g \circ f$

> attention, les deux $\text{id}$ ne sont pas les mêmes, dans une catégorie on aura à préciser $\text{id}_{A}$ par exemple

Une fonction inversible est appelée une bijection.

> pour des ensembles finis $A$ et $B$, l'existence d'une bijection implique $\mid A\mid \,=\, \mid B\mid$.

Certains cas de non-bijection:
- Ecrasement d'information
		$f(x)=f(y), x\neq y$
- Image incomplète
		$\exists y \in B, \not\exists x\in A, f(x)=y$

> une non-bijection "oublie" de l'information ou modélise:
> oubli: `isOdd`, `getAge`
> modèle: `toString`

Si une fonction n'écrase pas d'information, elle est "injective".
Si une fonction a une image complète, elle est "surjective".
Dans $\mathbf{Ens}$, injection et surjection en même temps impliquent bijection. Ce n'est pas le cas pour toute catégorie (il y a des cas pathologiques).

# Retour aux catégories

Un morphisme inversible est appelé un ==isomorphisme==. C'est un cas général de bijection.

Exprimons une injection et une surjection:
- **Monomorphisme**/morphisme monique (injection) noté $A \xhookrightarrow[]{f} B$
	$\forall g_{1},g_{2}, \quad f\circ g_{1} = f \circ g_{2} \iff g_{1}=g_{2}$

- **Epimorphisme**/morphisme épique (surjection) noté $A \xtwoheadrightarrow[]{f} B$
	$\forall g_{1},g_{2},\quad g_{1}\circ f = g_{2}\circ f \iff g_{1}=g_{2}$

> chez Bourbaki (pas de $CT$), les termes étaient synonymes de injection et surjection (racine latine vs racine grecque).
