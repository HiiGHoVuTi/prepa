#si #exercice #asservissement #équation-différentielle #transformée-laplace #schéma-bloc

# Énoncé

$$
(E): \begin{cases}
A\frac{d²\theta}{dt²} &= M(t) \\
m\frac{dv_x}{dt} &= -K_xv_x+F_p\text{sin}\theta + \frac{M}{L} \\
m\frac{dv_x}{dt} &= -K_z v_z + F_p \text{cos}\theta + mg
\end{cases}
$$

# Résolution

## Simplification

![[Exercice - Drone Asservi Résolution.excalidraw|800x400]]

## Transformée de Laplace

![[Exercice - Drone Asservi Laplace.excalidraw|800x400]]
# Schéma-Bloc
![[Exercice - Drone Asservi Schéma-Bloc.excalidraw|800X400]]

# Fonctions de Transfert
[[Formule de Black]]
![[Exercice - Drone Asservi Application Black.excalidraw|100%]]
![[Exercice - Drone Asservi 2022-10-19 16.18.44.excalidraw|100%]]

![[Exercice - Drone Asservi Epsilon.excalidraw]]
- Q6
$$
\begin{align}
M_{pert} &= 0 \\ \\

\epsilon_{c} = \lim_{ t \to \infty } \epsilon(t) &=^{\mathcal{L}_{}} \lim_{ p \to 0 } p\epsilon^{\sim}  \\
&= \lim_{ p \to 0 } (1-F_{1})V^{\sim}_{x_{c}}
\end{align}
$$
- Q7
$$
\begin{align}
V^{\sim}_{x_{c}} &= 0 \\ \\
\epsilon_{p} &= \lim_{ t \to \infty } \epsilon(t)  \\
&= \lim_{ p \to 0 } \, p \times \frac{-K_{1}(1-\tau_{1}p^{2})(1+\tau_{4}p)}{p^{2}(1+\tau_{2})(1+\tau_{4}) +K_{t}K_{1}K_{2}(1-\tau_{1}p^{2})(1+\tau_{3})}\times \frac{M_{0}}{P} \\
&= -\frac{M_{0}}{K_{t}K_{2}}
\end{align}
$$
