---
## Metadata
tags : 
 - Note_done Note_WIP Informatique
 - 
source : UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1.

_Fonctionnement des ordinateurs : Caractères & Chaînes de caractères_
1.

_Fonctionnement des ordinateurs : Eléments de conception logique_
1.

_Fonctionnement des ordinateurs : Processeur_
1.

_Fonctionnement des ordinateurs : Micro-architecture_
1.

_Fonctionnement des ordinateurs : Assemblage & Compilation_
1.

_Fonctionnement des ordinateurs : Hiérarchie de mémoires_
1.

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
**Grâce à l'algorithme normalisation** : 
Soit un nombre $x\neq 0$ 
On souhaite trouver $(m, e)$ tel que $m$ est normalisé (i.e. de la forme 1,…) et $x = m.2^e$ 
```python
m = x 
e = 0 
while m < 1: 
	m = m * 2 
	e = e – 1 
while m >= 2: 
	m = m / 2
	e = e + 1
```
On a donc que 