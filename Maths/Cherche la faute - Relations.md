#maths #exercice #ensembles 


# Ceci est faux, trouvez pourquoi
Montrons que si une relation R sur A est transitive et symétrique, elle est réflexive.

- Considérons x,y∈A tels qque $xRy$.
- Par symétrie, on a aussi $yRx$.
- Alors par transitivité, on a $xRx$.

# Correction
Ceci est faux car rien ne nous garantit qu'il existe toujours un $y$ tel qque $xRy$.
En fait, pour que la propriété souhaitée soit démontrée, il nous faut les quantificateurs suivants: $\forall x \exists y$. Or aucune des hypothèses ne nous donne l'existance de $y$.
L'argument suppose sa conclusion, elle est donc circulaire et **fausse**.