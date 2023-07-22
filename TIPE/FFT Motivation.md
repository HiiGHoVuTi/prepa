# Côté Maths

## Convolution Discrète

$$
f_{e}(i,j) = \begin{cases}
0 \text{ si }i,j \text{ hors-bornes}\\
f(i,j) \text{ sinon}
\end{cases}
$$

$$
(f_{e} * g_{e})(i,j) = \sum_{n=0}^{N} \sum_{m=0}^{M} f_{e}(n,m)g_{e}(i-n, j-m) 
$$

## Lien avec la convolution

1. Obtenir une convolution 
$F \{f(x,y) g(x,y)\} = F(u,v) ∗ G(u,v)$

2. Transformation en produit
$F \{f(x,y) ∗ g(x,y)\} = F(u,v) G(u,v)$

# Applications

## Réduction de bruit

```python
# x est le signal d'entrée
freq = fft(x)
freq[freq < dernier_quartile(freq)] = 0
x_debruite = ifft(freq)
```
