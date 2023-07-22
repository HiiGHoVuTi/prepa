---
aliases: [Intégration]
dg-publish: true
order: 19
active: true
---

# Fonctions lipchitziennes, uniformément continues et continues

## Définitions

### Continue

![[Cours Continuité#Continuité]]

### Lipchitzienne

![[Cours Dérivation#Fonction $k-$Lipchitzienne]]

### Uniformément continue

$$
\forall \varepsilon>0,\exists \eta> 0,\forall (x,y)\in I^{2},\quad\left| x-y \right|\leq \eta \implies \left| f(x)-f(y) \right|\leq \varepsilon
$$

>[!warning] Être continue n'est pas suffisant
>Pour $I=\mathbb{R}^{+}$, $f(x)=x^{2}$, alors $f$ n'est pas uniformément continue
>Pour $\varepsilon=1$, avec $x=y+\eta$, $\left| (x+\eta)^{2}-x^{2} \right|\leq \varepsilon$ absurde.

## Relations Intéressantes

### Implications en échelle

$$
\begin{align}
k-\text{lipch} &\text{itzienne} \\ \Downarrow& \\ \text{uniformeme} &\text{nt continue} \\ \Downarrow \\\text{conti}& \text{nue}
\end{align}
$$

![[Maths/Preuve - Implications continuite]]

### Sur un segment (Théorème de Heine)

Soit $f$ continue sur $[a,b]$ un *segment*, alors $f$ est uniformément continue.

![[Maths/Preuve - Continue segment]]

# Subdivision, fonctions en escalier et continues par morceaux

## Subdivision

On appelle subdivision de l'intervalle (segment) $[a,b]$ une famille de réels $(x_{0}\dots x_{n})$ vérifiant
- $x_{0}=a$
- $x_{n}=b$
- la famille est dans l'ordre

On dit que $u$ est plus fine que $v$ si $v\subset u$. 

>[!tip] Remarque
L'union de deux subdivisions est plus fine que les deux d'origine

## Fonctions en escaliers

$f$ est une fonction en escaliers sur $[a,b]$ si et seulement si il existe $u=(x_{0}\dots x_{n})$ une subdivision de $[a,b]$ telle que pour $i\in \textlbrackdbl 0,n-1 \textrbrackdbl$, $f(]x_{i},x_{i+1}[)$ est un singleton.

>[!tip] SEV
>L'ensemble des fonctions en escalier sur un même intervalle sont un sous-espace vectoriel de $\mathbb{R}^{[a,b]}$.

## Fonction continue par morceaux

$f$ est continue par morceaux si et seulement si il existe $u=(x_{0}\dots x_{n})$ une subdivision de $[a,b]$ telle que pour $i\in \textlbrackdbl 0,n-1 \textrbrackdbl$, $f$ est continue sur $]x_{i},x_{i+1}[$, admet une limite finie à droite en $x_{i}$ et à gauche en $x_{i+1}$

>[!tip] SEV
>Sous-espace vectoriel de $\mathbb{R}^{[a,b]}$

## Théorème d'Approximation

Soit $f$ une fonction continue par morceaux sur $[a,b]$, pour tout $\varepsilon>0$ il existe $\varphi$ et $\psi$ escaliers tels que
$$
\varphi\leq f\leq \psi \quad\text{et}\quad \psi-\varphi\leq \varepsilon
$$

![[Maths/Preuve - Théorème d'approximation]]

# Intégrale d'une fonction

## Intégrale d'une fonction en escalier

Soit $f$ escalier et $(x_{0}\dots x_{n})$ une subdivision adaptée
On définit alors l'intégrale de cette fonction en escalier par
$$
\int_{a}^{b} f(t) \, dt =\sum_{i=0}^{n-1} f\left( \frac{x_{i+1}+x_{i}}{2} \right)(x_{i+1}-x_{i})=\sum_{i=0}^{n-1}f(x_{i}+\varepsilon)\Delta x
$$
> on vérifiera que cette valeur est unique, peu importe la subdivision adaptée

### Lemme

Si $f\geq 0$ alors $\int f\geq 0$

#### Corollaire

Si $f \geq g$ alors $\int f\geq \int g$

### Chasles

$$
\int_{[a,c]} f(t) \, dt =\int_{[a,b]} f(t) \, dt  + \int_{[b,c]} f(t) \, dt 
$$

## Intégrale d'une fonction continue par morceaux

### Intégrale

On pose
$$
A=\left\{  \int_{[a,b]} \varphi(t) \, dt \;;\; \varphi \leq f  \right\}\quad B= \left\{  \int_{[a,b]} \psi(t) \, dt\;;\; f \leq \psi   \right\}
$$
avec $\varphi,\psi$ en escaliers.
Alors $A$ est majorée, $B$ minorée, alors $\text{sup}A=\text{inf}B$ et on appelle cette quantité l'intégrale de $f$ sur $[a,b]$ notée
$$
\int_{[a,b]} f(t) \, dt 
$$

![[Maths/Preuve - Intégrale]]

### Propriétés

Forme linéaire et Chasles aussi.
On pose $\int_{a}^{b} f \, dt=-\int_{b}^{a}  f\, dt$.

#### Nullité

$f\geq 0, \int f =0 \iff f=0$ (preuve par contraposée, on pose un petit escalier dessous, $\chi_{[x_{0}-\eta,x_{0}+\eta]} \frac{f\left( x_{0} \right)}{2}$)

### Somme de Riemann

Soient $f$ continue par morceaux sur $[a,b]$, et $S_{n}=\frac{b-a}{n}\sum_{k=0}^{n-1} f\left( a+k \frac{b-a}{n} \right)$, alors
$$
S_{n}\longrightarrow \int_{a}^{b} f(t) \, dt 
$$
et si de plus $f$ est $\mathfrak{k}-$lipchitzienne, alors
$$
S_{n}-\int_{a}^{b} f(t)  \, dt = O\left( \frac{1}{n} \right)
$$

![[Preuve - Somme de Riemann]]

De même pour $S'_{n}=\frac{b-a}{n}\sum_{k=1}^{n} f\left( a+ k\frac{b-a}{n} \right)$, on calcule la différence et montre qu'elle est de $0$.
De même pour $T_{n}=\frac{S_{n}+S'_{n}}{2}$ qu'on appelle méthode des trapèzes qui converge plus vite (en $O\left( \frac{1}{n^{2}} \right)$) si $f\in \mathcal{C}^{2}$ (admis).

# Intégration et Dérivation

## Théorème Fondamental

Soit $f$ continue sur $I$ avec $x_{0} \in I$. 
$$
F(x)=\int ^{x}_{x_{0}}f(t) \, dt 
$$
est *la* primitive de $f$ s'annulant en $x_{0}$

![[Preuve - Théorème fondamental de l'Analyse 2]]

### Corollaire Fondamental

![[Preuve - Théorème fondamental de l'Analyse]]

### Corollaire Chelou

Soient $\alpha,\beta$ dérivables sur $I$, $f$ continue sur $I$ avec 
$$
\varphi(x)=\int_{\alpha(x)}^{\beta(x)}f(t) \, dt 
$$

![[Preuve - Integrale aux Bornes Alpha Beta]]

## Formule de Taylor

$$
f(b)=\sum^{n}_{k=0}f^{(k)}(a) \frac{(b-a)^{k}}{k!} + \int_{a}^{b} \frac{(b-a)^{n}}{n!} f^{(n+1)}(t) \, dt 
$$

![[Maths/Preuve - Formule de Taylor]]


### Corollaire: Inégalité de Taylor-Lagrange

Soit $f$ telle que $| f^{(n+1)} |≤ M$, alors
$$
\left| f(b)-\sum f^{(k)}(a) \frac{(b-a)^{k}}{k!} \right|\leq M \frac{\left| b-a \right|^{n+1}}{(n+1)!}
$$

> preuve par inégalité triangulaire

# Compléments

## Extension de $\mathbb{R}$ dans $\mathbb{C}$

Tout se transfère sauf ce qui dépend de la relation d'ordre.
L'inégalité triangulaire est conservée

## Intégration par parties - le retour !

### Riemann-Lebesgue

Si $f$ est continue,
$$
\int _{a}^{b} f(t)e^{i\lambda t} \, dt \xrightarrow[\lambda \to \infty]{}  0 
$$
Si de plus $f$ est continuement dérivable,
$$
\int _{a}^{b}f(t)e^{i\lambda t} \, dt = O_{\lambda\to \infty }\left( \frac{1}{\lambda} \right) 
$$
![[Preuve - IPP le retour oscillation]]

#### Méthode: Intégration par parties

On utilisera les IPP pour obtenir des comportements asymptotiques.