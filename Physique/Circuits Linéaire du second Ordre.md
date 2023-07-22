#cours #physique #électricité 

Pour le premier ordre, voir [[Circuits Linéaires du premier Ordre en régime transitoire|le chapitre précédent]].

# Oscillations libres du circuit $LC$

## Circuit $LC$
#circuit-lc 

![[Circuits Linéaire du second Ordre - Illustration circuit LC.excalidraw|100%x400]]

## Equation différentielle de l'oscillateur harmonique

$$
\begin{align}
u_{C} + u_{L} &= 0 \\
u_{C} + L \frac{di}{dt} = 0 \\ \\

i = C \frac{du_{C}}{dt} \\
u_{C} + LC \frac{d²u_{C}}{dt²} = 0 \\
\frac{d²u_{C}}{dt²} + \frac{u_{C}}{LC} = 0
\end{align}
$$
On obtient une oscillation harmonique:
$$
u_{C} = A\cos(\omega_{0}t) + B\sin(\omega_{0}t),\quad \omega_{0}=\frac{1}{\sqrt{ LC }}
$$

Ou par formule de déphasage:
$$
u_{C}=X\cos(\omega_{0}t - \phi)
$$
![[Déphasage#Vers la forme factorisée]]

## Conditions initiales

$$
\begin{cases}
u_{C}(0) \text{ obtenue par continuité de } u \text{ en } C \\
\frac{du_{C}(0)}{dt}=\frac{i(0)}{C} \text{ obtenue par continuité de } i \text{ en } L
\end{cases}
$$

donc
$$
\begin{cases}
A = u_{C}(0) \\
B = \frac{1}{\omega_{0}} \frac{du_{C}}{dt}(0)
\end{cases}
$$
> On calcule $u_{C}(0)$ pour $A$ et $\frac{du_{C}}{dt}(0)$ pour $B$

## Aspect Energétique

$$
\begin{align}
uC + LC \frac{d²uC}{dt²} &= 0 \\
u_{C}i + LC + i \frac{d²u_{C}}{dt²} &= 0 \\
Cu_{C} \frac{du_{C}}{dt} + Li \frac{di}{dt} &= 0 \\
\frac{d}{dt}\left( \frac{1}{2} Cu_{C}² \right) + \frac{d}{dt}\left( \frac{1}{2} Li² \right) &= 0 \\
\frac{d}{dt} (Cu_{C}² + Li²) = 0
\end{align}
$$

Donc l'énergie totale du circuit est ==constante==.

# [[Physique/Signal sinusoïdal|Caractéristiques d'un signal sinusoïdal]]

# Circuits linéaires du 2nd ordre

## Circuit $RLC$ en série
#circuit-lc #circuit-rc

![[Circuits Linéaire du second Ordre - Illustration RLC.excalidraw|100%]]

- A $t=0$ on ferme $K$ avec $C$ initialement déchargé
- On applique la loi des mailles
$$
E+u_{L}+u_R-u=0
$$
- De plus on a 

| Bobine                   | $u=Ri$      | Condensateur        |
| ------------------------ | ----------- | ------------------- |
| $u_{L}=-L \frac{di}{dt}$ | $u_{R}=-Ri$ | $i=C \frac{du}{dt}$ |

- On a alors
$$
\begin{align}
E-L \frac{di}{dt} - Ri - u &= 0 \\
LC \frac{d²u}{dt²} + RC \frac{du}{dt} + u &= E \\
\frac{d²u}{dt²} + \frac{R}{L} \frac{du}{dt} +\frac{1}{LC}u &= \frac{1}{LC}E
\end{align}
$$

- On la met sous forme canonique
$$
\frac{d²u}{dt²} + \frac{\omega_{0}}{Q} \frac{du}{dt} + \omega_{0}²u=\omega²E
$$
avec $\omega_{0}² = \frac{1}{LC}$ et $Q=\frac{1}{R}\sqrt{ \frac{L}{C} }$

## Régime libre ou propre

Un régime libre est la solution de cette équation lorsque $E=0$.

## Résolution d'une équation différentielle du second ordre

On cherche à résourdre avec

| $u$       | $u'$       | $u''$       |
| --------- | ---------- | ----------- |
| $Ue^{rt}$ | $Ure^{rt}$ | $Ur²e^{rt}$ |

On a alors

$$
\begin{align}
Ur²e^{rt}+\frac{\omega_{0}}{Q}Ure^{rt}+\omega_{0}²Ue^{rt}&=0 \\
r²+\frac{\omega_{0}}{Q}r+\omega_{0}²&= 0 \\
\Delta=\left( \frac{\omega_{0}}{Q} \right)^{2} - 4\omega_{0}^{2} \\
\end{align}
$$

- $\Delta > 0$ est le régime apériodique
$$
\begin{align}
\frac{1}{Q^{2}} &> 4 \\
Q&< \frac{1}{2} \\
\frac{1}{R}\sqrt{ \frac{L}{C} } &< \frac{1}{2} \\
R &> 2\sqrt{ \frac{L}{C} }
\end{align}
$$
Les solutions sont donc
$$
r_{i} = -\frac{\omega_{0}}{2Q} \pm \omega_{0}\sqrt{ \frac{1}{4Q^{2}}-1 }
$$
Donc la solution est une combinaison linéaire des deux solutions
$$
u(t)=U_{1}e^{r_{1}t} + U_{2}e^{r_{2}t}
$$
On constate que c'est un régime transitoire si r1,r2<0.
ok !

- $\Delta = 0$ est le cas ==critique==
$Q=\frac{1}{2}$ ou $R=2\sqrt{ \frac{L}{C} }$
On a alors une solution double
$$
r=-\frac{2\omega_{0}}{2Q}
$$
donc un seul vecteur pour notre base $e^{rt}$.
![[Parachute|50x50]]
grâce au [[Parachute|parachute]], on en conclut qu'un autre vecteur est de forme
$$
u(t)=t e^{rt}
$$
> On peut vérifier
Donc toute solution est au final de forme
$$
\begin{align}
u(t) &= U_{1}e^{rt} + U_{2}te^{rt} \\
&= (U_2t+U_{1})e^{rt}
\end{align}
$$

- $\Delta < 0$, le cas pseudo-périodique
On a alors $Q > \frac{1}{2}$ et $R < 2\sqrt{ \frac{L}{C} }$
Les deux solutions sont complexes conjuguées
> $j^{2}=-1$
$$
r = -\frac{\omega_{0}}{2Q}\pm \frac{j\omega_{0}}{2Q}\sqrt{ 4Q^{2}-1 }
$$
On nomme $\omega=\frac{\omega_{0}}{2Q}\sqrt{ 4Q^{2}-1 }$ la **pseudo-pulsation**
![[Parachute|50x50]]
On a donc nos deux vecteurs, on peut alors écrire la solution générale
$$
\begin{align}
u(t)&=U_{1}e^{-\omega_{0}t/2Q}e^{j\omega t} + U_{2}e^{-\omega_{0}t/2Q}e^{-j\omega t} \\
&= (U_{1}e^{j\omega t} + U_{2}e^{-j\omega t})e^{-\omega_{0}t/2Q}
\end{align}
$$
Or on a
$$
U_{1}e^{j\omega t} + U_{2}e^{-j\omega t} = (U_{1}+U_{2})\cos\omega t + j(U_{1}+U_{2})\sin\omega t
$$
et $U_{1}=\overline{U_{2}}$ car ![[Parachute|50x50]]
donc
$$
u(t)=U\cos(\omega t+\phi)e^{\frac{-\omega_{0}t}{2Q}}
$$

> les deux caractéristiques sont la période et l'amplitude

## Cas Pseudo-Périodique

Il y a deux temps caractéristiques on peut définir
![[Physique/Période - Fréquence - Pulsation]]
pour ce système.
On a alors
$$
\begin{align}
\omega &= \omega_{0} \sqrt{ 1-\frac{1}{4Q²} } = \frac{2\pi}{T} \\
T &= \frac{4\pi}{\omega_{0}\sqrt{ 4Q²-1 }}
\end{align}
$$
Et le temps caractéristique est
$$
\tau = \frac{2Q}{\omega_{0}}
$$
On peut regarder le décrément logarithmique
![[Physique - Décrément logarithmique]]
Ici, 
$$
\begin{cases}
u(t)&=Ue^{-\omega_{0}t/2Q}\cos(\omega t+\phi) \\
u(t+T)&=Ue^{-\omega(t+T)/2Q}\cos(\omega (t+T)+\phi)
\end{cases}
$$
donc
$$
\delta=\frac{\omega_{0}T}{2Q}=\frac{\pi}{Q\sqrt{ 1-\frac{1}{4Q²} }}
$$
$$
T=\frac{2\pi}{\omega_{0}\sqrt{ 1-\frac{1}{4Q²} }}
$$
## Réponse à un échelon de tension
$$
\frac{d²u}{dt}+\frac{u_{0}}{Q} \frac{du}{dt}+\omega_{0}²u=\omega_{0}²E
$$
avec un échelon
$$
\begin{cases}
E \text{ pour } t<0 \\
E \text{ pour } t>0
\end{cases}
$$

Pour l'équation homogène, voir [[Circuits Linéaire du second Ordre#Résolution d'une équation différentielle du second ordre|le paragraphe précédent]].
On trouve une solution particulière:
$$
u_{p}(t)=E
$$
On a alors:
$$
\begin{cases}
\text{apériodique}&: U_{1}e^{-r_{1}t}+U_{2}e^{-r_{2}t} &+E \\
\text{critique}&: U_{1}e^{t}+U_{2}e^{-\omega_{0}t/2Q} &+E \\
\text{pseudopériodique} &: U(\cos\omega_{0}+\phi)e^{-\omega_{0}t/2Q} &+ E
\end{cases}
$$
Pour trouver les constantes on a besoin de conditions initiales $u(0)$ et $\frac{du}{dt}(0)$ en utilisant les [[Circuits R,L,C - Notes importantes#^da3495|règles de continuité]].

## Aspects énergétiques

$$
\begin{align}
u+L \frac{di}{dt} + Ri &= E \\
ui + Li \frac{di}{dt} + Ri² &= Ei \\ \\
\begin{cases}
i &= C \frac{du}{dt} \\
Cu \frac{du}{dt} + Li \frac{di}{dt} + Ri²
 &= Ei \\ 
\frac{d}{dt}\left( \frac{1}{2}Cu² \right)+\frac{d}{dt}\left( \frac{1}{2}Li² \right) + Ri² &= Ei
\end{cases}
\end{align}
$$

| Quantité                                | Valeur           |
| --------------------------------------- | ---------------- |
| Puissance fournie alimentation          | $Ei$             |
| Puissance diffipée effet Joule dans $R$ | $Ri²$            |
| Energie Stockée dans $C$                | $\frac{1}{2}Cu²$ |
| Energie Stockée dans $L$                | $\frac{1}{2}Li²$ |

[[Circuits Linéaire du second Ordre - Energie Condensateur.excalidraw]]

## Facteur de qualité dans le cas d'un amortissement faible

$\mathcal{E}$ est l'énergie de forme $e^{-ω0t/Q}$ avec l'autre facteur périodique.
$$
\frac{\mathcal{E}(t+T)}{\mathcal{E}(t)}=e^{-\omega_{0}T/Q}
$$
On a alors
$$
\frac{\mathcal{E(t)}-\mathcal{E}(t+T)}{\mathcal{E}(t)}= 1-\frac{\mathcal{E}(t+T)}{\mathcal{E}(t)} = 1-e^{-\omega_{0} T/Q}
$$
On fait un développement limité de l'exponentielle ![[Parachute|100x100]]
$$
e^{x}\approx1+x+o(x)
$$
Donc
$$
\frac{\Delta \mathcal{E}}{\mathcal{E}}\approx\frac{\omega_{0}T}{Q}
$$
Donc
$$
\omega \approx\omega_{0}
$$
Et aussi
$$
Q = \frac{2\pi \mathcal{E}}{\Delta \mathcal{E}}
$$

> Le facteur de qualité est l'inverse de la différence d'énergie pendant une période lors d'un amortissement faible

