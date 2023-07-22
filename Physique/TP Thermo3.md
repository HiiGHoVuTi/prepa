
Aspects Théoriques
---

1. Le système est isolé donc $Q,W=0$. Donc $\Delta U=0$ soit $\sum_{i} C_{i}(T_{f}-T_{i}^{0})=0$.
2. On a un glaçon de masse $m_{1}$ à température de fusion $T_{fus}=0° \text{ C}=273.15 \text{ K}$ et une masse $m_{2}$ d'eau liquide à température $T_{eau}$. Alors, en appelant $L_{f}$ l'enthalpie massique de fusion de l'eau et $c_{eau}$ la capacité thermique massique de l'eau,

$$
m_{1}L_{f} +m_{1}c_{eau}(T_{f}-T_{fus})+m_{2}c_{eau}(T_{f}-T_{eau})=0
$$
Ainsi

$$
\boxed{L_{f} = c_{eau}(T_{fus}-T_{f})-\frac{m_{2}}{m_{1}}c_{eau}(T_{f}-T_{eau})}
$$

3. On chauffe une masse $m$ d'eau depuis une température $T_{0}$ par une résistance parcourue par un courant d'intensité $I$ soumis à une tension $U$. On a
$$
mc_{eau}(T-T_{0})=UI(t-t_{0})
$$
D'où
$$
\boxed{T=T_{0}+\frac{UI}{mc_{eau}}t}
$$

Mesure de la valeur en eau du calorimètre
---

1. On a $C_{0}$ la capacité thermique du calorimètre et $c$ la capacité thermique massique de l'eau. Ainsi $\alpha=\frac{C_{0}}{c}$ est une grandeur homogène à une masse. C'est la valeur en eau du calorimètre qui indique quelle masse d'eau il faut ajouter au modèle théorique afin de simuler la capacité thermique du calorimètre (pour ne pas avoir à la compter séparément).
2. Protocole
	1. On verse une masse $m_{1}$ d'eau dans le calorimètre, mesurée en la pesant dans le récipient sur la balance allumée et tarée
	2. On note $T_{1}$ la température à l'équilibre, mesurée avec le thermomètre fourni
	3. On ajoute une masse $m_{2}$ d'eau à une température $T_{2}$ (idem)
	4. On attend qu'un nouvel équilibre soit atteint et mesure $T_{f}$ la nouvelle température
 On obtient les mesures suivantes:
 
| $\mathfrak{(}m_{1}\text{ (g)},T_{1} \text{ (°C)}\mathfrak{)}$ | $\mathfrak{(}m_{2}\text{ (g)},T_{2}\text{ (°C)}\mathfrak{)}$ | $T_{f}\text{ (°C)}$ |
| ------------------------------------------------------------- | ------------------------------------------------------------ | ------------------- |
| 149.1, 22.2                                                    | 151, 91.2                                                     | 54.1                |
| 145.8, 20.1                                                    | 101, 81.3                                                     | 45.1                |
| 89.1, 19.9                                                     | 299, 86.2                                                     | 66.1                |
| 137.6, 19.8                                                    | 107.6, 84.3                                                   | 48.4                |
| 115.2, 20.9                                                    | 164.5, 85.9                                                   | 57.8                |

3. D'après la question $\mathfrak{4.1.2.1}$, on a
$$
C_{1}(T_{f}-T_{1})+C_{2}(T_{f}-T_{2})=0
$$
Puis comme $C_{i}=m_{i}c_{eau}$,
$$
m_{1}c_{eau}(T_{f}-T_{1})+m_{2}c_{eau}(T_{f}-T_{2})=0
$$
D'où
$$
T_{f,th}=\frac{m_{1}T_{1}+m_{2}T_{2}}{m_{1}+m_{2}}
$$

On remarque une légère sur-estimation de température par la formule théorique, qui donne en moyenne $2°\text{C}$ de trop (à incertitude de $\pm2°\text{C}$). Les résultats sont les suivants 

| $T_{f,observé}$ | $T_{f,th}$    |
| ---------- | --- |
  | 54.1 | 56.9 |
  | 45.1 | 45.1 |
  | 66.1 | 70.9 |
  | 48.4 | 48.1 |
  | 57.8 | 59.1 |

On a en réalité
$$
m_{1}c_{eau}(T_{f}-T_{1})+m_{2}c_{eau}(T_{f}-T_{2})+C_{cal}(T_{f}-T_{1})=0
$$
d'où
$$
\alpha=\frac{C_{cal}}{c_{eau}}=-m_{1}-m_{2} \frac{T_{f}-T_{2}}{T_{f}-T_{1}}
$$

On peut calculer cette valeur pour chaque donnée du tableau et on obtient $\alpha=30\pm 10\text{ g}$ en ne comptant que les expériences montrant en effet du "surcomptage".
Nos mesures ne semblent ainsi pas concluantes, l'incertitude étant beaucoup trop grande

Capacité thermique massique de l'eau
---

1. On étudie maintenant une masse $m$ d'eau dans le calorimètre à une température $T(t)$. On plonge dans l'eau une résistance chauffante alimentée par un générateur de tension $U=5V$. On insère dans le circuit un ampèremètre afin de déterminer son intensité $I$. On remarque $I$ constante avec $I=4.9 \text{ A}$. On réalise régulièrement des mesures de la température du système. On obtient les résultats suivants avec une masse d'eau de $m=370.2\text{ g}$.

| $t\text{ (s)}$ | $T\text{ (°C)}$ |
| -------------- | --------------- |
| 0              | 18.1            |
| 30             | 18.1            |
| 60             | 18.1            |
| 120            | 18.2            |
| 180            | 18.3            |
| 195            | 18.4            |
| 210            | 18.5            |
| 240            | 18.7            |
| 270            | 18.9            |
| 300            | 19.2            |
| 330            | 19.5            |
| 360            | 19.9            |
| 390            | 20.2            |
| 420            | 20.6            |
| 450            | 20.9            |
| 480            | 21.3            |
| 510            | 21.7            |
| 540            | 22.1            |
| 570            | 22.5            |
| 600            | 22.9            |
| 630            | 23.2            |
| 660            | 23.7            |
| 690            | 24.1            |
| 720            | 24.4            |
| 750            | 24.8            |
| 780            | 25.2            |
| 810            | 25.6            |
| 840            | 26.1            |
| 870            | 26.4            |
| 900            | 26.8            |
| 930            | 27.2            |
| 960            | 27.5            |
| 990            | 27.9            |
| 1020           | 28.3            |
| 1050           | 28.8            |
| 1080           | 29.2            |
| 1110           | 29.5            |
| 1140           | 29.9            |
| 1170           | 30.3            |
| 1200           | 30.7            |
| 1230           | 31.1            |
| 1260           | 31.5            |
| 1290           | 31.9            |
| 1320           | 32.2            |
| 1350           | 33.6            |
| 1380           | 33.1            |
| 1410           | 33.4            |
| 1440           | 33.8            |
| 1470           | 34.2            |
| 1500           | 34.6            |
| 1530           | 34.9            |
| 1560           | 35.3            |
| 1620           | 36.1            |
| 1680           | 36.9            |
| 1740           | 37.6            |
| 1800           | 38.4                |

Voici la courbe de $T(t)$.
![[T(t).png]]

2. On a d'après la question $\mathfrak{4.1.2.3}$, $T=T_{0}+\frac{UI}{mc_{eau}}t$ d'où $C_{eau}=mc_{eau}=\frac{UI}{\mathfrak{p}}$ avec $\mathfrak{p}$ la pente de la régression linéaire, c'est aussi $\frac{UIt}{T-T_{0}}$. On obtient alors $C_{eau}= 1993$ soit $c_{eau}=5.3\pm 0.4 \text{ J.K}^{-1}\text{.g}^{-1}$.

4. On peut considérer avoir obtenu un effet de moyenne avec une seule manipulation car on a effectué plusieurs mesures chacune donnant l'augmentation de température en un écart de temps donné, ainsi la pente obtenue est en quelque sorte la moyenne de ces pentes individuelles.

