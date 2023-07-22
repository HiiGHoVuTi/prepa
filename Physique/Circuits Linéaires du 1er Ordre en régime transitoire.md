#physique #électricité #cours 

# Régime continu ou variable / permanent ou transitoire
#ac/dc 

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

## Equation différentielle
#équation-différentielle 

![[Circuits Linéaires du 1er Ordre en régime transitoire CircuitRC.excalidraw|800X400]]

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

\int \frac{dx_{H}}{x_{H}} \, dx &= \int -at \, dt  \\ \\

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
