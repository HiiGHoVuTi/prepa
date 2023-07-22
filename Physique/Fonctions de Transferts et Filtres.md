
# Fonction de Transfert et diagramme de Bode

## Notion de quadripôle


![[Fonctions de Transferts et Filtres Illustration Quadripôle.excalidraw|100%]]

$$
\begin{align}
\underline{s} &\propto e, \underline{i_{e}} \\
\underline{i_{s}} &\propto e, \underline{i_{e}}
\end{align}
$$
$$
\begin{cases}
\underline{e} &= \underline{Z}_{e,e} \underline{i}_{e} + \underline{Z}_{e,s} \underline{i}_{s} \\
\underline{s} &= \underline{Z}_{s,e} \underline{i}_{e} + \underline{Z}_{s,s} \underline{i}_{s}
\end{cases}
$$

On a alors une impédance d'entrée et une impédance de sortie

$$
\begin{cases}
\underline{Z}_{e}& = \frac{\underline{e}}{\underline{i}_{e}} \\
\underline{Z}_{s} &= \frac{\underline{s}}{\underline{i}_{s}}
\end{cases}
$$

## Fonction de transfert en régime sinusoïdal

Le système est linnéaire seulement si
$$
\begin{align}
\sum a_{k} \frac{d^{k}a}{dt^{k}} &+ \sum b_{\ell} \frac{d^{\ell}e}{dt^{\ell}} &= 0 \\
\sum a_{k} (j\omega)^{k} \underline{s} &+ \sum b_{\ell} (j\omega)^{\ell} \underline{e} &= 0 \\
\implies \\
\underline{H} = \frac{\underline{s}}{\underline{e}} &= - \frac{\sum b_{\ell}(j\omega)^{\ell}}{\sum a_{k} (j\omega)^{k}}
\end{align}
$$

## Lien  entre fonction de transfert et équation différentielle

![[Fonctions de Transferts et Filtres Illustration RCRC.excalidraw|100%]]

$$
\underline{H} = \frac{\underline{s}}{\underline{e}} = \dots
$$

## Gain et phase d'une fonction de transfert

- Gain
$$
G = | \underline{H} |
$$
- Gain en décibels
$$
G_{dB} = 20 \log_{10}G
$$

- Phase
$$
\phi = \text{arg}(\underline{R})
$$
## Les deux tracés du diagramme de Bode

1. Diagramme en gain
$$
G_{dB} = f\left( \log_{10}\left( \frac{\omega}{\omega_{0}} \right) \right)
$$

![[Fonctions de Transferts et Filtres Diagramme Gain.excalidraw|100%]]
2. Diagramme en phase

## Exemple du circuit $R,C$

![[Circuit RC.excalidraw|100%]]

$$
\begin{align}
\underline{s} &= \frac{\underline{Z}_{c}}{\underline{Z}_{c}+\underline{Z}_{r}} \underline{e} \\
\underline{H} &= \frac{\frac{1}{j\omega C}}{\frac{1}{j\omega C}+R}=\frac{1}{1+j\omega RC} \\
G &= |\underline{H}| \\
G &= \frac{1}{\sqrt{ 1+R^{2}C^{2}\omega^{2} }}
\end{align}
$$
On observe aux limites,
$$
\begin{align}
\omega \to 0 \implies G \to 1
\end{align}
$$
Ou on peut faire une approximation quand $\omega\to+\infty$
$$
G \approx \frac{1}{RC\omega} \land G_{dB} = -20\log RC\omega
$$

Diagramme asymptotique:
- $\omega\to 0 \implies$ asymptote horizontale, $G_{dB}=0$
- $\omega\to+\infty$ asymptote pente à $-20$dB/déc (linéaire)

> [[Unités]]

On trace la vraie courbe (bleu) grâce aux deux asymptotes (orange)

![[Fonctions de Transferts et Filtres Bode Asymptotes.excalidraw|100%]]

> On voit $G_{dB}(\omega_{0}) \approx -3dB$

On peut calculer le déphasage $\phi$ de $\underline{H}$

$$
\begin{align}
\underline{H} &= \frac{1}{1+jRC\omega} \\
\phi &= \text{arg}(\underline{H}) = -\text{arg}(1+jRC\omega) \\
&= -\text{arctan}(RC\omega) &\text{car } RC\omega>0
\end{align}
$$

On en déduit que $\omega \to 0 \implies \phi \to 0$ et $\omega \to +\infty \implies \phi \to -\frac{\pi}{2}$

![[Fonctions de Transferts et Filtres Phase.excalidraw|100%]]

# Notion de filtre

## But du filtrage

- Se débarrassser du bruit
- Se focaliser sur certains signaux

## Bande passante

La bande passante est l'ensemble (intervalle) des fréquences conservées après le filtre. La BP à $3$dB est l'ensemble des fréquences telles que
$$
\begin{align}
G(\omega) &\geq \frac{G_{max}}{\sqrt{ 2 }} \\
G_{dB} = 20\log(G(\omega)) &\geq 20 \log(G_{max}) - 20 \sqrt{ 2 } \\ \\

G_{dB}(\omega) &\geq G_{dB,max} - 3
\end{align}
$$
![[Fonctions de Transferts et Filtres Filtrage.excalidraw|100%]]

## Filtrage idéal

Le filtrage idéal est impossible, il serait discret et total.

## Types de filtres

En orange le filtre idéal associé et en bleu le filtre réel

### Passe-bas

![[Fonctions de Transferts et Filtres Passe Bas.excalidraw|100%]]

### Passe-haut

![[Fonctions de Transferts et Filtres Passe-Haut.excalidraw|100%]]

### Passe-Bande

![[Fonctions de Transferts et Filtres Passe Bande.excalidraw|100%]]

### Coupe Bande

![[Fonctions de Transferts et Filtres Coupe Bande.excalidraw|100%]]

### Ordre des filtres

$$
\underline{H}=\frac{N(j\omega)}{D(j\omega)}
$$
On considère la réponse du système, donc $D(j\omega)\underline{s}$. L'ordre du filtre est $\text{deg}D$.

# Filtres passifs du 1er ordre

## Définition

Un filtre du premier ordre est un filtre associé à une équation différentielle du premier ordre en $\underline{s}$, donc un dénominateur du type $1+\frac{j\omega}{\omega_{0}}$ et donc
$$
\left( 1 + j \frac{\omega}{\omega_{0}}  \right)\underline{s} = N(j\omega)\underline{e}
$$
### Forme canonique passe-bas
$$
\frac{H_{0}}{1+j \frac{\omega}{\omega_{0}}}
$$
### Forme canonique passe-haut
$$
H_{0} \times \frac{j \frac{\omega}{\omega_{0}}}{1+j \frac{\omega}{\omega_{0}}}
$$
## Filtre passe-bas du premier ordre

### Exemple du Circuit $R,C$

![[Circuit RC.excalidraw|100%]]

$$
\underline{s} = \frac{1}{1+jRC\omega} \underline{e}
$$

On identifie
$$
\begin{cases}
H_{0} &= 1 \\
\omega_{0} &= \frac{1}{RC}
\end{cases}
$$
Et on met sous forme canonique ![[Fonctions de Transferts et Filtres#Forme canonique passe-bas]]
### Comportement asymptotique

![[Physique/Comportement Asymptotique RC]]

## Filtre passe bas



## Filtre passe haut

