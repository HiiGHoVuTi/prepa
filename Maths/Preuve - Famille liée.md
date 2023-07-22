---
dg-publish: true
---

**Récurrence sur** $\mathbb{N}$.

*Initialisation*: ok, attention à séparer $\lambda_{1}=0$.
*Hérédité*: 
Il existe $f_{i}=\lambda_{ij}e_{j}$, $i\leq n+2,j\leq n+1$.
On a un grand système linéaire.
- Si pour $i\in \textlbrackdbl 1,n+2 \textrbrackdbl$, $\lambda_{i,n+1}=0$ alors $f_{1},\dots f_{n+1}\in \text{Vect}(e_{1}\dots e_{n})$ par hypothèse  liée.
- Sinon, on applique le [[Cours Matrices#Opérations Elementaires|pivot de Gauss]]
	
$$
L_{i} \leftarrow L_{i} - \frac{\lambda_{i,n+1}}{\lambda_{n+2,n+1}}
$$
On a alors 

$$
	f_{i}^{\sim}=\sum_{k=1}^{n}\left( \lambda_{i,k}- \frac{\lambda_{i,n+2}}{\lambda_{i,n+1}}\lambda_{n+2,k} \right)x_{k}
$$

Donc $\mathcal{F}^{\sim}=(f_{1}^{\sim}\dots f_{n+1}^{\sim})$ liée par hypothèse de récurrence, donc $\gamma_{1}f_{1}^{\sim}+\dots\gamma_{n+1}f_{n+1}^{\sim}=0$ avec $(\gamma_{1}\dots\gamma_{n+1})\neq (0\dots 0)$.

d'où
$$
\gamma_{1}f_{1}+\dots+\gamma_{n+1}f_{n+1}-\left( \sum_{k=0}^{n+1}\gamma_{k} \frac{\lambda_{k,n+1}}{\lambda_{n+2,n+1}} \right)f_{n+2} = 0
$$


