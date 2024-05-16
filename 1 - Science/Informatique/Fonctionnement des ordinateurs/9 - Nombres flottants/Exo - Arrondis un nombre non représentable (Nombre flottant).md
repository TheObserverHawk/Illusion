---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1. [[2.3.2 - Représentation binaire]]
2. [[2.3.2.1 - Bit]]


_Fonctionnement des ordinateurs : Nombres flottants_
1. [[9.2.1 - Biais de l'exposant (Représentation en virgule flottant)]]
1. [[9.2.2 - Représentation normalisée (Nombre flottant)]]
2. [[9.3 - Standard IEEE 754 (Nombre flottant)]]
3. [[9.3.2 - Valeur spéciale (IEEE754) (Nombre flottant)]]
4. [[9.3.4 - Arrondis (Rounding) (IEEE 754) (Nombre flottant)]]

# Exo
Soit $M=3, E=2$ et un biais $B=4$. Il n’y a pas de valeurs spéciales ($NaN, +/- ∞$) et seule la représentation normalisée est supportée. 
\
Comment représenter le nombre $x = 0,815$ ?
\
En conversion binaire, on a $$0.1101000010100011110101110…$$ qui n’est pas représentable sur $M=3$ bits. En normalisant, on a $$1.101000010100011110101110…$$ car on a multiplié par 2 i.e. 1 décalage vers la gauche. En arrondissant, on a $$1.101$$ L’exposant $e-B$ doit valoir $-1$, par conséquent $$e=-1+4=3$$ Le nombre arrondi est représenté avec $m=101$ et $e=11$, ce qui correspond à $$x^\prime= \left(1+\frac{5}{2^3}\right).2^{3-4}=\frac{1}{2}+\frac{5}{2^4}=\frac{8+5}{16}=0,8125$$ 
- L’erreur absolue est égale à $$\Delta_x=|x-x^\prime|=|0,815-0,8125|=0,0025$$
- L’erreur relative est égale à $$\epsilon_x=\frac{\Delta_x}{|x|}=\frac{|0,815-0,8125|}{|0,815|}\approx0,003604<\varepsilon_M=2^{-(M+1)}=0,0625$$