#maths #cours #review 

# Négligeabilité, domination et équivalence

Dans cette partie, on suppose les fonctions définies sur un intervalle $]a,b[$ (avec $a,b \in \overline{\mathbb{R}}$) et $c \in ]a,b[\cup \{ a,b \}$.

## Définitions

1. La fonction $f$ est négligeable par rapport à $g$ au voisinage de $c$
$$
f(x)=\mathcal{o}_{x \to c}(g(x)) \iff \frac{f(x)}{g(x)} \xrightarrow[x \to c]{} 0
$$
2. On dit que $f$ est dominée par $g$ au voisinage de $c$
$$
f(x) = \mathcal{O}_{x \to c}(g(x)) \iff B_{i}\leq \frac{f(x)}{g(x)} \leq B_{s}
$$
3. La fonction $f$ est équivalente à la fonction $g$ au voisinage de $c$ 
$$
f \sim_{x \to c} g (x) \iff \frac{f(x)}{g(x)} \xrightarrow[x \to c]{} 1
$$

> On remarque que l'équivalence implique la domination mutuelle

> On remarque que si $f$ est négligeable elle est dominée

## Négligeabilités de référence

Soient $α,β∈\mathbb{R}$, $\alpha < \beta$

1. $x^{\alpha} = o_{x\to \infty}(x^{\beta})$
2. $x^{\beta}=o_{x \to 0}(x^{\alpha})$

Soient $\gamma, \delta \in \mathbb{R}_{+}^{*}$

3. $(\ln x)^{\gamma}=o_{x\to \infty}(x^{\delta})$
4. $x^{\gamma} = o_{x\to \infty}(e^{\delta x})$
5. $(\ln x)^{\gamma} = o_{x\to 0}\left( \frac{1}{x^{\delta}} \right)$

## Equivalences de référence

1. $\ln(1+x) \sim_{x\to 0} x$
2. $\sin(x) \sim_{x \to 0} x$
3. $e^{x}-1 \sim_{x \to 0} x$
4. $\cos(x) - 1 \sim_{x \to 0} -\frac{1}{2} x^{2}$
5. $\cosh(x) \sim_{x \to \infty} \frac{e^{x}}{2}$
6. $\sinh(x) \sim_{x \to \infty} \frac{e^{x}}{2}$
7. $\tan(x) \sim_{x \to 0} x$
8. $\sinh(x) \sim_{x \to 0} x$
9. $\tanh(x) \sim_{x \to 0} x$
10. $\tanh(x) \sim_{x \to \infty} 1$

Preuves: par taux de variations en $0$, en factorisant pour l'infini, sinon:
$\frac{\cos(x)-1}{x^{^{2}}} \xrightarrow[x \to 0]{} 1$

> $f(x) \xrightarrow[x \to c]{} \ell \in \mathbb{R}^{*}_{+} \implies f(x) \sim_{x \to c} \ell$

## Reformulations et propriétés

### Lemme - négligeabilité

Les propositions suivantes sont équivalentes

1. $f(x) = o_{x\to c}(g(x))$
2. Il existe $\epsilon$ une fonction définie au voisinage de $c$ telle que
$$
f(x) = g(x) \epsilon(x), \;\; \epsilon(x) \xrightarrow[x \to c]{} 0
$$

![[Maths/Preuve - Comparaisons Locales - Lemme1]]

## Lemme - équivalences


Toutes les propositions suivantes sont équivalentes

1. $f(x) \sim_{x \to c} g(x)$
2. $f = ag$ et $a \xrightarrow[x\to c]{} 1$
3. $f(x) - g(x) = o_{x\to c}(g(x))$

![[Maths/Preuve - Comparaisons Locales - Lemme 2]]

## Lemme - Règles opératoires

1. $f(x) = o(h(x))$ et $g(x)=o(h(x))$, alors pour $j$ une combinaison linéaire finie de $f$ et $g$, $j = o(h(x))$
2. $f(x)=o(h(x))$ et $g(x)=\mathcal{O}(h(x))$ alors pour $j$ une combinaison linéaire finie de $f$ et $g$,  $j(x) = \mathcal{O(h(x))}$
3. $f(x)=o(g(x))$ alors $f(x)+g(x) \sim g(x)$
4. $f(x)\sim g(x)$ et $h(x)=o(g(x))$ alors $h(x)=o(f(x))$

![[Preuve - Comparaisons Locales - Lemme3]]

[[Comparaisons locales de fonctions et Développements Limités - Lemmes ex.excalidraw|Exemples]]

## Equivalents et calcul de limites

### Lemme - Limites 

Soient $f,g,h,t$ quatre fonctions définies au voisinage de $c$

1. $f(x) \sim h(x) \land g(x) \sim t(x) \implies f(x)g(x) \sim h(x)t(x)$
2. $f(x)\sim g(x) \land f(x) \xrightarrow[x\to c]{} \ell \in \overline{\mathbb{R}} \implies g(x) \xrightarrow[x\to c]{} \ell$

![[Preuve - Comparaisons Locales - Lemme4]]

[[Comparaisons locales de fonctions et Développements Limités - Limite par equiv.excalidraw|Exemple]]

> LES SOMMATIONS D'EQUIVALENTS SONT ==INTERDITES==
> Au voisinnage de 0,
> $1+x \sim 1+2x$ et $-1-2x \sim -1 +x$, mais $−x≁3x$

> LES COMPOSITIONS D'EQUIVALENTS SONT ==INTERDITES==
> Au voisinnage de $0$,
> $1+x \sim 1+2x$ mais $\ln(1+x) \not \sim \ln(1+2x)$ car $2x \not \sim x$

[[Comparaisons locales de fonctions et Développements Limités Exercice.excalidraw]]

# Développement Limité

Dans ce paragraphe, les fonctions sont définies sur $]a, b[$ avec $0 \in ]a,b[$

## Définition

On dit que $f$ admet un développement limité d'ordre $n \in \mathbb{N}$ en $0$ si et seulement si il existe une séquence $a_{0}, a_{1}, a_{2}, \,\dots,a_{n}$ tels que
$$
f(x) = \sum_{k=0}^{n}a_{k}x^{k} + o_{x\to 0}(x^{n})
$$
> La partie polynômiale est dite "régulière"

- Pour $n=0$, si $f(x)=a_{0} + o(1)$ alors $f$ admet une limite $a_{0}$ en $0$
- Pour $n=1$, si $f(x)=a_{0}+a_{1}x+o(x)$, alors $f$ est dérivable en $0$ avec $f'(0)=a_{1}$

On peut aussi chercher un DL en $c \in ]a,b[$ avec la fonction $g(x)=f(x-c)$ donc
$$
f(x) = a_{0} + a_{1}(x-c)+\dots+a_{n}(x-c)^{n} + o((x-c)^{n})
$$
> On peut poser $g(h)=f(c+h)$ avec $h=x-c$ et on étudie $g$ au viosinnage de $0$.

## Unicité

> si et seulement si existence

Si $f$ admet un DL-$n$ en $0$, la partie régulière est unique.

![[Maths/Preuve - Unicité DL]]

## Forme normalisée

Soit $f(x)=a_{0}+\dots a_{n}x^{n}+o(x^{n})$

Soit $j$ le plus petit entier tel que $a_{j}\neq 0$, on a 
$$
f(x) = x^{j}(a_{j}+a_{j+1}+\dots + a_{n-j}x^{n-j}+o(x^{n-j}))
$$

## Formules de Taylor-Young

Soit $f$ une fonction $n-$fois dérivable sur $]a,b[$ alors $f$ admet un DL$-n$ en $0$.

$$
f(x)=\sum_{k=0}^{n} f^{(k)}(0) \times \frac{x^{k}}{k!} + o(x^{n})
$$
> la $n-$dérivabilité est suffisante mais pas nécessaire

![[Preuve - Taylor-Young]]


## DLs de référence

| $f(x)$           | Partie régulière DL                     |
| ---------------- | --------------------------------------- |
| $\frac{1}{1+x}$  | $\sum (-1)^{k}x^{k}$                    |
| $\frac{1}{1-x}$  | $\sum x^{k}$                            |
| $(1+x)^{\alpha}$ | $\sum{\alpha \choose k}x^{k}$           |
| $e^{x}$          | $\sum \frac{x^{k}}{k!}$                 |
| $\cosh(x)$       | $\sum \frac{x^{2k}}{2k!}$               |
| $\sinh(x)$       | $\sum \frac{x^{2k+1}}{(2k+1)!}$         |
| $\cos(x)$        | $\sum \frac{(-1)^{k}x^{2k}}{2k!}$       |
| $\sin(x)$        | $\sum \frac{(-1)^{k}x^{2k+1}}{(2k+1)!}$ |
| $\ln(1+x)$       | $\sum \frac{(-1)^{k}x^{k+1}}{k}$                                      |


## Cas d'équivalence

Soit $f$ définie sur $]a, b[$ et $0 \in ]a,b[$, 
$$
f'(0) \text{ existe} \iff f \text{ admet un DL}_{1}(0)
$$

![[Preuve - DL Equivalence]]

## Propriétés Opératoires

### Troncature

Si $f$ admet un DL$-n$, et $m \leq n$
$$
\begin{align}
f(x)&=a_{0}+a_{1}x+\dots +a_{n}x^{n}+o(x^{n}) \\
&= a_{0}+a_{1}x+\dots+a_{m}x^{m} + o(x^{m}) 
\end{align}
$$

![[Preuve - DL troncatures]]

### Combinaisons Linéaires

Si $f$ et $g$ admettent des DL$-n$ et $\alpha,\beta \in \mathbb{R}$,
$$
\begin{align}
f(x)&=\sum a_{k}x^{k} + o(x^{n}) \\
g(x) &= \sum b_{k}x^{k}+o(x^{n}) \\
\implies \\
\alpha f(x)+\beta g(x) &= \sum (\alpha a_{k} + \beta b_{k})x^{k} + o(x^{n})
\end{align}
$$

![[Preuve - DL Combinaisons Linéaires]]

[[Comparaisons locales de fonctions et Développements Limités Exercice Somme.excalidraw|Exemple]]

### Equivalence

Si $f$ admet un DL$-n$ avec partie régulière non nulle,
$$
f(x) \sim a_{p}x^{p}
$$
avec $p$ le plus petit entier tel que $a_{p}$ non nul

![[Preuve - Equivalence DL]]

[[Comparaisons locales de fonctions et Développements Limités Exercice Equiv.excalidraw|Application]]

![[Maths/DLs et équivalences en physique]]

### Lemme de parité

Si $f$ admet un DL$-n$
$$
f(x)=a_{0}+\dots+a_{n}x^{n}
$$
- si $f$ est paire, $a_{2k+1}=0$
- si $f$ est impaire $a_{2k}=0$

![[Maths/Preuve - Lemme parité]]

[[Comparaisons locales de fonctions et Développements Limités Exercice DL Eq.excalidraw|Exercice]]

### Produits

Soient $f$ et $g$ deux fonctions admettant des DL$-n$ en $0$.
$$
\begin{align}
f(x)&=\sum a_{k}x^{k} + o(x^{n}) \\
g(x)&= \sum b_{k}x^{k}+o(x^{n})
\end{align}
$$
On a alors:
$$
g\times f(x) = \sum_{k=0}^{n} \left( \sum_{\ell=0}^{k} a_{\ell}b_{k-\ell} \right)x^{k} + o(x^{n})
$$

> Dans la pratique on multiplie les parties régulières en mettant à la poubelle les degrés élevés

![[Maths/Preuve - Multiplication DL]]

[[Comparaisons locales de fonctions et Développements Limités Ex DL Multiplication.excalidraw|Exemple]]

### Division par $x$

Soit $f$ une fonction admettant un DL$-n$ avec $n \geq 1$,
$$
f(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}
$$
Si $a_{0}=0$ alors 
$$
g(x)=\begin{cases}
\frac{f(x)}{x}  & \text{si } x \neq 0 \\
a_{1}  & \text{sinon}
\end{cases}
$$
admet un DL$-(n-1)$ tel que
$$
g(x)=a_{1}x+\dots+a_{n}x^{n-1}+o(x^{n-1})
$$

![[Maths/Preuve - Division DL]]
[[Comparaisons locales de fonctions et Développements Limités Sinc.excalidraw|Exercice]]

### Composition

Soient $f,g$ admettant des DL$-n$ avec $g(0)=0$
$$
\begin{align}
f(x)&=a_{0}+a_{1}x+\dots+a_{n}x^{n} +o(x^{n}) \\
g(x)&=b_{1}x+\dots+b_{n}x^{n} + o(x^{n})
\end{align}
$$
alors $f \circ g$ admet un DL$-n$ obtenu en composant les parties régulières.

![[Preuve - Composition DL]]


[[Comparaisons locales de fonctions et Développements Limités Composition.excalidraw|Exercices]]

> Corollaire, le DL$-3$ de $\tan$ est 
$$
\begin{align}
\tan(x) &= \frac{\sin(x)}{\cos(x)} = \left( x-\frac{x^{3}}{6} \right)\left( 1+\frac{x^{2}}{2} \right) + o(x^{3}) \\
&= x + \frac{x^{3}}{3} + o(x^{3})
\end{align}
$$

### Primitive

Soit $f$ une fonction qui admet un DL-$n$
$$
f(x)=a_{0}+\dots +a_{n}x^{n}
$$
et $F$ un primitive de $f$
Alors $F$ admet un DL$-(n+1)$
$$
F(x)=F(0)+a_{0}x+\frac{a_{1}x^{2}}{2}+\frac{a_{2}x^{3}}{3}+\dots+\frac{a_{n}}{n+1}x^{n+1} + o(x^{n+1})
$$
![[Maths/Preuve - Primitive de DL]]

[[Comparaisons locales de fonctions et Développements Limités Exemples Primitives.excalidraw|Exemples]]

### DL de $\arctan$

$$
\arctan'(x) = \frac{1}{1+x^{2}}= \sum(-1)^{k}(x^{2})^{k}+o(x^{2n})
$$
Par primitive, 
$$
\arctan(x) = \sum(-1)^{k} \frac{x^{2k+1}}{2k+1} + o(x^{2n+1})
$$

### DL de $\tan$

$$
\tan(x)  \sim x
$$
donc
$$
\tan(x) = x + o(x)
$$
or
$$
\tan'(x) = 1+\tan(x)^{2}
$$
et
$$
\tan(x) = x(1+o(1))
$$
donc
$$
\tan ^{2}(x) = x^{2}(1+o(1)) = x^{2}+o(x^{2})
$$
ainsi
$$
\tan'(x) = 1+x^{2}+o(x^{2})
$$
par primitive
$$
\tan(x) = x + \frac{x^{3}}{3} + o(x^{3})
$$
on itère pour obtenir
$$
\tan(x)=x\left( 1+\frac{x^{2}}{2}+o(x^{2}) \right)
$$
d'où
$$
\tan ^{2}(x)= x^{2} \left( 1 + \frac{2x^{2}}{3} + o(x^{2}) \right) = x^{2}+\frac{2x^{4}}{3} + o(x^{4})
$$
donc
$$
\tan'(x) = 1+x^{2}+\frac{2}{3}x^{4}
$$
puis par primitive
$$
\tan (x) = x + \frac{x^{3}}{3} + \frac{2}{15}x^{5}+o(x^{5})
$$

[[Comparaisons locales de fonctions et Développements Limités Exercice DL Factorisation par x.excalidraw|Exercice]]

# Applications des DL


## Etude de fonctions en un point fini

Soient un entier $m\geq 2$ et $f$ une fonction admettant un DL$-m(0)$ de la forme
$$
f(x) = a_{0}+a_{1}x+a_{m}x^{m}+o(x^{m})
$$
alors la courbe de $f$ admet une tangente en $0$ d'équation
$$
y = a_{0} + a_{1}x
$$
et l'entier $m$ et le signe de $a_{m}$ donnent la position de la courbe par rapport à la tangente

[[Comparaisons locales de fonctions et Développements Limités Explication.excalidraw|Exemples]]
[[Comparaisons locales de fonctions et Développements Limités comparer la position de courbes.excalidraw|Exercice]]

## Comportement à $+\infty$

Un DL$-n(+\infty)$ s'exprime de $x^{n}$ à $x^{p}$
$$
f(x) = a_{n}x^{n} + a_{n-1}x^{n-1} + \dots + a_{p}x^{p} + o(x^{p})
$$


[[Comparaisons locales de fonctions et Développements Limités Exercice infini.excalidraw|Exemples]]

### Classifications des branches infinies

Soit $f$ définie au voisinage de $+\infty$

- La courbe de $f$ admet une droite asymptote en $+\infty$ 
$\iff$ 
$f(x)=a_{1}x+a_{0}+o(1)$

> si $a_{1}\neq 0$ on a $f(x) \sim a_{1}x$

### Limite $\frac{g(x)}{x}$

Soit $g(x) \to \pm\infty$

Si $\frac{g(x)}{x}$ admet une limite $\ell$ dans $\overline{\mathbb{R}}$

1.  $\ell \in \mathbb{R}^{*}$
On a $g(x) \sim \ell x$
donc la courbe de $g$ admet une direction asymptotique $y=\ell x$
On regarde alors $g(x)-\ell x$
- $g(x)-\ell x \to \alpha \in \mathbb{R}$
on a une droite asymptote
- sinon
pas de droite asymptote

2. $\ell = 0$
direction asymptotique $y=0$

3. $\ell = \pm \infty$
branche asymptote $x=0$

