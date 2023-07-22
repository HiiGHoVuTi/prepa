---
dg-publish: true
---

En général, on travaillera avec $a,b,c \in \mathbb{R}$ (avec $a \neq 0$) en on cherchera les solutions à valeurs réelles.
Si $ay''+by'+c=0$ l'équation caractéristique a des solutions complexes conjuguées ou réelles.
$\alpha_{1}=A+i\omega, \alpha_{2}=\overline{\alpha_{1}}$
On a donc, en prenant des combinaisons linéaires qui arrangent:
$$
\frac{e^{\alpha_{1}t}+e^{\alpha_{2} t}}{2}= \cos(\omega t)e^{At}
$$
Et:
$$
\frac{e^{\alpha_{1}t}-e^{\alpha_{2}t}}{2i} = \sin(\omega t)e^{At} 
$$
Par combinaisons linéaires, l'ensemble des solutions est:
$$
\{ \lambda_{1}\cos(\omega t)e^{At}+\lambda_{2}\sin(\omega t)e^{At};\; \lambda_{1},\lambda_{2} \in\mathbb{R} \}
$$

Dans l'autre sens, on suppose $f\in S_{E,\mathbb{R}} \subset S_{E,\mathbb{C}}$
donc il existe $\lambda_{1},\lambda_{2} \in \mathbb{C}$ tels que $f(t) = \lambda_{1}e^{\alpha_{1}}+\lambda_{2}e^{\alpha_{2}t}$

On pose $\alpha_{1}=A+i\omega$ et $\alpha_{2}=A-\omega i$
On peut alors factoriser par $e^{At}$
$$
(\lambda_{1}e^{i\omega t}+\lambda_{2}e^{i\omega t})e^{At}
$$
On a donc 
$$
\lambda_{1}e^{i\omega t} + \lambda_{2}e^{-i\omega t} \in \mathbb{R}
$$
En choisissant $t=0$ et $t=\frac{\pi}{2\omega}$, on obtient le système suivant
$$
\begin{cases}
\lambda_{1}+\lambda_{2} &\in \mathbb{R} \\
\lambda_{1}i - \lambda_{2}i &\in \mathbb{R}
\end{cases}
$$
Donc $\lambda_{1}=\overline{\lambda_{2}}$. On pose $\lambda_{1}=u+iv$ avec $u,v\in\mathbb{R}$.
D'où

$$
\begin{align}
& \lambda_{1}e^{\alpha_{1}t}+\lambda_{2}e^{\alpha_{2} t} \\
=& (u+iv) e^{i\omega t}e^{At} + (u-iv)e^{-i\omega t}e^{At} \\
=& ((u+iv)e^{i\omega t}+(u-iv)e^{-i\omega t})e^{At} \\ \\
\end{align}
$$

Les deux quantités de la parenthèse sont conjuguées
$$
\begin{align}
=& 2\text{Re}((u+iv)e^{i\omega t})e^{At} \\
= & 2(ucos(ω t)-vsin(ω t))eAt
\end{align}
$$
C'est effectivement une combinaison linéaire.