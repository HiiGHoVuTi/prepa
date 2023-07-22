---
aliases: [Proba]
dg-publish: true
order: 16
active: true
---

#maths/cours 

# Evénement

## Expérience Aléatoire

Une expérience aléatoire est une expérience pouvant mener à plusieurs résultats, formellement l'ensemble $\Omega$ l'univers ou espace des états
Traditionnellement, un résultat possible (issue ou épreuve) est notée $\omega$.

>[!example]- Quelques Univers
> Pour pile ou face: $\Omega=\{ \text{Pile, Face} \}$
> Pour un dé à $n$ faces: $\Omega=\textlbrackdbl 1,n \textrbrackdbl$

On appelle événement une partie $E\subset\Omega$. On dit que $\omega\in\Omega$ est réalisée si $\omega\in E$.
On dit que $E$ est élémentaire s'il est un singleton.

## Opérations Ensemblistes

Soient $\Omega$ un univers et $A$ un événement. On appelle indicatrice de $A$ notée $\chi_{A}$ la fonction
$$
\chi_{A}(x)=\begin{cases}
1 \text{ si } x\in A \\
0 \text{ sinon}
\end{cases}
$$

- $\chi_{\overline{A}}=1-\chi_{A}$
- $\chi_{A\cap B}=\chi_{A}\chi_{B}$
- $\chi_{A\cap B}=\chi_{A}+\chi_{B}-\chi_{A}\chi_{B}$

On dit que $A$ et $B$ sont incompatibles si $A\cap B=\emptyset$.

## Système Complet d'Evenements

$A=(A_{1}\dots A_{n})$ est un système complet si et seulement si $A$ est une partition de $\Omega$.
- $A_{i}\neq \emptyset$
- $\cap A= \emptyset$
- $\cup A=\Omega$

# Probabilité

## Fonction de probabilité

Soit $\Omega$ un univers, alors $p$ est une probabilité si et seulement si

- $p:\mathcal{P}(\Omega)\to[0,1]$
- $\mathcal{p}(\Omega)=1$
- $\mathcal{p}(A\cup B)=\mathcal{p}(A)+\mathcal{p}(B)$ si $A\cap B=\emptyset$


## Propriétés Calculatoires

- $p(A)=1-p(\overline{A})$
- $p(A\cup B)=p(A)+p(B)-p(A\cap B)$
- $A\subset B\implies p(A)\leq p(B)$

## Probabilités Finies

Une probabilité sur $\Omega$ fini est caractérisé par les probabilités des singletons.

On dit qu'une probabilité finie est uniforme si $p(A)=\frac{\left| A \right|}{\left| \Omega \right|}$.

## Outils de Dénombrement

### Rappels

Soit $E$ un ensemble à $n$ éléments
- Il existe $n^{p}$ $p-$uplets d'éléments de $E$
- Il existe $\frac{n!}{(n-p)!}$ $p-$listes d'éléments de $E$
- Il existe ${n\choose p}=\frac{n!}{(n-p)!p!}$ $p-$combinaisons d'éléments de $E$

# Probabilité Conditionnelle

On appelle probabilité de $A$ sachant $B$ la quantité
$$
P_{B}(A)=P(A\mid B)=\frac{P(A\cap B)}{P(B)}
$$
Cela revient à changer d'univers , et $P_{B}$ est bien une probabilité.

1. $P_{B}(A_{1}\cup A_{2})=P_{B}(A_{1})+P_{B}(A_{2})$ si $A_{1},A_{2}$ incompatibles.
2. Si $P$ uniforme, $P_{B}(A)=\frac{\left| A\cap B \right|}{\left| B \right|}$.

## Probabilités Composées

$$
P(A\cap B)=P_{B}(A)P(B)
$$

puis par récurrence immédiate

$$
P(\cap_{i=0} A_{i})=P(A_{0})\times P_{A_{0}}(A_{1})\times\dots \times P_{\cap^{n-1}A_{i}}(A_{n})
$$

> on montrera bien qu'aucune des probabilités n'est nulle

## Formule des Probabilités Totales

Pour $(A_{0}\dots A_{n})$ une partition de $\Omega$, on a:
$$
P(B)=\sum P_{A_{k}}(B)
$$

![[Maths/Preuve - Probabilité Totale]]

## Formule de Bayes

Pour $B$ de probabilité non-nulle,

$$
P_{B}(A)=\frac{P(A)}{P(B)} P_{A}(B)
$$

$$
P(A_{j}\mid B)=\frac{P(B\mid A_{j})P(A_{j})}{\sum P(B \mid A_{k})P(A_{k})}
$$

# Variables Aléatoires

On appelle variable aléatoire réelle une application $X:\Omega\to \mathbb{R}$.

On notera $(X\in A)$ l'ensemble $X^{-1}(A)$.

## Loi d'une variable aléatoire

Pour $(\Omega,P)$ un espace probabilisé fini,
Soit $X$ une variable aléatoire réelle, on note $X(\Omega)=\{ x_{1}\dots x_{n} \}$ dans l'ordre.

La loi de probabilité de $X$ est:
$$
P_{X}(x_{i})=P(X=x_{i})
$$
Alors $(X(\Omega),P_{X})$ est un espace probabilisé fini.

>[!note] Système complet d'événements canonique
>$(X=x_{k})_{k\in\textlbrackdbl 1,n \textrbrackdbl}$

## Espérance

L'espérance de $X$ notée $E[X]$ est la quantité
$$
E(X)=\sum x_{i}P(X=x_{i})
$$

Si l'espace est probabilisé fini,
$$
E(X)=\sum_{\omega\in\Omega} X(\omega)P(\{ \omega \})
$$

![[Maths/Preuve - Espérence élémentaires]]

### Formules en Vrac

- Si $X$ constant de valeur $k$, $E(X)=k$
- Si $X<Y$ alors $E(X)<E(Y)$
- $E(aX+Y)=aE(X)+E(Y)$
- $E(\chi_{A})=P(A)$

### Théorème de Transfert

$$
E(f(X))=\sum_{x\in X(\Omega)} f(x)P(X=x)
$$

![[Maths/Preuve - Théorème de Transfert]]

## Variance et Ecart-type

La variance est la quantité suivante
$$
V(X)=E((X-E(X))^{2})
$$
L'écart-type est la racine carrée de la variance $\sigma(X)=\sqrt{ V(X) }$.

Aussi, $V(X)=E(X^{2})-2(E(X)X)+E(X^{2})+E(X)^{2}=E(X^{2})-E(X)^{2}$

- $V(aX+b)=a^{2}V(X)$
- $\sigma(aX+b)=\left| a \right|\sigma(X)$
