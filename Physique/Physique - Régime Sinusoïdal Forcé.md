# Intérêt de la notation complexe

## Exemple du $R,C$ série

![[Physique - Régime Sinusoïdal Forcé R,C.excalidraw|100%]]

$$
\begin{align}
e(t)&=E\cos(\omega t) \\ \\
\text{Maille: } \\
e(t)-Ri(t)-u&= 0 \\
\text{Condensateur: }\; i&=C \frac{du}{dt} \\
RC \frac{du}{dt}+u = e(t) &=E\cos(\omega t) 
\end{align}
$$
On résoud l'équation différentielle

1. $u_{H}(t) = Ue^{-t/\tau}$
2. On cherche $u_{p}$ sous la forme du second membre
$$
\begin{align}
u_{p} &= X\cos(\omega t + \phi) \\
&=A\cos(\omega t) + B\sin(\omega t) \\
\frac{du_{p}}{dt}&= -X\omega \sin(\omega t+\phi) \\
\tau(-X\omega \sin(\omega t+\phi)) +X\cos(\omega t+\phi) &= E\cos(\omega t) \\
(X\cos \phi  -\tau X\omega \sin \phi-E)\cos(\omega t) &-(\tau X\omega \cos \phi+X\sin \phi)\sin(\omega t) = 0 \\
\begin{cases}
X\cos \phi-\tau X\omega\sin \phi&=E \\
\tau X\omega \cos \phi+X\sin \phi &= 0
\end{cases} \\
\tan \phi &= -\tau\omega= -RC\omega \\
\sin \phi &= -\tau\omega \cos \phi \\
X\cos \phi+\tau²\omega²X\cos \phi&=E \\
X\cos \phi&=\frac{E}{1+\tau²\omega²} \\
\tan²\phi&=\frac{\sin²\phi}{\cos²\phi}=\frac{1}{\cos²\phi}-1 \\
\cos \phi=\frac{1}{\sqrt{ 1+\tan²\phi }}&=\frac{1}{\sqrt{ 1+\tau²w² }} \\
\implies \\
X=\frac{E}{(1+\tau²\omega²\cos \phi)}&= \frac{E}{\sqrt{ 1+\tau²\omega² }}
\end{align}
$$

## Notation complexe

Dans tout ce chapitre on pose $j²=-1$ et on travaille dans $\mathbb{R}[j]$.
$$
\begin{align}
x(t)&=X\cos(\omega t+\phi) \\
&= \text{Re}(Xe^{j(\omega t+\phi)}) \\
\underline{x}(t) &= Xe^{j(\omega t+\phi)}
\end{align}
$$

On a alors
$$
\begin{align}
\underline{x}(t)&=Xe^{j\phi}e^{j\omega t} \\
\underline{X}&= Xe^{j\phi}
\end{align}
$$
- C'est l'**amplitude complexe**
L'amplitude réelle $X=|\underline{X}|=|\underline{x}(t)|$

- La **phase initiale** est alors $\text{Arg}(\underline{X})$ 

- La **phase instantanée** est $\omega t+\phi=\text{Arg}(\underline{x}(t))$

## Règles de calcul

$$
\begin{align}
|\underline{x_{1}}\underline{x_{2}}|&=|\underline{x_{1}}| |\underline{x_{2}}| \\
\text{Arg}(\underline{x_{1}}\underline{x_{2}})&= \text{Arg}(\underline{x_{1}})+\text{Arg}(\underline{x_{2}}) \\
\text{Arg}\left( \frac{1}{\underline{x}} \right)&=-\text{Arg}(\underline{x})
\end{align}
$$

## Représentation de Fresnel dans le plan complexe
voir le cours de maths

## Traduction des opérations différentielles

### Dérivée

![[Quelques Résultats de base sur les Intégrales et Primitives#Dans les Complexes]]

$$
\begin{align}
\underline{x}(t)&=Xe^{j(\omega t+\phi)} \\
\frac{dx}{dt}&=X(-\omega \sin(\omega t+\phi)) \\
&=\omega X\cos\left( \omega t+\phi+\frac{\pi}{2} \right) \\
&= \text{Re}(\omega Xe^{j(\omega t+\phi+\pi/2)}) \\
&= Re(j\omega \times Xe^{j(\omega t+\phi)})
\end{align}
$$

On a alors
$$
\frac{dx}{dt} \text{ réel} \iff j\omega \underline{x} \text{ complexe}
$$

### Primitive

$$
\begin{align}
\int x(t) \, dt &= \int X\cos(\omega t+\phi) \, dt \\
&=  X \frac{\sin(\omega t+\phi)}{\omega} \\
&= \text{Re}\left( \frac{Xe^{j(\omega t+p)}}{j\omega} \right)
\end{align}
$$
On  a alors
$$
\int x(t) \, dt = \frac{\underline{x}}{j\omega}
$$

## Retour à l'exemple

$$
\begin{align}
RC \frac{du}{dt}+u&=E\cos\omega t \\
Rc j\omega Ue^{j(\omega t+\phi)} + Ue^{j(\omega t+\phi)} &= Ee^{j\omega t} \\
(jRC\omega+1)Ue^{j(\phi)} &= E \\
\underline{U}=Ue^{j\phi}&=\frac{E}{1+jRC\omega} \\
U &= |\underline{U}| = \left|\frac{E}{1+jRC\omega}\right| \\
U &=\left| \frac{E}{\sqrt{ 1+R²C²\omega² }} \right| \\
\phi&=\text{Arg}(\underline{U})=-\text{Arg}(1+jRC\omega) \\
\tan \phi&= -RC\omega
\end{align}
$$

# Lois de Kirchoff en notation complexe

## Validité des lois du continu en régime sinusoïdal

ok

## Loi des noeuds


$$
\sum_{k=0}^{n} \underline{i}_{k}(t)\epsilon_{k}=0
$$

## Loi des mailles

$$
\sum_{k=0}^{n} \underline{u}_{k}(t)\epsilon_{k}=0
$$

# Impédances ou admittances complexes

> on rappelle
$$
\underline{u}(t)=\underline{U}e^{j\omega t} \quad \underline{U}=Ue^{j\phi}
$$

## Vocabulaire

### Impédance (complexe)
$$
\underline{Z} = \frac{\underline{u}}{\underline{i}} = \frac{\underline{U}}{\underline{I}}
$$

### Admittance
$$
\underline{Y} = \frac{1}{\underline{Z}}
$$
### Impédance réelle
$$
| \underline{Z} | = Z
$$
### Déphasage
$$
\phi = \text{Arg} \underline{Z}
$$
### Résistance $R$ et Réactance $X$
$$
\begin{align}
\underline{Z} &=Z\cos \phi+jZ\sin \phi \\
&= R + jX
\end{align}
$$
## Dipôles usuels

### Résistance

$$
\begin{align}
\underline{u}(t) &= R\underline{i}(t) \\
\underline{Z}&=R
\end{align}
$$

> $\phi=0$

### Bobine

$$
\begin{align}
u(t) &= L \frac{di}{dt} \\
\underline{u}(t) &= j\omega L\underline{i}(t) \\
\underline{Z} &= j\omega L
\end{align}
$$

### Condensateur

$$
\begin{align}
i(t) &= C \frac{du}{dt} \\
i(t) &= jC \omega \underline{u}(t) \\
\underline{u}(t) &= \frac{1}{jC\omega}\underline{i}(t) \\
\underline{Z} &= -\frac{j}{C\omega}
\end{align}
$$

## Association d'impédances

### En série

- $\underline{i_{k}}=\underline{i_{\ell}}$
- $\underline{u} = \sum \underline{u_{k}}$
donc
- $\underline{Z}=\sum\underline{Z_{k}}$

### En Parallèle

- $\underline{i} = \sum\underline{i_{k}}$
donc
- $\frac{1}{\underline{Z}} = \sum \frac{1}{\underline{Z_{k}}}$

# Ponts diviseurs complexes

## Pont diviseur de tension
$$
\begin{align}
\underline{u}&=(\underline{Z_{1}}+\underline{Z_{2}})\underline{i} \\
\underline{i}&=\frac{\underline{u}}{\underline{Z_{1}}+\underline{Z_{2}}} \\
\underline{u_{1}}&=\underline{Z_{1}}\underline{i}
\end{align}
$$
donc
$$
u_{1}=\frac{\underline{Z_{1}}}{\sum\underline{Z_{k}}} \underline{u}
$$

## Pont diviseur de courant

$$
\underline{i_{1}}=\frac{\underline{Z_{1}}}{\sum \underline{Z_{k}}} \underline{i}
$$
