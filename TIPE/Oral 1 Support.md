
# TIPE

Graphes d'interaction et $\lambda-$calcul

---

#### Pourquoi ?

- FFT sans `float`
- HVM
- $\beta-$optimalité
![[Complexité HVM.png.png]]
---

###### Recherche et documents d'appui

- Calcul d'interaction (Yves Lafont au CNRS)
- Combinateurs d'interaction 
![[Règles Equivalence IC.png]]
---

###### $\beta-$optimalité 

- "Abstract Algorithm" optimal
![[inet-simulation.gif]]

---

###### Implémentation Machine

- Réseaux comme graphes 
![[TIPE Example Code Comment#^e4d89a]]
- Le problème du clonage
	- Partage de travail
	- Clonage incrémental de $\lambda$-abstractions


---

###### Représentation des données en machine

- Bloc de mémoire
- Scott Encodings
![[Scott Encoding#^7c3f29]]
- Nombres Complexes comme arbres
![[TIPE roots of unity.png]]

---

##### Fusion 

- Composition de fonctions fusibles en $\mathcal{O}(\log n)$
- Economie de mémoire ($\mathcal{O}(1)$ additionnel)

---

#### Expériences

>[!todo] à compléter

---

###### Applications 

- Réseaux de Preuves
- Transformée de Fourier Rapide
- Parallélisation (GPU ?)
