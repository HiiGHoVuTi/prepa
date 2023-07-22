#cours #physique #mécanique

![[Mécanique 2 - Cinématique.pdf]]

# Description cinématique 

## Référentiel absolu

temps absolu => identique pour tous les référentiels
on le supposera dans ce chapitre 

## Position, équations horaires et trajectoires

Position décrite dans un système de coordonnées

$$
\vec{OM} = x(t) \vec{u_{x}} + y(t) \vec{u_{y}} + z(t)\vec{u_{z}}
$$

La trajectoire est la courbe $f(x,y,z)=0$

> on fait disparaître $t$ des équations 

## Vitesse

$$
\vec{v}_{/\mathcal{R}} (t) = \frac{d\vec{OM}}{dt}_{/\mathcal{R}}(t)
$$
> elle dépend du référentiel 

$$
\vec{v}_{/\mathcal{R'}}(t) = \frac{d\vec{OO'}}{dt}_{/\mathcal{R'}}(t) + \frac{d\vec{OM}}{dt}_{/\mathcal{R'}}(t)
$$

## Accélération 

$$
\vec{a}_{/\mathcal{R}} = \frac{d\vec{v}}{dt}_{/\mathcal{R}}
$$

## Expression de la vitesse et de l'accélération

## Coordonnées cartésiennes

$$
\begin{align}
\vec{OM} &= x(t)\vec{u_{x}} + y(t) \vec{u_{y}} + z(t)\vec{u_{z}}  \\
\implies \\
\vec{v} &= \dot{x}\vec{u_{x}} + \dot{y}\vec{u_{y}} + \dot{z}\vec{u_{z}}  \\
\implies  \\
\vec{a} &= \ddot{x}\vec{u_{x}} + \ddot{y}\vec{u_{y}} + \ddot{z}\vec{u_{z}}
\end{align}
$$

## Coordonnées cylindriques

$$
\begin{align}
\vec{OM} &= r(t)\vec{u_{r}} + z(t)\vec{u_{z}}  \\
\implies  \\
\vec{v} &= \dot{r}\vec{u_{r}} + r\dot{\theta}\vec{u_{\theta}} + \dot{z}\vec{u_{z}}  \\
\implies \\
\dots

\end{align}
$$


[[Cours Description cinématique dérivation.excalidraw]]

## Repère de Frenet

$$
\vec{v} = \dot{s}\vec{u_{t}}
$$

$$
\begin{align}
\vec{a} &= \frac{d\vec{u}}{dt} = \ddot{s} \vec{u}t + ṡ  \frac{d\vec{u_{t}}}{dt} \\
&= \ddot{s} \vec{u}_{t} + \frac{\dot{s}^{2}}{R}u_{n} \\
&= \frac{dv}{dt}\vec{u_{t}}+\frac{v^{2}}{R} u_{n} \\
\end{align}
$$
## Repère circulaire 

[[Cours Description cinématique Circulaire.excalidraw]]

# Exemples de mouvement 

## Mouvement circulaire

le rayon de courbure est le rayon du cercle

### Coordonnées polaires

$$
\vec{OM} = R \vec{u_{r}} \implies \vec{v} = R\dot{\theta}\vec{u_{\theta}} \implies \vec{a} = R \ddot{\theta} \vec{u_{\theta}} - R \dot{\theta}^{2} \vec{u_{n}}
$$

## Mouvement rectiligne sinusoïdale

$$
\begin{align}
\vec{OM}(t) &= X\cos(\omega t+\varphi) \vec{u_{x}}  \\
\vec{v}(t) &= -X\omega \sin(\omega t+\varphi)\vec{u_{x}} \\
\vec{a}(t) &= -X\omega^{2} \cos(\omega t+\varphi)\vec{u_{x}} 
\end{align}
$$

> oscillateur harmonique

## Accélération constante

$$
\vec{v} = \vec{a_{0}}t + \vec{v_{0}}
$$

## Uniforme, accéléré et décéléré

### Uniforme 

$$
\frac{dv}{dt} = 0 \iff \vec{v} \cdot \vec{a} = 0
$$

1. $\vec{v} = \vec{0}$, système immobile
2. $\vec{a} = \vec{0}$, mouvement rectiligne uniforme 
3. $\vec{a} \perp \vec{v}$, mouvement circulaire uniforme 


### Accéléré 

$$
\frac{dv}{dt} > 0 \iff \vec{v} \cdot \vec{a} > 0
$$

### Décéléré 

$$
\frac{dv}{dt} < 0 \iff \vec{v} \cdot \vec{a} < 0
$$

## Mouvement circulaire 

Mouvement circulaire ssi $r = R$ en coordonnées polaires 

$$
\vec{OM} = r \vec{u_{r}} \implies \vec{v} = R \dot{\theta} \vec{u_{\theta}}
$$
car $\dot{r} = 0$

$$
\vec{a} = -R \dot{\theta}^{2} \vec{u_{r}} + R \ddot{\theta} \vec{u_{\theta}}
$$
pour un mouvement circulaire uniforme, le terme de droite disparaît car $\ddot{\theta}$ est nul

# Caractère relatif du mouvement - Changement de référentiel 
