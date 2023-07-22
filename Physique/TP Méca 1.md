---
dg-publish: false
---

# $1\mathfrak{.1}$ Etude d'une chute libre

1. Fait
![[Petanque-pointage.PNG]]
2. Fait
3. L'abcisse (coordonnée en $x$) est constante au fil du temps.
4. Voici le graphe
![[petanque-yt.PNG|100%]]
Vu l'allure de la courbe, une fonction semblant convenir serait de la forme:
$$
y(t) = at^{2}+bt + h
$$
avec $h$ la hauteur initiale, $a$ négatif.

5. On considère qu'à partir du lâcher la seule force s'appliquant à la boule est son poids, on a alors:
$$
m \vec{a} = m\vec{g}
$$
où $\vec{g}$ est un vecteur de norme $g$ le long de l'axe des ordonnées vers le bas.
On a alors par intégration successive:
$$
\begin{align}
\ddot{y} &= -g  \\
\dot{y} &= -gt \text{ car la vitesse initiale est nulle} \\
y &= -gt^{2} + h \text{ avec h la hauteur initiale}
\end{align}
$$

6. La fonction obtenue est de la bonne forme, et l'ordonnée à l'origine et le signe du coefficient dominant correspondent.
7. Fait
8. Voici le graphique expérimental de $\dot{y}(t)$
![[Petanque-vt.PNG]]
9. Non, à cause des imprécisions de mesure surtout au début, d'où l'approximation par la droite.
10. Une droite d'équation $ax+b$ avec $a$ négatif et $b$ faible pourrait convenir.
11. Le graphique convient tout à fait à l'équation $\dot{y}(t) = -gt$ qu'on avait prévue, car $9,45 \approx g$ (on peut expliquer le coefficient $b$ par un lâcher imparfait).
12. On propose un modèle quadratique, et on obtient le graphe suivants 
![[petanque-vy.PNG]]
14. D'après ce graphique on obtient $g\approx9,61$ en lisant le coefficient $a$ de notre modélisation.
15. On recommence l'étude avec la bille de polystyrène, et on obtient les graphiques suivants:
	- Pointage
	![[Poly-pointage.PNG]]
	- $y(t)$
	![[Poly-yt.PNG]]
	- $\dot{y}(t)$ 
	![[Poly-vt.PNG]]
	- $\dot{y}(y)$ 
	![[Poly-vy.PNG]]

15. Les résultats obtenus pour la boule de polystyrène sont beaucoup moins cohérents avec le modèle théorique qui considère qu'aucune autre force ne s'applique. La vitesse semble se stabiliser avec le temps une fois atteint une certaine vitesse finale. On peut penser que c'est à cause de frottements de l'air qui augmentent avec la vitesse de la boule, jusqu'à la compenser.

# $1.\mathfrak{2}$ Etude d'une chute dans un fluide

1. Fait
![[Bille-Pointage.PNG]]
 > Il y a quelques erreurs de pointage qui se répercuteront clairement plus tard lors de la modélisation 
 
 2. Fait 
 3. Voici le graphe obtenu
 ![[Bille-vt.PNG]]
> l'erreur se remarque à la fin du mouvement avec une courbe absurde

4. On observe une phase d'accélération forte suivi d'une vitesse constante, probablement due au fluide 
5. La vitesse limite est de $0,3\text{m.s}^{-1}$ d'après la courbe, en ignorant les fluctuations dues aux mesures
6. Le mouvement est alors rectiligne (vertical) uniforme car la vitesse est constante 
7. Le bilan des forces nous indique cette fois que la somme des forces est:
$$
\begin{align}
\sum \vec{F} &= \vec{P} - kv^{\alpha}\vec{v}  \\
\implies m \vec{a} &= \vec{P} - kv^{\alpha}\vec{ v}
\end{align} 
$$
Tous les vecteurs sont colinéaires, on s'intéresse alors à leurs normes:
$$
\begin{align}
m\ddot{y} &= mg - k\dot{y}^{\alpha}\dot{y} \\
\ddot{y} &= g - \frac{k\dot{y}^{\alpha+1}}{m} \\ \\
\end{align}
$$
8. Dans la première phase de mouvement la force de frottement est négligeable car la vitesse est faible (elle est nulle au départ).
9. On sait que la variation de vitesse $\ddot{y}$ est nulle, on a alors:
$$
g = \frac{k}{m}\dot{y}^{\alpha+1}
$$
10. Pour $\alpha=0$ et donc $\dot{y}^{\alpha+1}=\dot{y}$, on obtient l'expression suivante de la vitesse limite:
$$
\dot{y} = g\times\frac{m}{k}
$$
Cela semble raisonnable, et confirme que les objets plus lourds tombent plus vite dans les fluides.
11. On résoud la même équation pour $\dot{y}^{\alpha+1}=\dot{y}^{2}$:
$$
\begin{align}
g &= \frac{k}{m} \dot{y}^{2} \\
\dot{y}^{2} &= g \times \frac{m}{k} \\
\dot{y} &= \sqrt{ g \times \frac{m}{k} }
\end{align}
$$
> on garde la racine positive car la vitesse est positive 

12. On aurait pu effectuer une modélisation et laisser $k$ et $\alpha$ comme paramètres libres. On aurait alors pu obtenir une valeur pour $\alpha$ qui aurait concordé avec les données expérimentales. Nous avons manqué de temps.

# $1.\mathfrak{3}$ Etude d'un même mouvement dans plusieurs référentiels

1. Fait
![[Velo-velo-pointage.PNG]]
![[Velo-Balle-Pointage.PNG]]
2. Les données modélisées nous donnent une vitesse quasi-constante en $x$ et quasi-nulle en $y$ pour le vélo. On conclut qu'il suit une trajectoire rectiligne uniforme.

> Nous avons manqué de temps pour la fin des manipulations

