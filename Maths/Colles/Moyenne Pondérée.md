---
dg-publish: true
chapitres: Analyse
difficulté: ⭐⭐⭐
---

Soient $t\in \mathbb{R}_{+}^{*}$, $(a_{1},\dots,a_{\ell})\in \mathbb{R^{*}_{+}}^{\ell}$ et $(m_{1},\dots m_{\ell})\in \mathbb{R^{*}_{+}}^{\ell}$ vérifiant $\sum_{i} m_{i}=1$. La moyenne des $p$ points pondérés $(a_{i},m_{i})$ d'ordre $t$ est définie par:
$$
\mu(t)=\left( \sum_{i=1}^{p}m_{i}(a_{i})^{t} \right)^{1/t}
$$
Et on pose aussi:
$$
\mu(0)= \prod_{i=1}^{p} (a_{i})^{m_{i}}
$$
1. Montrer que pour $t>1$ on a $\mu(t)\geq\mu(1)$ avec égalité si et seulement si tous les $a_{i}$ sont égaux
> Utiliser $x \mapsto x^{t}$

En déduire que pour $t>s>0$ on a $\mu(t)>\mu(s)$
2. Prouver que $\forall t\in \mathbb{R}^{*}_{+}, \mu(t)\geq\mu(0)$, préciser les cas d'égalité.
3. Montrer que $\mu$ est soit strictement croissante soit constante sur $\mathbb{R}_{+}$.
