## 1.
$$
\begin{align}
i&=C \frac{du}{dt} \\
E &= Ri+u \\
E &= RC \frac{du}{dt} + u 
\end{align}
$$
[[TD - Rendement Condensateur 1.excalidraw]]
[[TD - Rendement Condensateur 2.excalidraw]]
$$
\begin{align}
E_{c} &= \int^{+\infty}_{0} P(t) \, dt \\
&= \left[ \frac{1}{2}Cu²(t) \right]_{t=0}^{+\infty} \\
&=\frac{1}{2}CE²
\end{align}
$$

$$
\begin{align}
p &= ui \\
&= Rii \\
&= Ri² = \frac{dE_{J}}{dt} \\ \\

E_{J} &= \int_{0}^{+\infty} Ri² \, dt \\
&=  R \int \frac{E²}{R²} e^{-2t/\tau} \, dt  \\
&= \frac{E²}{E} \left[ -t \frac{e^{-2t/\tau}}{2} \right] \\
&= \frac{CE²}{2}
\end{align}
$$
$$
E_{G} = E_{C} + E_{J} \iff CE² = \frac{1}{2} CE² + \frac{1}{2} CE²
$$
>ok.

On voit alors que la moitié de l'énergie a été perdue par effet Joule.
$$
\eta = \frac{E_{C}}{E_{G}} = \frac{1}{2}
$$

Idem que les questions précédentes.

$$E_{C_{1}} = \frac{CE²}{4}$$ et $$E_{G_{1}} = \frac{CE²}{8}$$

$\dots$

$$
\begin{align}
\rho &= E_{C_{1}} + E_{C_{2}} \\
&= \dots \\
&= \frac{2}{3}
\end{align}
$$
