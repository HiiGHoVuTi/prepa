#physique #exercice #devoir-libre

# Observation de Proxima du Centaure

$$
E \xrightarrow[O_{1}, f_{1}']{\mathcal{L}_{1}} E_{1} \xrightarrow[O_{2},f'_{2}]{\mathcal{L}_{2}} E'
$$


## 1.
![[Physique - DL05 L1.excalidraw|100%]]

On a toutes les données nécessaires pour utiliser la formule de conjugaison de Descartes sur la partie gauche de notre schéma (avec $O=O_{1}$ pour alléger):
$$
\begin{align}
\frac{1}{f_{1}'} &= \frac{1}{\overline{OA_{1}}} - \frac{1}{\overline{OA}} \\
\frac{1}{\overline{OA_{1}}}&=\frac{1}{f_{1}'}-\frac{1}{\overline{OA}} \\ \\
\overline{OA_{1}} &= \frac{1}{\frac{1}{f_{1}'} - \frac{1}{\overline{OA}}} \\
\text{Application numérique,} \\
\overline{OA_{1}}&=\frac{1}{\frac{1}{8} -\frac{1}{3,99\times 10^{13}\times 10^{3}}} \\
\overline{OA_{1}} &= 8 \text{ m}
\end{align}
$$
En effet, un rayon (quasi) à l'infini sera conjugué sur le plan focal image de la lentille.

## 2.
La taille recherchée ici est $B_{1}A_{1}$ et la taille originelle de l'étoile est $BA$
Les triangles $O_{1}AB$ et $O_{1}A_{1}B_{1}$ sont semblables, donc:
$$
\begin{align}
\frac{O_{1}A}{O_{1}A_{1}} &= \frac{BA}{B_{1}A_{1}} \\ \\
\text{donc,} \\
T_{1}=E_{1}A_{1} &= BA× \frac{O_{1}A_{1}}{O_{1}A} \\ \\
\text{d'après la question précédente,} \\

T_{1} &= R \times \frac{1}{D \times \left( \frac{1}{f_{1}'} - \frac{1}{D} \right)} \\
T_{1} &= R \times \frac{1}{\frac{D}{f_{1}'} - 1} \\ \\
T_{1} &= \frac{Rf_{1}'}{D - f_{1}'}
\end{align}
$$


## 3.
D'après la formule de conjugaison de Descartes:

$$
\frac{1}{f_{2}'} = \frac{1}{\overline{O_{2}A'}} -\frac{1}{\overline{O_{2}A_{1}}}
$$
On rappelle qu'ici le grandissement est $\gamma=\frac{\overline{O_{2}A'}}{\overline{O_{2}A_{1}}}$.
On a alors:

$$
\begin{align}
\frac{1}{f_{2}'} &= \frac{1}{\gamma \times \overline{O_{2}A_{1}}} - \frac{1}{\overline{O_{2}A_{1}}}  \\
\frac{1}{f'_{2}} &= \frac{1}{\overline{O_{2}A_{1}}} \left( \frac{1}{\gamma} - 1 \right) \\
\frac{1}{\overline{O_{2}A_{1}}} &= \frac{1}{f_{2}'} \left( \frac{\gamma}{\gamma-1} \right) \\
\overline{O_{2}A_{1}} &= \frac{f_{2}'(\gamma-1)}{\gamma}
\end{align}
$$
Or on connaît la position de $A_{1}$, le grandissement $\gamma=-4$ et la distance focale $f_{2}'$. On peut donc déterminer la distance $\overline{O_{1}O_{2}}$:

$$
\overline{O_{1}O_{2}} = \overline{O_{1}A_{1}} + \overline{A_{1}O_{2}}
$$
Application numérique avec $\gamma=-4$, $f_{2}'=-20$cm:
$$
\overline{O_{1}O_{2}} = 8 - 20\times 10^{-2} \times\frac{5}{4} = 7,8\text{m}
$$


## 4.
![[Physique - DL05 Q4.excalidraw|100%]]
## 5.
Ici il faut calculer la taille de l'image pour voir si elle dépasse la taille d'un cristal. On a déterminé $T_{1}$ plus tôt et on sait que la taille finale $T'$ est $4$ fois plus grande que celle-ci.

$$
T' =\, \mid \gamma\mid T_{1}  = \,\mid \gamma\mid \frac{Rf_{1}'}{D -f_{1}'}
$$
Application numérique:

$$
T' = \frac{4\times 9,81\times 10^{4} \times 10^{3}}{3,99 \times 10^{13} \times 10^{3} - 8} = 9,8\times10^{-9}\text{m}
$$

 On remarque que $T' \ll 10\mu\text{m}$, donc on ne pourra pas voir qu'une image ponctuelle.

## 6.
On commence par calculer la surface de la grille:
$$
S = 24\times 10^{-3} \times 32 \times 10^{-3} = 7,7\times 10^{-4} \text{ m}^{2}
$$
Comme tous les pixels sont  de taille identique, chaque pixel a une surface $\sigma$ de:

$$
\sigma = \frac{S}{10^{6}} = 7,7\times 10^{-10}\text{ m}^{2}
$$
Or un pixel est un carré, donc ses côtés ont une longueur de $\ell=7,7 \times 10^{-10}$ m. 
Cette fois, on remarque $\ell < T'$ avec aucune grandeur négligeable par rapport à l'autre. L'image observée ne sera pas ponctuelle, elle s'étalera sur plusieurs pixels, nombre qu'on peut estimer grossièrement:
$$
n = \left(\frac{T'}{\ell}\right)^{2} = 161
$$
## 7.
![[Physique - DL05 Parallaxe.excalidraw|100%]]

On a placé les triangles rectangles $SO_{1}E$ et $SO_{2}E$. Ces triangles sont droits en $S$ et l'angle en $E$ est $\alpha=\frac{P}{2}$. On nomme la distance entre le Soleil et l'étoile $SE=D$
On a alors:

$$
\begin{align}
\tan\alpha&= \frac{d}{D} \\
D &= \frac{d}{\tan \alpha} \\
D &= \frac{d}{\tan \frac{P}{2}} \\
\text{Application numérique,} \\
D&=\frac{150\times 10^{6}\times 10^{3}}{\tan (1545\times 10^{-3})'} = \frac{150\times 10^{6}}{\tan0.0004°} \\
&= 2\times 10^{16} \text{ m}
\end{align}
$$
On remarque que l'ordre de grandeur est bon avec les données de l'énoncé, malgré une imprécision à $50$% près.

# Fonctionnement d'une lampe au Néon

![[Physique - DL05 Circuit2.excalidraw|100%]]

Ici on raisonne avec K fermé.

## 1.
D'après la loi des mailles ici, avec $u_{R}$ la tension aux bornes de la résistance:

$$
\begin{align}
E&=u_{R}+u \\
E&=Ri+u 
\end{align}
$$

Ici l'intensité aux bornes de la résistance et du condensateur est la même car l'autre branche a une résistance infinie, donc $i=\frac{u}{\infty}=0$.
Or on connaît l'intensité aux bornes du condensateur,

$$
\begin{align}
i &= C\frac{du}{dt} \\ \\

E&=R\left( C \frac{du}{dt} \right)+u \\
E &= RC \frac{du}{dt} + u
\end{align}
$$

## 2.
Il faut ici résoudre l'équation différentielle qu'on a énoncé ci-dessus.

- On commence par résoudre l'équation homogène $\frac{du}{dt} + \frac{u}{RC} = 0$. On remarque que la fonction nulle est une solution. En supposant $u$ jamais nulle, et avec $\alpha=-\frac{1}{RC}$

$$
\begin{align}
\frac{du}{dt} &= \alpha u \\ \\
\text{en réarrangeant,} \\

\frac{\frac{du}{dt}}{u} &= \alpha \\ \\

\text{on cherche une primitive}, \\
\int \frac{du}{dt \times u} \, dt &= \int \alpha \, dt \\
\int \frac{du}{u} &=\int \alpha \, dt \\
 \\
\ln\mid u\mid &= \alpha t+C \\
 u&=Ke^{\alpha t} ,\quad K=\pm e^{C}   
\end{align}
$$

On remarque qu'avec $K\in \mathbb{R}^{*}_{-} \cup \mathbb{R}^{*}_{+} \cup \{ 0 \}=\mathbb{R}$, on a toutes nos solutions potentielles.

En revenant à l'équation différentielle complète, on a une solution particulière $u(t)=E$, on en déduit la solution complète:

$$
u(t) = Ke^{\alpha t} + E
$$
avec $K$ à déterminer grâce aux conditions initiales. On sait en effet que $u(0)=0$.
$$
\begin{align}
u(0) &= 0 \\
Ke^{\alpha \times 0} + E &= 0 \\
K + E &= 0 \\
K &= -E \\ \\
u(t) &=-Ee^{\alpha t} + E \\
&= E (1 - e^{-t/RC})
\end{align}
$$
## 3.
La tension aux bornes de la lampe est $u$. Or $u(t)$ est une expression strictement croissante de $0$ à $E$. Il faut donc $0 \leq E_{a} \leq E$ pour qu'elle s'allume au bout d'un moment.

## 4.
Si la lampe à néon ne s'allume jamais, on peut conserver la fonction précédente pour obtenir la tension.

```functionplot
---
title: Allure de la tension sans Néon
xLabel: t
yLabel: u
bounds: [0,10,0,1]
disableZoom: false
grid: false
---
f(x) = 1-exp(-x)
```

La courbe ci-dessus a une échelle d'abcisses telle que $RC=1$ et d'ordonnées telle que $E=1$.

## 5.
On sait que la lampe s'allume pour $u(t_{0})=E_{a}$, on peut résoudre cette équation pour trouver la temps $t$ qui convient.

$$
\begin{align}
u(t_{0}) &= E_{a} \\
E(1-e^{-t_{0}/RC})&=E_{a} \\
e^{-t_{0}/RC}&=1-\frac{E_{a}}{E} \\
-\frac{t_{0}}{RC}&=\ln\left( 1-\frac{E_{a}}{E} \right) \\
t_{0} &=-RC\ln\left( 1-\frac{E_{a}}{E} \right)
\end{align}
$$
Selon les caractéristiques du circuit on peut calculer le temps au bout duquel la lampe s'allumera. On remarque la cohérence de ce résultat, avec $\frac{E_{a}}{E}<1$ si la lampe s'allume, et $t$ obtenu positif. De plus, $RC$ est homogène à un temps et $\ln\dots$ n'a pas d'unité.

## 6.
Une fois la lampe allumée, on peut considérer qu'elle est une résistance $r$. On a alors le circuit suivant:
![[Physique - DL05 Circuit2Allumé.excalidraw|100%]]

On observe un pont diviseur de tension. D'après la loi des mailles,
$$
\begin{align}
E &= u + u_{R} \\
E &= u + Ri 
\end{align}
$$
Mais maintenant $i$ est la somme des tensions au bord du condensateur et de la résistance $r$.

$$
\begin{align}
E &= u + R\left( \frac{u}{r} + C \frac{du}{dt} \right) \\
E &= u \left( 1 + \frac{R}{r} \right) + RC \frac{du}{dt}
\end{align}
$$
> On remarque que pour r=∞, on retrouve l'équation précédente.

## 7.

On cherche désormais à résoudre cette équation différentielle, et on le fait de manière très similaire, à la différence près de la constante $\alpha$.

$$
u\left( 1+\frac{R}{r} \right) + RC \frac{du}{dt} = 0 \iff \frac{du}{dt} = -u\left( \frac{1}{RC} + \frac{1}{rC} \right)
$$
donc $\alpha=-\frac{1}{RC} - \frac{1}{rC}$

On choisit alors cette valeur de $\alpha$ et on raisonne de même pour obtenir qu'une fois la lampe allumée, 

$$
u(t) = Ke^{t/RC + t/rC} + E
$$
Or à l'instant $t_{0}$ le moment où la lampe s'allume, $u=E_{a}$. On peut donc déterminer $K$. On réutilise $\alpha$ pour alléger la notation.

$$
\begin{align}
u(t_{0}) = Ke^{\alpha t_{0}} + E &= E_{a} \\ \\

K\exp\left( RC\ln\left( 1-\frac{E_{a}}{E} \right) \times \left( \frac{1}{RC} + \frac{1}{rC} \right) \right) +E &= E_{a} \\
K \exp\left( -\ln\left( 1-\frac{E_{a}}{E} \right) \times \left( 1+\frac{R}{r} \right) \right) &= E_{a} - E \\
K\left( 1-\frac{E_{a}}{E} \right)^{1+R/r} &= E_{a} - E\\
K &= \frac{E_{a} - E}{(1-\frac{E_{a}}{E})^{1+R/r}}
\end{align}
$$
> On remarque que pour $r=\infty$, on a bien $K=-E$ 

On en déduit donc une expression de $u$

$$
u(t) = \frac{E_{a}-E}{\left( 1-\frac{E_{a}}{E} \right)^{1+R/r}} e^{-t/RC-t/rC} + E
$$

## 8.

Pour que la lampe s'éteigne il faut $u < E_{e}$. A l'instant $t_{a}$, la tension est de $E_{a}$. De plus la fonction $u$ est croissante car $K$ est négatif. Enfin, sa limite lorsque $t\to +\infty$ est $E$. On en déduit que $E_{a} \leq u < E$. La lampe ne peut alors s'éteindre que si $E_{e}$ est comprise dans cet intervalle.

## 9.

```functionplot
---
title: Allure de la tension avec Néon
xLabel: t
yLabel: u
bounds: [0.5,10,0,1]
disableZoom: false
grid: false
---
f(x) = 1-exp(-x)
```
Si la lampe reste allumée, c'est comme si on ajoutait simplement une résistance à notre circuit à partir d'un moment.

## 10.
On cherche $t_{1}$ tel que $u(t_{1})=E_{e}$ et $t_{1}>t_{0}$. La nature croissante de la fonction $u$ garantit la deuxième condition, car on a dit précédemment que $E_{e}>E_{a}$ si on veut que la lampe puisse s'éteindre.

$$
\begin{align}
u(t_{1}) &= E_{e} \\
\frac{E_{a}-E}{\left( 1-\frac{E_{a}}{E} \right)^{1+R/r}}e^{-t(1/RC +1/rC)} + E &= E_{a}
\end{align}
$$
Nommons la constante multiplicative de l'exponentielle $\omega$ et de la variable $\tau$ de sorte qu'on résolve l'équation suivante
$$
\begin{align}
\omega e^{-t_{1}\tau} + E &= E_{a} \\
\omega e^{-t_{1}\tau} &= E_{a} - E \\
e^{-t_{1}\tau} &= \frac{E_{a} - E}{\omega} \\
t_{1} &= -\frac{1}{\tau}\ln\left( \frac{E_{a}-E}{\omega} \right) \\
t_{1} &= -\frac{rRC}{r + R}\ln\left( \left( 1-\frac{E_{a}}{E} \right)^{1+R/r} \right)
\end{align}
$$

## 11.
==TODO==

# Simulation par la méthode d'Euler

## 1.
```haskell
uniforme (a,b) n = let h = (b - a) / n 
	in (h, [a, a+h .. b])

euler
	:: (Double -> Double -> Double) -- ^ F(y,t)
	-> (Double, Double) -- ^ [a,b]
	-> Double -- ^ n
	-> ([Double], [Double])
euler f (a,b) n y0 = 
	(intervalle, scanl recur y0 (tail intervalle))
	where
		(intervalle, h) = uniforme (a,b) n
		recur yk tk = yk + h * f yk tk
```


## 2.

On rappelle l'équation différentielle en question

$$
\begin{align}
E &= RC \frac{du}{dt} + u \\
\frac{du}{dt} &= \frac{- u + E}{RC} \\
\frac{du}{dt} &= -u + 1
\end{align}
$$
On en déduit une expression de $F$:

$$
\begin{align}
\frac{du}{dt} &= F(u, t) \\
F(u, t) &= -u + 1
\end{align}
$$
Pour $n$ points, on écrit alors la fonction suivante pour afficher le nuage de points correspondant à la charge du condensateur pendant $7$ secondes.

```haskell
f u t = 1 - u

chargeEuler :: Double -> String -> Matplotlib
chargeEuler n c 
	= scatter xs ys 
	@@ [o2 "marker" "+", o2 "color" c]
	where
		(xs, ys) = euler f (0, 7) n 0
```

On affiche le résultat de ce programme

```haskell
file "test1.png" (chargeEuler 100 "blue")
```

## 3.

On programme rapidement la fonction de référence
```haskell
chergeCondensateurF t = 1 - exp (- t)

chargeCondensateur :: String -> Matplotlib
chargeCondensateur c 
	= lineF (fst (uniforme (0,7) 100)) 
			chargeCondensateurF 
	@@ [o2 "color" c]
```

Et on superpose plusieurs versions, avec $5$ et $25$ points respectivement.

```haskell
file "test2.png" 
	$ chargeEuler 5 "red"
	% chargeEuler 25 "orange"
	% chargeCondensateur "blue"
```

On observe qu'avec peu de points d'Euler, l'approximation "dépasse" la courbe à chaque fois.

## 4.

On programme une fonction créneau
```haskell
creneau :: Double -> Double -> Double -> Double -> Double
creneau f e em t = em + coef * e
	where
		coef = 2 * (floor (2 * t * f) `mod` 2) - 1 
		ampl = e - em

creneauExo :: Double -> Double
creneauExo = creneau 50 1 0.5
```


## 5.
On modifie simplement la fonction qu'on donne au programme selon la nouvelle équation différentielle du système. On note $\mathcal{U}$ le créneau qui dépend du temps.

$$
\begin{align}
E &= RC \frac{du}{dt} + u + \mathcal{U} \\
\frac{du}{dt} &= \frac{E - u - \mathcal{U}}{RC} 
\end{align}
$$
En rappelant $E=1$ et $RC=1$, on a

$$
F(y,t) = 1-y-\mathcal{U}(t)
$$

```haskell
euler (\u t -> 1 - u - creneauExo t) (0,7) 100 (creneauExo 0)
```

## 6.
On ajuste les valeurs du programme pour changer $RC$ et on obtient les courbes suivantes

