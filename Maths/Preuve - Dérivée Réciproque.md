---
dg-publish: true
---

Soit $x\in f(I)$

On considère $A=\frac{f^{-1}(x+h)-f^{-1}(x)}{h}$. 

On pose $k=f^{-1}(x+h)-f^{-1}(x) \to 0$ (car $f^{-1}$ continue).

On remarque que $f(f^{-1}(x)+k)=f(f^{-1}(x+h))=x+h$.

En réarrangeant,

$$
A= \frac{k}{f(f^{-1}(x)+k)-f(f^{-1}(x))}
$$
Or $f$ est dérivable sur $I$ donc $f$ est dérivable en $f^{-1}(x)$ ainsi $\frac{1}{A} \to f'(f^{-1}(x))$ par la formule usuelle.
On passe par l'inverse pour obtenir la limite de $A$.
