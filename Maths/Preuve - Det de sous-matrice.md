---
dg-publish: true
---

On fait le dessin, et nomme les colonnes $C_{i}$
$$
\text{det}\dots = \text{det}\left(\lambda e_{1}, \alpha_{2}e_{1}+\begin{pmatrix}
0 \\
(C_{1})
\end{pmatrix}, \dots\right)=0+\text{det}\left(\lambda e_{1}, \begin{pmatrix}
0 \\
(C_{1})
\end{pmatrix}, \dots\right)
$$
Puis par linéarité
$$
=\lambda\det \begin{pmatrix}
1 & (0) \\
(0) & (M)
\end{pmatrix}
$$
On montre que $\varphi= M\mapsto \det\begin{pmatrix}1 & (0) \\ (0) & (M)\end{pmatrix}$ est une forme antisymétrique $n-1$ linéaire, alors $\varphi$ est le déterminant.