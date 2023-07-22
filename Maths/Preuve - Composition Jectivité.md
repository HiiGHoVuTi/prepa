---
dg-publish: true
---

## Injectivité

On suppose $f\in F^E$ et $g\in G^F$ toutes deux injectives.
Supposons $x,x'\in E$ tels que $g\circ f (x) = g \circ f (x')$.
Par définition de la composition, $g(f(x)) = g(f(x'))$.
Comme $g$ est injective, $f(x) = f(x')$.
Comme $f$ est injective, $x = x'$.
=> $g\circ f$ est injective.

## Surjectivité

On suppose $f\in F^E$ et $g\in G^F$ toutes deux surjectives.
Soit $y\in G$. Montrons que $y$ admet un antécédent par $g\circ f$.
Or $g$ surjective donc il existe $x\in F$ tel que $g(x)=y$.
De plus $f$ surjective donc il  existe $z \in E$ tel que $f(z) =x$.
Alors $g\circ f(z) = y$.
=> $g\circ f$ est surjective.