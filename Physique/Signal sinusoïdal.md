# Définition

$$
\begin{align}
x(t)&=X\cos(\omega t+\phi) \\
&= X\sin(\omega t+\psi) \\
&=A\sin(\omega t) + B\cos(\omega t)
\end{align}
$$
avec $\psi\equiv\phi+\frac{\pi}{2} [2\pi]$

# Amplitude

$$
X = \sqrt{ A² + B² }
$$

# Valeur Moyenne

$$
\begin{align}
<x> &= \frac{1}{T} \int_{t_{0}}^{t_{0}+T} x(t)  \, dt  \\
&= \frac{1}{T} \int_{t_{0}}^{t_{0}+T} X\cos(\omega t+\phi)  \, dt \\
&= \frac{X}{T} \left[ \frac{\sin(\omega t + \phi)}{\omega} \right]_{t=t_{0}}^{t_{0}+T} \\
<x> &= \frac{X}{T} \frac{\sin(\omega t+\phi+\omega T)-\sin(\omega t+\phi)}{\omega}
\end{align}
$$
or on voit $\omega T=2\pi$ car on a défini $\omega=\frac{2\pi}{T}$
$$
<x> = 0
$$

# Valeur efficace

$$
\begin{align}
X_{eff} &= \sqrt{ \frac{1}{T} \int _{t_{0}}^{t_{0}+T} x²(t) \, dt  } \\ \\
&= \sqrt{ \frac{1}{T}\int _{t_{0}}^{t_{0}+T}X²\cos(\omega t+\phi) \, dt  } \\
&= \sqrt{ \frac{X²}{2T}\int _{t_{0}}^{t_{0}+T}\cos(2\omega t+2\phi) +1 \, dt  }  \\
&=\sqrt{ \frac{X²}{2T} \left[ \frac{\sin(2\omega t + 2\phi)}{2\omega} +t\right]_{t=t_{0}}^{t_{0}+T} } \\
X_{eff} &= \frac{X}{\sqrt{ 2 }} = \frac{\sqrt{ 2 }}{2}X
\end{align}
$$
# Pulsation - Fréquence - Période

![[Période - Fréquence - Pulsation]]

# Mesures de fréquence ou période

On mesure l'équart entre deux maxima ou deux minima. Pour plus de précision on en mesure plusieurs à la fois.

```functionplot
---
title: 
xLabel: 
yLabel: 
bounds: [-6,6,-1.1,1.1]
disableZoom: false
grid: false
---
f(x)=cos(x+1.8)
```

On peut effectuer une $FFT$ pour obtenir un spectre de fréquences.

# Phases

- Phase instantanée
$$
\omega t+\phi
$$
- Phase initiale / à l'origine
$$
\phi
$$

> la phase n'intervient vraiment que lors du déphasage entre deux signaux


# Déphasage

Pour un déphasage, il faut que $f_{1}=rf_{2}$ avec $r\in \mathbb{Q}$, le plus souvent $f_{1}=f_{2}$.

Le déphasage de $x_{2}$ par rapport à $x_{1}$ est $\phi_{2}-\phi_{1}$.

| En phase            | Opposition de phase                   |
| ------------------- | ------------------------------------- |
| $\phi_{2}\equiv\phi_{1}[2\pi]$ | $\phi_{2}-\phi_{1} \equiv \pi [2\pi]$ |

