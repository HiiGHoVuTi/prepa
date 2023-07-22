# Premier cas, $a\in \mathbb{N}$

## Initialisation

Pour $a=0$, ok.

## Hérédité

On suppose $a^{p}\equiv a[p]$

On a par le binôme de Newton:
$$
(a+1)^{p}=\sum_{k=0}^{p}{p \choose k} a^{k} = 1+a^{p} + \sum_{k=1}^{p-1}{p\choose k} a^{k} \equiv 1+a^{p}[p]
$$
congruence par le lemme précédent.

Ainsi, $(a+1)^{p}\equiv 1+a^{p}[p] \equiv 1+a [p]$ par hypothèse de récurrence.

# Second cas, $a\in -\mathbb{N}$

On utilise le théorème pour $-a$ et comme $p$ premier (donc impair), on a $-a^{p}=(-a)^{p}$

# Dernier cas, $p=2$

On a $a^{2}=-a[2]$ et $a^{2}\equiv a[2]$. Donc c'est bon !


