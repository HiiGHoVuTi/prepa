#physique #électricité #cours #review

# Régime continu ou variable / permanent ou transitoire
#ac-dc 

## 1) Régime continu ou variable

### Continu
$U$ et $I$ sont constants
![[Circuits Linéaires du 1er Ordre en régime transitoire ContinuIllustration.excalidraw|800x400]]
### Variable
Le cas contraire

### Permanent ou Stationnaire
![[Circuits Linéaires du 1er Ordre en régime transitoire PermanentIllustration.excalidraw|800x400]]
## Régime Transitoire

Un régime transitoire est la transition entre deux régimes permanents

## Echelon de tension ou de courant
#what

## Circuit linéaire

Un circuit linéaire est un circuit composé uniquement de

| Nom               | Grandeur   | $Lettre$ |
| ----------------- | ---------- | ------ |
| Résistor          | Résistance | $R$    |
| Bobine            | Inductance | $L$    |
| Condensateur      | Capacité   | $C$    |
| Source de Tension | Tension    | $E$    |

# Régime transitoire d'un circuit RC
#circuit-rc

![[Circuits R,L,C - Notes importantes#^fb0fce]]

## Equation différentielle
#équation-différentielle 

![[Circuit RC.excalidraw|800X400]]

on écrit l'équation suivante
$$
E = RC\frac{du}{dt} + u
$$
![[Equation Différentielle Premier Ordre]]

### Application

- On résoud l'équation homogène

$$
\begin{align}
\frac{dx_{H}}{dt}(t) + ax_{H}(t) &= 0 \\ \\

\frac{dx_{H}}{dt} &= -ax_{H} \\ \\

\int \frac{dx_{H}}{x_{H}} &= \int -at \, dt  \\ \\

dx &= \lim_{ \Delta t \to 0 } x(t+\Delta t) - x(t) \\ \\

\ln x_H(t) &= -at + K \\ \\

  x_{H}(t) &= e^{-at+K} \\ \\

x_{H}(t) &= Xe^{-at}
\end{align}
$$
- On calcule une solution particulière
#what
$$
\begin{align}
x(0) &= X + \frac{Y}{a} \\
x(t) &= \left( x(0) - \frac{Y}{a} \right)e^{-at} + Y
\end{align}
$$
- Pour notre cas particulier

$$
\begin{align}
E &= RC\frac{du}{dt} + u \\ \\

u(t) &= Ue^{-t/RC} + E
\end{align}
$$
- Avec nos conditions initiales, on détermine que $U + E = 0$
$$
u(t) = E(1- e^{-t/RC})
$$
=> On en déduit le graphe suivant
![[Circuits Linéaires du 1er Ordre en régime transitoire GrapheChargementRC.excalidraw|800x400]]
> Ici, $E$ est la solution particulière et représente le régime permanent. Le régime transitoire est représenté par $-Ee^{-r/RC}$

## Charge et décharge d'un condensateur

```functionplot
---
title: Décharge
xLabel: t
yLabel: u
bounds: [0,5,0,1]
disableZoom: false
grid: false
---
f(x) = exp(-x)
```

```functionplot
---
title: Charge
xLabel: t
yLabel: u
bounds: [0,5,0,1]
disableZoom: false
grid: false
---
f(x) = 1-exp(-x)
```
> Ici le $1$ en odronnées correspond à $\frac{E}{R}$. 

> On définit le "temps caractéristique" du système RC par la valeur $\tau=RC$ qui est homogène à un temps.

> On observe une asymptote en $+\infty$

La tangente à l'origine:
$$
u_{\tan}(t) = \left[ \frac{du}{dt}(t=0) \right]t + u(0)
$$

```functionplot
---
title: Intersection
xLabel: t
yLabel: u
bounds: [0,5,0,1.1]
disableZoom: false
grid: false
---
f(x)=1
g(x)=1-exp(-x)
h(x)=x
```

La tangente à l'origine a une insersection avec l'asymptote pour $t=\tau$.

## Aspects énergétiques

$$
\begin{align}
\frac{du}{dt} \frac{u}{RC} &= \frac{E}{RC} \\ \\

Ri^2 + C\frac{du}{dt}u &= Ei \\ \\

Ri² + \frac{d}{dt}\left( \frac{1}{2}Cu² \right) &= Ei
\end{align}
$$
Voici le bilan des puissances:

| Puissance                | Valeur           |
| ------------------------ | ---------------- |
| Fournie générateur       | $Ei$             |
| Emmagasinée condensateur | $\frac{1}{2}Cu²$ |
| Dissipée (effet Joule)   | $Ri²$            |

# Régime transitoire d'un circuit du $1^{er}$ degré
#circuit-lc

## Equation Différentielle

$$
\begin{align}
\tau &= \frac{L}{R} \\ \\

\frac{di}{dt} + \frac{i}{\tau} &= \frac{E}{L} \\ \\

i(t) &= i_{H}(t) + i_{P}(t) \\ \\

\frac{i_{P}(t)}{\tau} &= \frac{E}{L} \\ \\

i_{P}(t) &= \frac{\tau}{L}E \\ \\

i(t) &= Ie^{-t/\tau} + \frac{E}{R} \\ \\

I &= -\frac{E}{R} \\ \\
i(t) &= \frac{E}{R}(1-e^{-t/\tau})
\end{align}
$$

-  On se place dans des conditions initiales nulles et la continuité pour déterminer $I$ 

## Etablissement et Rupture du Courant
$$
\begin{align}
u(t) &= L\frac{di}{dt} \\ \\

&= \frac{LE}{R} \frac{1}{\tau} e^{-t/\tau} \\ \\

&= Ee^{-t/\tau}
\end{align}
$$

![[Circuits Linéaires du 1er Ordre en régime transitoire CircuitLC.excalidraw|800x400]]

![[Circuits R,L,C - Notes importantes#^f1f659]]

## Aspect Energétique
$$
\begin{align}
L \frac{di}{dt} + Ri &= E \\
Li \frac{di}{dt} + Ri^2 &= Ei \\
\frac{d}{dt} \left( \frac{1}{2} Li^2 \right) + Ri^2 &= Ei
\end{align}
$$
| Puissance                | Valeur           |
| ------------------------ | ---------------- |
| Fournie générateur       | $Ei$             |
| Emmagasinée condensateur | $\frac{1}{2}Li²$ |
| Dissipée (effet Joule)   | $Ri²$            |

### Energie totale
$$
\begin{align}
&\int_{0}^{T}  E \frac{E}{R}(1-e^{-t/\tau}) \, dt \\ \\
= & \frac{E^{2}}{R} (T + \tau(e^{-t/\tau} - 1)) 
\end{align}
$$
### Energie dissipée
$$
\begin{align}
&\int_{0}^T Ri^{2} \, dt \\ \\

=& \int_{0}^T  R \frac{t^{2}}{R^{2}}(1-e^{-t/\tau})^2 \, dt  
\end{align}
$$

