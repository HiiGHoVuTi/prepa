---
dg-publish: false
active: false
---

#physique/cours

# Objet de la Mécanique

![[Mécanique 1 - Introduction et systèmes de coordonnées 1.pdf]]

## Définitions

- cinématique
décrire le mouvement d'un point matériel

- dynamique
décrire les forces

- statique
cas particulier de la dynamique, quand la vitesse est $0$

## Cadre de la Mécanique Newtonienne

- Il faut des repères de temps et d'espace.

- Précision infinie en termes de vitesse et de position (pas d'inégalité d'Heisenberg).

- Pas de système chaotique.

- L'espace est euclidienne 

# Systèmes de coordonnées

## Base fixe - coordonnées cartésiennes

On se munit d'un repère $(O, \hat{\mathbf{x}}, \hat{\mathbf{y}}, \hat{\mathbf{z}})$

Un point $M$ est identifié par le vecteur $\hat{OM} = x \hat{\mathbf{x}} + y \hat{\mathbf{y}} + z \hat{\mathbf{z}}$.

On peut faire un déplacement élémentaire de $M$ à $M'$:
$$
d \hat{OM} = d\hat{\mathbf{x}}+d\hat{\mathbf{y}}+d\hat{\mathbf{z}}
$$
Volume élémentaire
$$
d\tau = dx\times dy\times dz
$$

## Base mobile - coordonnée cylindriques


On se munit d'un repère $(O, \hat{\mathbf{x}}, \hat{\mathbf{y}}, \hat{\mathbf{z}})$ et on décrit des coordonnées avec un triplet $(r, \theta, z)$
où
$$
\hat{OM} = r \cos \theta \hat{\mathbf{x}} + r \sin \theta \hat{\mathbf{y}} + z\hat{\mathbf{z}}
$$
A partir de coordonnées cartésiennes:
$$
\begin{cases}
r = \sqrt{ x^{2}+y^{2} } \\
\theta=\arctan\left( \frac{y}{x} \right) + \begin{cases} 
\pi  \\
2\pi 
\end{cases}
\end{cases}
$$
$$
\begin{cases}
\hat{u}_{r} = \cos \theta \hat{u}_{x} + \sin \theta \hat{u}_{y} \\
\hat{u}_{r} = -\sin \theta \hat{u}_x + \cos \theta \hat{u}_{y}
\end{cases}
$$
$$
\begin{cases}
\hat{u}_{x} =\cos \theta \hat{u}_{x} - \sin \theta \hat{u}_{y} \\
\hat{u}_{y} = \sin \hat{\theta}u_{x} + \cos \theta \hat{u}_{y}
\end{cases}
$$

On donne aussi les noms suivants:
$$
\hat{a} = a_{r} \hat{u}_{r} + a_{\theta}\hat{u}_{\theta } + a_{z}\hat{u}_{z}
$$
Composantes radiale, orthoradiale, et axiale.

Pour les variations:

$$
d\hat{OM} = dr \hat{u}_{r} + r d\theta \hat{u}_{\theta} + dz \hat{u}_{z}
$$

> $\iiint \dots \, dxdydz$
> $\int\oint \dots \, dr d\theta$


## Une autre base mobile, coordonnées sphériques

On utilise deux angles et une position est un triplet $(r, \theta, \phi)$ avec $\theta$ entre $z$ et $y$ et $\phi$ entre $x$ et $y$ avec $\theta \in [0; \pi[$ et $\phi \in [0; 2\pi[$

==insérer vocabulaire méridien, etc==

Pour retrouver les coordonnées polaires, $z = \cos \theta$

On donne les noms suivants:
$$
\hat{a} = a_{r}\hat{u}_{r} + a_{\theta} \hat{u}_{\theta} + a_{\phi} \hat{u}_{\phi}
$$
$a_{r}$ est la composante radiale

Déplacement élémentaire:
$$
d \hat{OM} = d \hat{u}_{r} + r d\theta \hat{u}_{\theta} + r \sin \theta d\phi \hat{u}_{\phi}
$$

## Base liée au mouvement, repère de Frenet

voir suite

# Dérivée d'un vecteur unitaire tournant

## Le cas des coordonnées polaires

$$
\begin{cases}
d \hat{u}_{r} = d \theta \hat{u}_{\theta} \\
d \hat{u}_{\theta} = - d\theta \hat{u}_{r}
\end{cases}
$$

## Cas général

On l'obtient en dérivant l'expression $\hat{u}=1$, la dérivée est perpendiculaire à $\alpha$