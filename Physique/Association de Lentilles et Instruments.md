#physique #cours #optique #lentilles #review 

# Associations de lentilles

## Méthode Générale
> Il est intéressant de commencer par dessiner ce schéma

$$
A \xrightarrow[]{\mathcal{L}_{1}} A_{1} \xrightarrow[]{\mathcal{L}_{2}} A'
$$
- Formules de conjugaison

$$
\begin{align}
\frac{1}{\overline{OA'}} - \frac{1}{\overline{OA}} &= \frac{1}{f'} \\ \\

\overline{F'A'} \overline{FA} &= -f'^{2}
\end{align}
$$
- Relation de Chasles

## Système Afocal

- $F'_{1} = F_{2}$

$$
\infty \xrightarrow[]{\mathcal{L}_{1}} F_{1}'=F_{2} \xrightarrow[]{\mathcal{L}_{2}} \infty
$$

- Avec $3$ lentilles

$$
\infty \xrightarrow[]{\mathcal{L}_{1}} F'_{1} \xrightarrow[]{\mathcal{L}'} F_{2} \xrightarrow[]{\mathcal{L}_{2}} \infty
$$

## Lentilles Accolées

On écrit les relations de conjugaisons:
$$
\begin{align}
\mathcal{L_{1}}: \frac{1}{\overline{OA_{1}}} - \frac{1}{\overline{OA}} &= \frac{1}{f'_{1}}  \\
\mathcal{L_{2}}: \frac{1}{\overline{OA'}} - \frac{1}{\overline{OA_{1}}} &= \frac{1}{f'_{2}} \\ \\

\mathbb{+}: \frac{1}{\overline{OA'}} - \frac{1}{\overline{OA}} = \frac{1}{f'_{1}} + \frac{1}{f'_{2}} &= \frac{1}{f'_{\text{total}}}
\end{align}
$$

# L'Œil

## Consitution

Le cristallin est modélisé par une lentille. Cependant il peut s'accomoder pour voir à l'$\infty$ (pas les myopes).

## Caractéristiques

- $PR$: *punctum remotum*
	le point le plus éloigné vu par l'oeil au repos à l'$\infty$
- $PP$: *punctum proximum*
	le point le plus proche vu par l'oeil au repos à ≈25cm

- Acquité visuelle, angle minimal de distinction de points
 
![[Association de Lentilles et Instruments - Illustration Angle.excalidraw|800x400]]

> Cet angle $\alpha$ est de l'ordre de grandeur de $10^{-4}$

- Le champ visuel est l'espace dont l'image se forme sur une zone sensible de la rétine

## Modélisation

- Changement de lentille
#what 

## Défauts de l'oeil

### Myopie

Trop de convergence
![[Association de Lentilles et Instruments - Illustration Myopie.excalidraw|800x400]]

### Hypermétropie

Faute de convergence

![[Association de Lentilles et Instruments Illustration Hypermétropie.excalidraw|800x400]]

> L'hypermétropie est plus difficile à détecter car l'oeil accomode pour y faire face, au prix d'une fatigue des muscles

### Astigmatie

Faute de sphéricité de l'oeil, on le règle en utilisant une lentille qui compense la forme.
Elle est souvent quantifiée par un degré entre $0°$ et $360°$.

> Ceci peut causer plusieurs types d'aberrations

### Presbytie

Causé par la fatigue de l'oeil, il l'empêche de s'accomoder.

- Soient $D$ la distance entre l'oeil et le $PR$ et $d$ la distance entre l'oeil et le $PP$.
	- Pour un oeil normal, $\frac{1}{d} - \frac{1}{D} \approx 4\delta$
	- Plus on est presbyte, plus cette quantité diminue


## Loupe

![[Association de Lentilles et Instruments - Illustration Loupe.excalidraw|100%]]
- On définit le grossissement
$$
G=\frac{\alpha'}{\alpha}
$$
avec $\alpha$ l'angle sans loupe et $\alpha'$ l'angle avec loupe.

> ne pas confondre avec le grandissement $\gamma=\frac{\overline{A'B'}}{\overline{AB}}$

$$
\tan\alpha=\alpha= \frac{\overline{AB}}{d_{m}}
$$
avec $AB$ au $PP$.

$$
\tan\alpha' = \alpha' = \frac{\overline{AB}}{f'}
$$

- On définit la puissance

$$
P = \left| \frac{\alpha'}{\overline{AB}} \right| = \frac{1}{f'}
$$
## Lunette astronomique

![[Association de Lentilles et Instruments Illustration Lunette Astro.excalidraw|100%]]
La lunette astronomique est un système afocal:
$$
\infty\xrightarrow[O_{1}]{\mathcal{L}_{1}}F_{1}=F_{2}\xrightarrow[O_{2}]{\mathcal{L}_{2}}\infty 
$$
> On appelle encombrement l'épaisseur $\overline{O_{1}O_{2}}=\overline{O_{1}F_{1}}\,\overline{F_{2}O_{2}}=f'_{1}+f'_{2}$

![[Association de Lentilles et Instruments Illustration Lentille Gallilée.excalidraw|100%]]

On définit aussi le grossissement ici:
![[Association de Lentilles et Instruments - Illustration Lunette Astro Grossissement.excalidraw|100%]]
$$
G = \frac{\alpha'}{\alpha} = \frac{\frac{\overline{F'_{1}P}}{-f'_{2}}}{\frac{\overline{F'_{1}P}}{f'_{1}}} = -\frac{f'_{1}}{f'_{2}}
$$
### Profondeur de champ

Il y a deux cas extrêmes:
$$
\begin{align}
\infty \xrightarrow[]{\mathcal{L}_{1}}F'_{1} &= F_{2}\xrightarrow[]{\mathcal{L}_{2}}PR=\infty \\ \\
\infty \xrightarrow[]{\mathcal{L}_{1}}F'_{1} \text{ à } &\ell \text{ de } F_{2} \xrightarrow[]{\mathcal{L}_{2}} PP=\infty
\end{align}
$$
On en déduit la formule de la profondeur de champ:

$$
\begin{align}
\ell=\overline{F_{2}F_{1}'} \\ \\
\overline{F_{2}'(PP)} \cdot \overline{F_{2}F'_{1}} &= -f'_{2} \\
\overline{F'_{2}A'} \cdot \overline{F_{2}A} &= -f_{2}' \\ \\

\ell=\frac{f'^{2}_{2}}{d_{m}}
\end{align}
$$

![[Complément - Microscope]]
