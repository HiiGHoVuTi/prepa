---
dg-publish: true
---

On le montrera pour une colonne, par antisymétrie on les a toutes. Par transposition on a les lignes.

$$
\begin{align}
\det \begin{pmatrix}
m_{11}&\dots&m_{12} \\
\vdots & & \vdots \\
m_{n 1} & \dots & m_{nn}
\end{pmatrix} &= \sum_{i} m_{i 1} \det \begin{pmatrix}
0 & m_{12} & \dots \\
\vdots &  &  \\
1 &  & \\ 
\vdots & & \\
0 &m_{n 1} &\dots
\end{pmatrix}
\end{align}
$$

On change le $1$ de place si nécessaire et remet les autres colonnes dans l'ordre, le $(-1)^{i+j}$ apparaît (ici $j=1$).
On utilise le théorème [[Preuve - Det de sous-matrice|de det de sous-matrice]].
