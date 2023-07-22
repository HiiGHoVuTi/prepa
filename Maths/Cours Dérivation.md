---
aliases: [Cours Dérivée]
order: 9
---

#maths/cours 

On suppose sans précisions contraires $I$ un intervalle de $\mathbb{R}$ et $f\in \mathbb{R}^{I}$

# Fonction dérivée

## Définition

Soit $a\in I$ on dit que $f$ est dérivable si $\varphi_{a}=\frac{f(x)-f(a)}{x-a}$ admet une limite en $a$ et on appelle dérivée sa limite notée $f'(a)$ ou $\frac{df}{dx}(a)$ ou $Df(a)$. On a
$$
f'(a) = \lim_{ x \to a } \frac{f(x)-f(a)}{x-a} = \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}
$$
On dit que $f$ est dérivable à gauche (resp à droite) si dans la limite on a $h< 0$ (resp $>0$).

>[!example]- Valeur Absolue
>La fonction valeur absolue est dérivable à gauche et à droite mais pas au point en $0$.

Si la fonction est dérivable pour tout point de $I$ on lui associe sa fonction dérivée $f'$ ou $Df$.

## Propriétés

### Droite et Gauche

Soit $a\in I$ pas une borne, les propositions suivantes sont équivalentes
1. $f$ dérivable en $a$
2. $f$ dérivable à gauche et à droite en $a$ et les deux limites sont égales

### Développement limité

Soit $a$ un élément de $I$, les propositions suivantes sont équivalentes 
1. $f$ dérivable en $a$
2. $f$ admet un développement limité d'ordre $1$ en $a$ avec $f(x)=f(a)+f(a)(x-a)+o(x-a)$

![[Maths/Preuve - Développement Limité]]

>[!note]- Corollaire
>On en déduit que si $f$ est dérivable en $a$ alors elle est continue en $a$

En utilisant les propriétés des limites, on retrouve le formulaire de dérivation ([[Cours Espaces Vectoriels|combinaisons linéaires]] et produits).

De plus, il est préférable de ne pas oublier les formules usuelles.
![[Tableau Dérivées Primitives Usuelles]]

### Dérivée de composée

Soient $f\in J^{I}$ et $g\in \mathbb{R}^{J}$ dérivables, alors $g\circ f$ dérivable avec
$$
(g\circ  f)'(x) = (g'\circ  f)(x) \times f'(x)
$$

![[Maths/Preuve - Dérivée Composée]]

### Dérivée de bijection

Soit $f$ dérivable bijective dans l'intervalle $I$ telle que $f'$ ne s'annule pas sur $I$ alors $f^{-1}$ est dérivable avec
$$
(f^{-1})'(x) = \frac{1}{(f' \circ  f^{-1})(x)}
$$
![[Maths/Preuve - Dérivée Réciproque]]

## Dérivées Successives

On définit récursivement les dérivées $n$-ièmes notées $f^{(n)}$ avec $f^{(0)}=f$ et $f^{(n+1)}=f^{(n)'}$

>[!note] Classe
>On dit que la fonction $f$ est de classe $\mathcal{C}^{n}$ si $f$ est $n$ fois dérivable et $f^{(n)}$ est continue.
>On dit que $f$ est de classe $\mathcal{C^{\infty}}$ si pour tout entier $n\in \mathbb{N}$, $f$ est $\mathcal{C^{n}}$.

## Propriétés 

Soient $f,g$ deux fonctions $n$-fois dérivables, alors toute [[Cours Espaces Vectoriels|combinaison linéaire]] l'est aussi.

> de même pour $\mathcal{C}^{n}$

>[!example]- Une fonction dérivable mais pas $\mathcal{C}^{n}$ 
>$$
>f(x) = \begin{cases}
> x^{2}\sin\left( \frac{1}{x} \right) & x\neq 0 \\
> 0 & \text{sinon}
\end{cases}
>$$
>On a bien une dérivée mais est une vraie pathologie pour $x\to 0$
>```functionplot
>---
>title: 
>xLabel: 
>yLabel: 
>bounds: [-1,1,-1.5,1.5]
>disableZoom: false
>grid: false
>---
>f(x) = 2x*sin(1/x)-cos(1/x)
>```


### Formule de [[Leibniz]]

Soient $f,g \in \mathcal{C}^{n}$ (ou juste $n-$fois dérivable ) alors $f\times g \in \mathcal{C}^{n}$ (ou juste $n-$fois dérivable)

$$
(fg)^{(n)} = \sum_{k=0}^{n}{n\choose k} f^{(k)}g^{(n-k)}
$$

>[!note] Newton
>On remarque une grande ressemblance avec [[Introduction aux Structures Algébriques#Sommes et Puissances|le binôme de Newton]], ce qui indique que les fonctions de classe $\mathcal{C}^{n}$ forment un [[Introduction aux Structures Algébriques#Anneau - Définition|anneau]]

![[Maths/Preuve - Formule de Leibniz]]

### Composition

Soient $f$ une fonction de classe $\mathcal{C}^{n}$ de $I$ dans $J$ et $g$ une fonction de classe $\mathcal{C}^{n}$ de $J$ dans $\mathbb{R}$, alors $g \circ f \in \mathcal{C}^{n}$.

![[Maths/Preuve - n-Continuité composée]]

>[!note]- Corollaire 
>Pour $f\in \mathcal{C}^{n}$ ne s'annulant pas on a $\frac{1}{f}\in \mathcal{C}^{n}$.

### Réciproque

Soient $n\geq1$ et $f\in \mathcal{C}^{n}$ bijective telle que $f'$ ne s'annule pas sur $I$ alors $f^{-1}\in \mathcal{C}^{n}$

>[!note]- Hypothèses
>Le caractère bijectif est impliqué par la continuité et la dérivée non-nulle


![[Preuve - n-Continuité réciproque]]

# Taux d'accroissement

Supposons que $I$ est un intervalle de $\mathbb{R}$ de longueur non-nulle.

## Théorème de Rolle

### Défintion

Soit $f$ une fonction définie sur $I$, on dit que $f$ admet un *minimum* (resp *maximum*) **local** en $a$ si $f(x)\geq f(a)$ (resp $\leq$) au voisinage de $a$.

On dit que l'extremum est strict si de plus, $x\neq a \implies f(x)<f(a)$.

### Lemme

Soient $f$ dérivable sur $]a,b[$, et $c\in ]a,b[$ tels que $f$ admet un extremum local en $c$. Alors on a
$$
f'(c) = 0
$$

![[Maths/Preuve - Lemme Dérivée nulle]]

### Théorème de Rolle

Soit $f$ continue sur $[a,b]$ dérivable sur $]a,b[$ telle que $f(a)=f(b)$ alors il existe $c\in ]a,b[$ telle que $f'(c)=0$.

![[Maths/Preuve - Théorème de Rolle]]

## Théorème des accroissements finis et applications

### Théorème des accroissements finis 

Soit $f$ une fonction continue sur $[a,b]$ et dérivable sur $]a,b[$ alors il existe $c\in ]a,b[$ tel que
$$
\frac{f(b)-f(a)}{b-a} = f'(c)
$$

![[Maths/Preuve - Accroissements Finis]]

### Corollaire - Inégalité des accroissements finis  V$\mathfrak{1.}$

Soient $f$ dérivable sur $[a,b]$, $m,M\in \mathbb{R}$ tels que
$$
m \leq f' \leq M
$$
on a alors pour tous $x\neq y$
$$
m \leq \frac{f(y)-f(x)}{y-x}\leq M
$$

### Corollaire - Inégalité des accroissements finis  V$\mathfrak{2.}$

Soient $f$ dérivable et $M\in \mathbb{R}$ tels que
$$
\left| f' \right|\leq M
$$
on a pour tous $x\neq y$
$$
\left| \frac{f(x)-f(y)}{x-y} \right|\leq M
$$

## Fonction $k-$Lipchitzienne

Soit $f$ une fonction définie sur $I$ et $k\in \mathbb{R}_{+}$, on dit que $f$ est **$k-$lipchitzienne** sur $I$ si pour tout $x,y\in I$
$$
\left| f(x)-f(y) \right|\leq k\left| x-y \right|
$$

>[!tip] Fonctions lipchitziennes
>Si la dérivée de $f$ est bornée en valeur absolue par $M$ alors $f$ est $M-$lipchitzienne 
>Si $f$ est $\mathcal{C}^{1}$ sur $I$ , $f$ est lipchitzienne (car $f'(I)$ est un segment).

## Hiérarchie des implications

- Continue 
$\impliedby$
- Lipchitzienne 
~~Dérivable~~

![[Maths/Preuve - Lipchitz Continue]]

>[!warning]- Pas de Réciproque
>Par exemple, $x\mapsto \sqrt{ x }$ est continue mais pas lipchitzienne 
>Preuve en prenant $y=0$

## Variations

Soit $f$ dérivable sur $I$ un intervalle 

- $f'\geq0 \implies f$ *croissante*
- $f'\leq 0 \implies f$ *décroissante*
- $f'=0 \implies f$ *constante*

![[Maths/Preuve - Variations]]

### Monotonie Stricte

Soit $f$ une fonction dérivable sur $I$ telle que $f'$ ne change pas de signe sur $I$ et la fonction $f'$ n'est pas identiquement nulle sur un intervalle de longueur non-nulle, alors la fonction $f$ est *strictement monotone*.

![[Maths/Preuve - Monotonie Stricte]]

## Théorème de la limite de la dérivée 

Soient $f$ une fonction continue sur $[a,b]$ dérivable sur $[a,b]\setminus\{ c \}$ tels que
$$
f'(x)\xrightarrow[x \to c]{} \ell \in \overline{\mathbb{R}}
$$
- Si $\ell \in \{ +\infty, -\infty \}$, $f$ n'est pas dérivable en $c$ et la courbe de $f$ a une tangente verticale en $c$
- Si $\ell \in \mathbb{R}$, $f$ est dérivable en $c$ et $f'$ est continue en $c$ avec $f'(c)=\ell$.

![[Maths/Preuve - Limite de la Dérivée]]

# Retour aux [[Cours études locales et Développements Limités|DLs]]

## Comparaisons locales de fonctions et DLs

>[!warning]- A revoir au cas où
>[[Preuve - Unicité DL]]

### Lemme - Primitive & Négligeabilité

Soit $f$ dérivable sur $I$, $a\in I$, et $n\in \mathbb{N}$,
$$
f'(x) = o((x-a)^{n+1}) \implies f(x) = o((x-a)^{n})
$$

On a donc le corollaire suivant:
![[Cours études locales et Développements Limités#Primitive]]

### Formule de [[Cours études locales et Développements Limités#Formules de Taylor (Young)|Taylor-Young]]

![[Cours études locales et Développements Limités#Formules de Taylor-Young]]

### Exemples de calculs de DL par la méthode des indéterminés

#### Calcul d'un DL de $f=x \mapsto x + e^{x}- 1$

- Montrons d'abord que $f$ admet une réciproque 

- Montrons ensuite que $f^{-1}$ admet un développement limité à tout ordre en tout point 

> Sachant que $f$ est $\mathcal{C^{\infty}}$ *et* $f'$ ne s'annule pas

- Calculons ensuite le DL de $f^{-1}$ à l'ordre $3$ 

> On considérera $f^{-1}(x) = \alpha + \beta x + \gamma x^{2}+\delta x^{3}+o(x^{3})$ et $f\circ f^{-1}$ ou $f^{-1}\circ f$



