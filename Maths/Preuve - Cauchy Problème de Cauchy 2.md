---
dg-publish: true
---

On [[Parachute|admet]] avoir déterminé une solution particulière $g$ sur $I$ à l'équation $L_{1}$.

On a donc
$$
S_{L_{1}} = \{ g+y_{h} \;;\; y_{h} \in S_{L_{1_{h}}} \}
$$

On a deux cas

1. Si les deux racines sont simples
$$
S_{L_{1_{h}}} = \{ t \to \lambda_{1}e^{\alpha_{1}t} + \lambda_{2}e^{\alpha_{2}t} \;;\; \lambda_{1},\lambda_{2} \in \mathbb{C} \}
$$

__Analyse__:
On suppose $g(t)+\lambda_{1}e^{\alpha_{1}t}+\lambda_{2}e^{\alpha_{2}t}$ est solution
$$
\begin{cases}
y_{0} &= g(t_{0}) + \lambda_{1}e^{\alpha_{1}t_{0}}+\lambda_{2}e^{\alpha_{2} t_{0}} \\
y_{1} &= g(t_{1}) + \lambda_{1}\alpha_{1}e^{\alpha_{1}t_{1}} + \lambda_{2}\alpha_{2}e^{\alpha_{2}t_{1}} 
\end{cases}
$$
Donc le système suivant:
$$
\begin{cases}
\lambda_{1}e^{\alpha_{1}t_{0}}+\lambda_{2}e^{\alpha_{2}t_{0}} = y_{0} - g(t_{0}) \\
\lambda_{1}\alpha_{1}e^{\alpha_{1}t_{0}}+\lambda_{2}\alpha_{2}e^{\alpha_{2}t_{0}} = y_{1} - g'(t_{0})
\end{cases}
$$
On applique $L_{2} \leftarrow L_{2} - \alpha_{1}L_{1}$ et on remarque un système triangulaire à diagonale non nulle, il existe donc une unique solution.

__Synthèse__:
Toutes les équations sont équivalentes donc la solution est ok

2. Si $\alpha$ est racine double
$$
S_{L_{1_{h}}} = \{ t \to (\lambda_{1}+t\lambda_{0})e^{\alpha t} \;;\; \lambda_{1},\lambda_{2} \in \mathbb{C} \}
$$

__Analyse__:
On suppose $y$ solution.
D'où
$$
\begin{cases}
y_{0} =  g(t_{0})+(\lambda_{1}+t\lambda_{0})e^{\alpha t_{0}} \\
y_{1}=g'(t_{0})+(\lambda_{1}+\alpha(\lambda_{1}t+\lambda_{0}))e^{\alpha t_{0}}
\end{cases}
$$

Donc le système suivant
$$
\begin{cases}
\lambda_{1}t_{0}e^{\alpha t_{0}}=\lambda_{0}e^{\alpha t_{0}} &= y_{0} - g(t_{0}) \\
(\alpha t_{0}+1)\lambda_{1}e^{\alpha t_{0}} + \alpha \lambda_{0}e^{\alpha t_{0}} &=  y_{1} - g'(t_{0})
\end{cases}
$$
De même, avec $L_{2} \leftarrow L_{2}-\alpha L_{1}$ on a un système triangulaire à diagonale non nulle donc une unique solution.

__Synthèse__: équivalences, ok.