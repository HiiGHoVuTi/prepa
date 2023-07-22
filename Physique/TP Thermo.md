---
dg-publish: true
---

Mesure de $\gamma$ par la méthode de Rückhardt
---

1. Une transformation adiabatique est une transformation sans échange thermique avec l'extérieur.
   On peut le faire de deux manières, soit en réalisant la mesure assez vite soit avec un milieu suffisamment isolé.
2. Les hypothèses de la loi de Laplace sont:
	1. Gaz parfait
	2. Transformation adiabatique 
	3. Gaz quasi-stationnaire
3. On étudie le système "bille" dans le référentiel du laboratoire supposé Galiléen (temps court) et les forces s'appliquant sont:
	1. Le poids $m\vec{g}=-mg\vec{u_{z}}$
	2. La pression atmosphérique $-P_{atm}S\vec{u}_{z}$
	3. La pression de l'air intérieur $PS\vec{u_{z}}$
	On applique le principe fondamental de la dynamique
	$$
	m\ddot{z}=PS-P_{atm}S-mg
$$
En particulier à l'équilibre on a $\ddot{z}=0$ donc
$$
P_{e}=P_{atm}+\frac{mg}{S}
$$
4. On rappelle la loi de Laplace, $PV^{\gamma}$ constante. Donc en particulier,
$$
PV^{\gamma}=P_{e}V_{e}^{\gamma}
$$
D'où
$$
P=P_{e} \left(\frac{V_{e}}{V}\right)^{\gamma}=P_{e}\left( \frac{V-Sz}{V} \right)^{\gamma}=P_{e}\left( 1-\frac{Sz}{V} \right)^{\gamma}
$$
Puis, comme $Sz\ll V_{e}$
$$
= P_{e}\left( 1-\frac{Sz}{V_{e}} \right)^{\gamma}=P_{e}\left( 1-\gamma\frac{Sz}{V_{e}} \right)
$$
5. On en déduit
$$
m\ddot{z}=PS-P_{atm}S-mg
$$
soit
$$
m\ddot{z}=SP_{e}\left( 1-\gamma  \frac{Sz}{V_{e}} \right)-P_{atm}S-mg
$$
enfin
$$
\ddot{z}+\frac{P_{e}\gamma S^{2}}{V_{e}m} z = \frac{P_{e}-P_{atm}}{m}S-g
$$
6. On résoud l'équation juste établie en reconnaissant l'oscillateur harmonique, 
$$
z=\sin\left( \sqrt{ \frac{P_{e}\gamma S^{2}}{V_{e}m} } t\right)+\mathfrak{K}, \quad\mathfrak{K} \text{ constante}
$$
On a 
$$
\omega_{0}= \frac{2\pi}{T_{0}}=\sqrt{ \frac{P_{e}\gamma S^{2}}{V _{e}m} }
$$
D'où 
$$
T_{0}=2\pi \sqrt{ \frac{V_{e}m}{P_{e}\gamma S^{2}} }
$$
7. On réalise les mesures:
	1. On lâche la bille depuis le point d'équilibre 
	2. Après avoir utilisé le mode "SINGLE" de l'oscilloscope, on observe la courbe obtenue
	3. On mesure la période avec les curseurs
	4. Après avoir enlevé une quantité $\Delta n$ d'eau, on réitère
 
| $n \text{(dL)}$ | $T_{n} \text{(ms)}$ | $T_{n}^{2} \text{ (s²)}$
| --------------- | ------------------- |
| $0$             | $400$               |  $0.16$
| $5$             | $480$               | $0.23$
| $10$            | $520$               | $0.27$
| $15$            | $600$               | $0.36$
| $20$            | $660$               | $0.44$
| $25$            | $700$               | $0.49$
| $30$            | $710$               | $0.50$
| $40$            | $780$               | $0.60$
| $50$            | $855$               | $0.72$
| $60$            | $925$               | $0.86$
| $70$            | $975$               | $0.95$
8. On trace donc les graphiques $T_{n}^{2}(n)$, avec et sans la droite de régression linéaire.
![[TPruck1.png]]
![[TPruck2.png]]
9. 
$$
T_{n}^{2}=\frac{4\pi^{2}m(V_{e_{1}}+n)}{\gamma S^{2}P_{e}}\implies \text{pente} = \mathfrak{p} = \frac{4\pi^{2}m}{\gamma S^{2}P_{e}}
$$
d'où 
$$
\gamma = \frac{4\pi^{2}m}{\mathfrak{p}S^{2}P_{e}} \quad\quad\text{A.N.} \quad\gamma \approx1.47
$$
Cette valeur de $\gamma$ est cohérente
10. On observe un amortissement dû aux frottements négligés mais cela ne remet pas en cause notre étude car les frottements n'influent pas sur la période.

Expérience de Clément-Desormes
---

1. Voir ci-dessus.
2. Similairement à l'étude précédente, on obtient
$$
P=P_{0}\left( 1-\gamma  \frac{\Delta V}{V_{0}} \right)
$$
d'où
$$
P-P_{0}=-P_{0}\gamma \frac{\Delta V}{V_{0}}=\Delta P_{max}
$$
3. D'après l'équation des gaz parfaits,
$$
PV=nRT
$$
avec $n,T$ constants ici. Donc on a
$$
PV=P_{0}V_{0}
$$
Alors
$$
P=P_{0}\left( \frac{V_{0}}{V} \right)=P_{0}  \frac{V-\Delta V}{V}
$$
donc
$$
P-P_{0}=-P_{0}\frac{\Delta V}{V_{0}}=\Delta P_{eq}
$$
4. On a 
$$
\frac{\Delta P_{max}}{\Delta P_{eq}}=\gamma
$$
5. On réalise les mesures en:
	1. Ouvrant le robinet afin que le flacon soit à pression atmosphérique 
	2. Tirant la seringue pour qu'elle contienne $\Delta V$ d'air
	3. Fermant le robinet
	4. Réduisant brutalement le volume de $\Delta V$ en vidant la seringue 
	5. Mesurant la pression (variation) immédiatement après ($\Delta P_{max}$)
	6. Attendant que le système effectue l'échange thermique 
	7. Mesurant la pression (variation) à l'équilibre ($\Delta P_{eq}$)

| $\Delta V \text{ (mL)}$ | $\Delta P_{max} \text{ (mbar)}$ | $\Delta P_{eq} \text{ (mbar)}$ | $\frac{\Delta P_{max}}{\Delta P_{eq}}$ |
| ----------------------- | ------------------------------- | ------------------------------ | -------------------------------------- |
| $100$                   | $56$                            | $45$                           | $1.24$                                 |
| $100$                   | $60$                            | $46$                           | $1.30$                                  |
| $100$                   | $60$                            | $46$                           | $1.30$                                 |
| $100$                   | $59$                            | $46$                           | $1.28$                                 |
| $100$                   | $57$                            | $45$                           | $1.22$                                 |
| $90$                    | $53$                            | $41$                           | $1.29$                                 |
| $90$                    | $53$                            | $41$                           | $1.29$                                 |
| $90$                    | $55$                            | $42$                           | $1.31$                                 |
| $90$                    | $54$                            | $42$                           | $1.29$                                 |
| $90$                    | $53$                            | $42$                           | $1.26$                                 |
| $80$                    | $49$                            | $37$                           | $1.32$                                 |
| $80$                    | $49$                            | $37$                           | $1.32$                                 |
| $80$                    | $48$                            | $38$                           | $1.26$                                 |
| $80$                    | $48$                            | $37$                           | $1.30$                                 |
| $80$                    | $48$                            | $37$                           | $1.30$                                 |
| $70$                    | $41$                            | $32$                           | $1.28$                                 |
| $70$                    | $41$                            | $32$                           | $1.28$                                 |
| $70$                    | $42$                            | $33$                           | $1.27$                                 |
| $70$                    | $40$                            | $30$                           | $1.33$                                 |
| $70$                    | $39$                            | $31$                           | $1.26$                                 |
| $60$                    | $33$                            | $25$                           | $1.32$                                 |
| $60$                    | $34$                            | $25$                           | $1.36$                                 |
| $60$                    | $35$                            | $25$                           | $1.40$                                 |
| $60$                    | $34$                            | $26$                           | $1.31$                                 |
| $60$                    | $34$                            | $26$                           | $1.31$                                 |
| $50$                    | $28$                            | $22$                           | $1.27$                                 |
| $50$                    | $28$                            | $21$                           | $1.33$                                 |
| $50$                    | $29$                            | $21$                           | $1.38$                                 |
| $50$                    | $26$                            | $21$                           | $1.24$                                 |
| $50$                    | $29$                            | $22$                           | $1.31$                                       |
| $40$                    | $23$                            | $18$                           | $1.27$                                       |
| $40$                    | $22$                            | $19$                           | $1.16$                                       |
| $40$                    | $22$                            | $19$                           | $1.16$                                       |
| $40$                    | $22$                            | $19$                           | $1.16$                                       |
| $40$                    | $22$                            | $20$                           | $1.10$                                       |
| $30$                    | $19$                            | $16$                           | $1.18$                                       |
| $30$                    | $18$                            | $15$                           |  $1.20$                                      |
| $30$                    | $17$                            | $14$                           |  $1.21$                                      |
| $30$                    | $18$                            | $15$                           |  $1.20$                                      |
| $30$                    | $18$                            | $14$                           |  $1.29$                                      |
| $20$                    | $12$                            | $10$                           |  $1.20$                                      |
| $20$                    | $12$                            | $10$                           |  $1.20$                                      |
| $20$                    | $12$                            | $10$                           |  $1.20$                                      |
| $20$                    | $12$                            | $10$                           |  $1.20$                                      |
| $20$                    | $12$                            | $10$                           |  $1.20$                                      |
| $10$                    | $7$                             | $5$                            |  $1.40$                                      |
| $10$                    | $6$                             | $5$                            | $1.20$                                       |
| $10$                    | $7$                             | $5$                            | $1.40$                                       |
| $10$                    | $7$                             | $6$                            | $1.17$                                       |
| $10$                    | $6$                             | $5$                            | $1.20$                                       |

Voici la courbe de $\Delta P_{e}$ en fonction de $\Delta V$ 
![[pe(dv).png]]
Voici la courbe de $\Delta P_{max}$ en fonction de $\Delta V$
![[pm(dv).png]]
On effectue une régression linéaire pour obtenir la pente de chaque droite, et on obtient les valeurs suivantes ($\overline{x}$ étant la valeur moyenne de $x$ et $x=\overline{x}\pm b$ veut dire que l'incertitude sur $x$ est de $b$).
$$
\begin{align}

\overline{\frac{\Delta P_{max}}{\Delta V}} &= 0.59 \\ \\
\overline{\frac{\Delta P_{eq}}{\Delta V}}&= 0.45 \\ \\
\frac{\Delta P_{max}}{\Delta P_{eq}} &= 1.27\pm0.10
\end{align}
$$
Les résultats sont légèrement sous-évalués et la valeur correcte de $\gamma$ est un peut en dehors de l'incertitude.


Bouteille de Franklin
---

1. On a
$$
\ell_{v}=T(v_{v}-v_{\ell}) \frac{dP_{sat}}{dT}
$$
Comme $v_{\ell}\ll v_{v}$ et $v_{v}=\frac{RT}{MP_{sat}}$ on a
$$
\ell_{v}=\frac{RT^{2}}{P_{sat}M}  \frac{dP_{sat}}{dT}
$$
d'où
$$
\frac{dP_{sat}}{dT} -\frac{\ell_{v}M}{RT^{2}}P_{sat}=0
$$
en résolvant cette équation,
$$
P_{sat}=P_{0}e^{\ell_{v}M/R\times-1/T}
$$
d'où
$$
\frac{P_{sat}(T)}{P_{sat}(T_{0})}=e^{-\ell_{v}M/R\times (1/T-1/T_{0})}
$$
puis
$$
\ln \left( \frac{P_{sat}(T)}{P_{sat}(T_{0})} \right)=-\frac{\ell_{v}M}{R} \left( \frac{1}{T}-\frac{1}{T_{0}} \right)
$$
2. On réalise les mesures:
	1. On s'assure que le robinet est ouvert au début
	2. On fait chauffer l'eau dans le chauffe-ballon jusque $\approx 373 \text{ K}$
	3. On lance la pompe à vide et éteint le chauffe-ballon 
	4. On ferme *progressivement* le robinet de manière à maintenir l'ébullition
	5. Tant que l'eau est en équilibre liquide-vapeur, on fait des mesures 
	6. On lit la tension qui est proportionnelle à la pression $P=5U$
 
| $T \text{ (K)}$ | $U \text{ (V)}$ |
| --------------- | --------------- |
| 372.5           | 4.991           |
| 367             | 4.6             |
| 363             | 4.34            |
| 361             | 4.1             |
| 359             | 3.9             |
| 360             | 3.7             |
| 357             | 3.5             |
| 356             | 3.3             |
| 355             | 3.2             |
| 355             | 2.8             |
| 351             | 2.3             |
| 349             | 2.27            |
| 348             | 2.1             |
| 345             | 1.8             |
| 342             | 1.6             |
| 340             | 1.55            |
| 329             | 0.8             |
| 320             | 0.55            |
| 317             | 0.4             |
| 368             | 4.6             |
| 367             | 4.6             |
| 364             | 4.5             |
| 363             | 4.3             |
| 363             | 4.2             |
| 360             | 4.0             |
| 359             | 3.8             |
| 358             | 3.7             |
| 359             | 3.6             |
| 355             | 3.5             |
| 354             | 3.3             |
| 354             | 3.1             |
| 352             | 3.0             |
| 350             | 2.5             |
| 347             | 2.3             |
| 343             | 2.0             |
| 342             | 1.8             |
| 336             | 1.4             |
| 334             | 1.35            |
| 330             | 0.9             |
| 320             | 0.6             |
| 317             | 0.45            |
| 313             | 0.3             |

3. Voici le graphe de $P$ en fonction de $T$
![[P(T).png]]

4. On cherche donc à déterminer une équation de type $f(P)=\alpha g(T)$ qui serait équivalente à notre calcul du modèle de Clapeyron.
On avait donc
$$
P=e^{-\ell_{v}M/R\times 1/T} \implies \ln(P)=- \frac{\ell_{v}M}{R}\times \frac{1}{T}
$$
En choisissant $f=\ln$ et $g=x\mapsto \frac{1}{x}$, on a $\alpha=-\frac{\ell_{v}M}{R}$. Vérifions alors qu'on obtient une droite.
![[pasdroite.png]]
On remarque que la courbe est très similaire à une droite, on en déduit que le modèle est cohérent. Si la pente est $\mathfrak{p}$, on a alors 
$$
\mathfrak{p}=-\frac{\ell_{v}M}{R} \implies \ell_{v}=-\frac{\mathfrak{p}R}{M} \quad\quad \text{A.N.  } \ell_{v}= 2386 \text{ kJ.kg}^{-1}
$$
La valeur est cohérente avec la valeur théorique de $2257 \text{ kJ.kg}^{-1}$.


