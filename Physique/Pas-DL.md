1. Avant l'entrée dans l'eau, on suppose que le plongeur est en chute libre verticale. On étudie le système `Plongeur` dans le référentiel terrestre supposé Galiléen car le mouvement dure beaucoup moins d'un jour. On suppose que la seule force s'appliquant est le poids du plongeur. On applique le principe fondamental de la dynamique:
$$
m\vec{a}=m\vec{g} \implies \boxed{\vec{a} = \vec{g}}
$$
En projettant le résultat obtenu sur la verticale:
$$
\ddot{z} = g \implies v=gt \implies z = \frac{gt^{2}}{2}
$$
En supposant les conditions initiales nulles et l'axe orienté vers le bas.
Etudions l'équation obtenue afin de trouver pour quel $t$ on a $z=10$:
$$
z = 10 \iff \frac{gt^{2}}{2} = 10
$$
On résoud alors l'équation pour obtenir deux solutions et on choisit celle nous donnant un temps positif, qui est celui où il atteint l'eau:
$$
\boxed{
t = \sqrt{ \frac{20}{g} } = 1,4 \text{ s}
}
$$
On n'a plus qu'à déterminer la vitesse du plongeur à $t=1,4\text{ s}$
$$
\boxed{
\dot{z}(1,4\text{ s}) = 13,7 \text{ s}
}
$$

2. a. Une fois le plongeur dans l'eau on étudie toujours le même système dans le même référentiel, mais le bilan des forces est différent. Désormais on a la force de frottement fluide et la poussée d'Archimède qui s'ajoutent au poids:
$$
\vec{P} = m\vec{g} \quad \vec{f} = -k\vec{v}\quad \vec{\Pi}= -\frac{m}{d}\vec{g}
$$
On applique le principe fondamental de la dynamique que l'on projette sur l'axe vertical:
$$
m\ddot{z} = g\left( m - \frac{m}{d} \right) - kz
$$
En passant tout du même côté, 
$$
\boxed{\ddot{z} + \frac{k}{m}v = g\left( 1-\frac{1}{d} \right)}
$$
b. Résolvons l'équation homogène puis déterminons une solution particulière:
- $$
\ddot{z} + \frac{k}{m} v = 0
$$
on multiplie par $dt$ et divise par $v$:
$$
\frac{dv}{dt}+\frac{k}{m}v = 0 \implies \frac{dv}{v}+\frac{k}{m}dt = 0
$$
on peut désormais intégrer des deux côtés car on a deux formes différentielles:
$$
\int_{1}^{v} \frac{1}{v} \, dv = -\int^{t} \frac{k}{m} \, dt  
$$
on obtient alors:
$$
\ln(v)=-\frac{k}{m}t+ C
$$
avec $C$ une constante d'intégration.
En passant à l'exponentielle:
$$
v = e^{C - kt/m}
$$
et enfin en posant $A = e^{C}$,
$$
v_{h}=Ae^{-kt/m}
$$
- $$
\frac{k}{m}v_{p}=g\left( 1-\frac{1}{d} \right)
$$
nous donne une solution particulière:
$$
v_{p} = \frac{mg}{k}\left( 1-\frac{1}{d} \right) 
$$
- On obtient alors la solution avec un degré de liberté:
$$
\boxed{ 
v = Ae^{-kt/m}+\frac{mg}{k}\left( 1-\frac{1}{d} \right)
}
$$
- Connaissant les conditions initiales, on peut déterminer la constante:
$$
v_{0} = A + \frac{mg}{k}\left( 1-\frac{1}{d} \right) \implies A = v_{0} -\frac{mg}{k}\left( 1-\frac{1}{d} \right)
$$
Ainsi, on a:
$$
\boxed{ 
v = \left( v_{0} - v_{\infty} \right)e^{-kt/m} + v_{\infty}, \quad v_{\infty}=\frac{mg}{k}\left( 1-\frac{1}{d} \right)
}
$$
c. En faisant tendre $t$ vers $+\infty$, on obtient $v_{\infty}$ (d'où le nom choisi):
$$
v=(v_{0}-v_{\infty})e^{-kt/m}+v_{\infty} \xrightarrow[t \to +\infty]{}  v_{\infty}=v_{L}
$$
On calcule $v_L$ qui est la vitesse limite dans cette situation:
$$
\boxed{
v_L= \frac{80\times 9,81}{250}\left( 1-\frac{1}{0,90} \right) = -0,35 \text{ m}
}
$$

d. On l'a déjà fait dans la question b. grâce à notre définition de $v_{\infty}$:
$$
v = \left( v_{0} - v_{L} \right)e^{-kt/m} + v_{L}
$$

e. On cherche à déterminer quand le nageur commence à remonter, soit quand la vitesse change de signe, donc nécessairement lorsqu'elle est nulle (continuité de $v$):
$$
v= (v_{0} - v_L)e^{-kt/m} + v_L = 0 \implies e^{-kt/m} = \frac{v_L}{v_{0}-v_L}
$$
En passant l'égalité au logarithme, (le déplacement étant ralenti, on a bien $v_{0}>v_L$):
$$
\boxed{
t=-\frac{m}{k}\ln\left(\frac{v_L}{v_{0}-v_L}\right)
}
$$
Application numérique:
$$
t= - 80 \times \frac{\ln\left( \frac{0.35}{14-0.35} \right)}{250} = 1,19 \text{ s}
$$

f. On obtient la profondeur en prenant la primitive de la vitesse en fonction du temps:
$$
\boxed{ 
z = - \frac{m}{k}(v_{0}-v_L)e^{-kt/m} + v_Lt + Z
}
$$
Or on a choisi $z(0)=0$ donc on peut déterminer $Z$:
$$
Z = \frac{m}{k}(v_{0}-v_L)
$$
Ainsi, on a:
$$
\boxed{
z =- \frac{m}{k}(v_{0}-v_L)e^{-kt/m} + v_Lt + \frac{m}{k}(v_{0}-v_L) 
}
$$

On fait l'application numérique pour le temps de remontée obtenu: $\boxed{z = 4,06 \text{ m}}$

g. On cherche $t$ tel que $v=1,0$, par le même procédé que pour $v=0$, on obtient:
$$
\boxed{ 
t=-\frac{m}{k}\ln\left( \frac{v_L + 1}{v_{0}-v_L} \right)
}
$$
Application numérique: $t_{1}=0,76 \text{ s}$.
On réinjecte maintenant $t_1$ dans la formule de la profondeur:
$$
\boxed{ 
z(t_{1})= 3,90 \text{ m}
}
$$
On a alors la profondeur minimale du bassin de $3,90 \text{ m}$.