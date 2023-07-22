
Etude Statique
---

1. On étudie le système $\{ \text{barre} \}$ dans le référentiel terrestre supposé galliléen. Les forces s'appliquant sont la tension du fil, le couple de torsion. On néglige les frottements de la liaison et de l'air. On étudie le système à l'équilibre, soit $a=v=0$. Par le théorème du moment cinétique, $\mathcal{M}(\vec{T}_{1})+\mathcal{M}(\vec{T}_{2})-C\theta=0$. En considérant la poulie parfaite, $T_{1}=T_{2}=mg$. Avec le bras de levier égal à $\ell \cos \theta$, on a:
$$
2mg\ell \cos \theta - C\theta=0 \implies \boxed{ C=2mg\ell \frac{\cos \theta}{\theta}}
$$
2. Protocole:
	1. On accroche les masses égales ($m$) au bout de chaque fil passé dans les poulies
	2. On attend que le système soit à l'équilibre
	3. On mesure alors l'angle $\theta$ entre la position initiale (sans masses) et à l'équilibre (avec masses)
	On obtient les mesures ci-dessous:
 
| Masse de chaque côté $m\text{ (g)}$ | Angle $\theta \text{ (deg)}$ |
| ----------------------------------- | ---------------------------- |
| 2                                   | 3                            |
| 5                                   | 10                           |
| 7                                   | 14                           |
| 10                                  | 19                           |
| 12                                  | 21                           |
| 15                                  | 26                           |
| 17                                  | 28                           |

On mesure $\ell=9\text{ cm}$.
3.  On effectue le calcul de $C$ pour chaque donnée de masse, puis calcule la moyenne et incertitude pour obtenir $C=5.4\times 10^{-2} \pm 6\times 10^{-3} \text{ kg.m².s}^{-2}\text{.rad}^{-1}$

La fonction $\theta(m)$
![[theta(m).png]]

Etude Dynamique
---

1. Par le théorème du moment cinétique appliqué à un solide en rotation autour d'un axe (axe $\Delta$ le long du fil de torsion), on a $J_{\Delta}\ddot{\theta}=-C\theta$ d'où l'équation différentielle
$$
J_{\Delta}\ddot{\theta} + C\theta = 0
$$
On identifie alors $\omega_{0}=\sqrt{ \frac{C}{J_{\Delta}} }$ donc $T_{0}=2\pi \sqrt{ \frac{J_{\Delta}}{C} }$.
Or on a $J_{\Delta}=J_{0}+2m\ell^{2}$ donc $T_{0}=2\pi \sqrt{ \frac{J_{0}+2m\ell^{2}}{C} }$ et $\boxed{T_{0}^{2}=\frac{4\pi^{2}(J_{0}+2m\ell^{2})}{C}}$.
2. Protocole:
	1. On place les masses à une distance $\ell$ donnée du fil de torsion
	2. On tourne la barre de $60°$ par rapport à sa position d'équilibre (avec masses)
	3. On lache la barre sans vitesse initiale et on déclenche le chronomètre simultanément
	4. On compte cinq oscillations et on arrête le chronomètre ensuite
	5. On divise le temps obtenu par $5$ pour obtenir la pseudo-période $T_{0}$
	On obtient les données suivantes:
 
| Distance attache masses - centre $\ell \text{ (cm)}$ | Pseudo Période $T_{0} \text{ (s)}$ |
| ---------------------------------- | ------------------------------ |
| 9                                  | 1.72                           |
| 8                                  | 1.53                           |
| 7                                  | 1.39                           |
| 6                                  | 1.23                           |
| 5                                  | 1.09                           |
| 4                                  | 0.91                           |
| 3                                  | 0.79                           |
| 2                                  | 0.66                           |
| 2                                  | 0.69                           |
| 2                                  | 0.67                           |
| 2                                  | 0.67                           |
| 2                                  | 0.71                           |
| 3                                  | 0.81                           |
| 3                                  | 0.77                           |
| 3                                  | 0.79                           |
| 3                                  | 0.81                           |
| 4                                  | 0.95                           |
| 4                                  | 0.93                           |
| 4                                  | 0.93                           |
| 4                                  | 0.93                           |
| 5                                  | 1.09                           |
| 5                                  | 1.07                           |
| 5                                  | 1.07                           |
| 5                                  | 1.07                           |
| 6                                  | 1.21                           |
| 6                                  | 1.25                           |
| 6                                  | 1.21                           |
| 6                                  | 1.24                           |
| 7                                  | 1.37                           |
| 7                                  | 1.40                           |
| 7                                  | 1.39                           |
| 7                                  | 1.37                           |
| 8                                  | 1.58                           |
| 8                                  | 1.56                           |
| 8                                  | 1.57                           |
| 8                                  | 1.51                           |
| 9                                  | 1.72                           |
| 9                                  | 1.73                           |
| 9                                  | 1.68                           |
| 9                                  | 1.68                           |

On peut alors tracer la courbe $T_{0}^{2}(\ell^{2})$.
![[t02(l2).png]]

3. Dans les courbes précédentes, la pente est de $\mathfrak{p}=4\pi^{2}\frac{2m}{C}$, alors on a
$$
m = \frac{C\mathfrak{p}}{8\pi^{2}}
$$
Cela est cohérent avec la mesure expérimentale de $162\text{ g}$ réalisée avec la balance préalablement allumée et tarée.