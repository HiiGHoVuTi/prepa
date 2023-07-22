---
dg-publish: true
---

#maths #analyse #intégrales #cours #review 

# Définitions

## Intégrale

Soit $f$ continue sur $[a,b]$, l'intégrale de $f$ sur cet intervalle notée $\int_{[a,b]} f$ ou bien $\int^b_{a} f(t) \, dt$
est l'aire algébrique entre l'axe des abcisses et la courbe de $f$ sur le segment $[a,b]$.

![[Quelques Résultats de base sur les Intégrales et Primitives 2022-10-19 10.17.25.excalidraw|800x400]]
Par convention on a:
$$
\int^b_{a} f(t) \, dt = -\int^a_{b} f(t) \, dt  
$$

## Primitive

Soit $f$ une fonction continue sur $I$ et $F$ une fonction dérivable sur $I$, on dt que $F$ est une primitive de $f$ ssi $F'=f$ sur $I$.

- Soient $f$ continue sur $I$ et $F_{1}$, $F_2$ deux primitives de $f$ sur $I$, 
$$
\begin{align}
F_{1} - F_{2} &\in \mathbb{K}  \\
(F_{1} - F_{2})' &= 0
\end{align}
$$

- Soit $f$ une fonction continue sur $I$ et $c\in I$, alors
$$
x |\to \int_{c}^x f(t) \, dt 
$$
est la primitive de $f$ sur $I$ s'annulant en $c$

- Corollaire: Soit $f$ continue sur $I=[a,b]$ et $F$ une primitive de $f$ sur $I$
$$
\int_{a}^b f(t) \, dt = F(b) - F(a) 
$$
![[Preuve - Théorème fondamental de l'Analyse]]

- Soient $f$ continue sur $I$, $\alpha$, $\beta$ dérivables sur $J$ avec $\alpha(J) \subset I$, $\beta(J) \subset I$.
	La fonction $\phi$ définie sur $J$ par
$$
\phi(x) = \int_{\alpha(x)}^{\beta(x)} f(t) \, dt 
$$
est dérivable sur $J$ et
$$
\phi'(x) = \beta'(x)f(\beta(x)) - \alpha'(x)f(\alpha(x))
$$
![[Preuve - Integrale aux Bornes Alpha Beta]]

- Soit $f$ une fonction dérivable sur $I$, on dit que $f$ est de classe $\mathcal{C}_{1}$ si $f'$ est continue sur $I$.
> Exemple:
$$
f(x) = \begin{cases}
x^{2}\sin\left( \frac{1}{x} \right) &\text{si }x\neq 0 \\
0 &\text{sinon}
\end{cases}
$$
Ici $f$ est continue, dérivable avec $f'(x) = 2x\sin(x) - \cos\left( \frac{1}{x} \right)$ mais $f'$ pas continue en $0$


## Dans les Complexes
- On généralise la dérivation de $\mathbb{R}$ à $\mathbb{C}$.
	La fonction de $I$ dans $\mathbb{C}$ est dérivable sur $I$ si $\text{Re}\circ f$ et $\text{Im}\circ f$ sont dérivables.
$$
f'(x) = \text{Re(f(x))}' + i\,\text{Im}(f(x))'
$$

# Primitives usuelles et parties

## Primitives usuelles

Grâce aux dérivées usuelles, on a le *beau* tableau suivant:

![[Tableau Dérivées Primitives Usuelles]]

### Dérivée de composée

- Soient $f\in J^I$ et $g\in \mathbb{K}^J$ dérivables, alors $g\circ f$ est dérivable avec
$$
(g \circ f)' = (g'\circ f) \times f'
$$
- Avec $F$ une primitive de $f$, $F\circ u$ est une primitive de $u' \times f\circ u$

> [[Exercice d'Application de l'intégration par parties]]

# Utilisation des nombres complexes

## Linéarisation

- On utilise les formules d'Euler pour les formules de type
$$
\sin^p(x) \cos^q(x)
$$

> On peut parfois s'en passer
> 	$\sin(x)(\cos(x))^{861}$ donne $-\frac{\cos^{862}(x)}{861}$
> $\cos^3(x) = \cos(x) (1-\sin^2(x)) = \cos(x) - \cos(x)\sin^2(x)$ donne $\sin(x)-\frac{\sin^3(x)}{3}$


## Exponentielle Complexes

Lorsqu'on recherche une primitive de
$$
\cos(ax)e^{bx} \text{ ou } \sin(ax) e^{bx}
$$
On passe à l'exponentielle
$$
\begin{align}
\cos(ax)e^{bx} &= \text{Re}(e^{iax}e^{bx}) \\
&= \text{Re}(e^{iax + bx})
\end{align}
$$

![[Exemples d'Intégration par passage à l'exponentielle complexe]]

# Intégration par parties

## Propriété

Soient $u$ et $v$ deux fonction de classe $\mathcal{C}^{1}$ sur $[a,b]$, alors on a

$$
\int^{b}_{a} u'(x)v(x)\, dx  = \Big[u(t)v(t)\Big]^{b}_{a} - \int u(x)v'(x) \, dx 
$$
avec
$$
\Big[f(t)\Big]^{b}_{a} = f(b)-f(a)
$$

> L'intégration par parties sert souvent à simplifier les termes à intégrer ou alors pour des relations de récurrence

## Méthode
[[Preuve - intégration par parties]]

![[Méthode intégration]]

## Proposition

Soit $\phi$ une fonction de classe $\mathcal{C}_{1}$ à valeurs dans $I$, $f$ une fonction continue sur $I$

$$
\int _{a}^{b} f(\phi(t))\phi'(t) \, dt = \int _{\phi (a)}^{\phi(b)} f(x) \, dx  
$$


[[Preuve - Changement de variable d'intégration]]

