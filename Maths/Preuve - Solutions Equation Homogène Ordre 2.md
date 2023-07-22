---
dg-publish: true
---

Soit $E=\mathcal{C}^{\infty}/(\mathbb{R},\mathbb{C})$

On introduit:

$$
\begin{align}
&\phi :& E \to E \\
&\phi(y) =& ay'' + by' + cy
\end{align}
$$

Résoudre l'équation homogène revient à déterminer $\phi^{-1}(\{ \Delta_{0} \})$.

Soient $\alpha_{1}$, $\alpha_{2}$ les deux racines (peut-être confondues) de $a\alpha^{2}+b\alpha+c=0$.

On introduit aussi:

$$
\begin{cases}
\phi_{1}(y)=y'-\alpha_{1}y \\
\phi_{2}(y)=y'-\alpha_{2}y
\end{cases}
$$
Calculons alors $\phi_{1}\circ\phi_{2} (y)$
$$
\phi_{1} \circ \phi_{2} (y)= y'' - \alpha_{1} y' - \alpha_{2}y' + \alpha_{1}\alpha_{2}y
$$
Par les relations [[Maths/Formules Coéfficients-Racines|coéfficients-racines]]:
$$
= y'' + \frac{b}{a}y' + \frac{c}{a}y = \frac{\phi}{a}
$$
Donc on a une équivalence:
$$
\phi(y) = \Delta_{0} \iff \phi_1\circ\phi_{2}(y)=\Delta_{0}
$$
Posons alors $g=\phi_{2}(y)$, on a toujours
$$
\phi(y) = \Delta_{0} \iff \phi_{1}(g) = \Delta_{0} \iff g'-\alpha_{1}g = \Delta_{0}
$$
Donc $g$ est de la forme $\gamma e^{\alpha_{1}t}$

Il reste donc à résoudre
$$
\begin{align}
g&=\phi_{2}(y) \\
y'-\alpha_{2}y&=\gamma e^{\alpha_{1}t}
\end{align}
$$
La solution homogène est $y_{h}=\lambda_{2}e^{\alpha_{2}t}$
Pour la solution particulière on aura deux cas à traîter:
$$
y' - \alpha_{2}y=e^{\alpha_{1}t}
$$

> il faut pensefr à remettre le $\gamma$ par superposition à la fin

1. Si $\alpha_{1}=\alpha_{2}$
On sait que la solution sera de forme $y=\delta te^{\alpha_{1}t}$
On calcule la dérivée et on remplace pour déterminer $\delta=1$.


On a alors (*quelques étapes sautées*):
$$
y = \lambda_{2}e^{\alpha_{2}t}+\gamma t e^{\alpha_{2}t} 
$$

2. Si $\alpha_{1}\neq\alpha_{2}$
$$
y' - \alpha_{2}y = \gamma e^{\alpha_{1} t}
$$
Donc on a une solution de la forme $y(t)=\delta e^{\alpha_{1}t}$
On a alors
$$
y'(t)=\alpha_{1}\delta e^{\alpha_{1}t}
$$
Donc (étapes sautées aussi):
$$
y(t) = \lambda_{2}e^{\alpha_{2}t}+\frac{\gamma}{\alpha_{1}-\alpha_{2}}e^{\alpha_{1}t}
$$
