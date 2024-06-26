---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1. [[2.3.2.1 - Bit]]

_Fonctionnement des ordinateurs : Nombres flottants_
1. [[9.1 - Représentation d'un nombre flottant en virgule fixe (fixed point)]]
1. [[9.2.2 - Représentation normalisée (Nombre flottant)]]
2. [[9.2.1 - Biais de l'exposant (Représentation en virgule flottant)]]
3. [[9.3 - Standard IEEE 754 (Nombre flottant)]]
4. [[9.3.2 - Valeur spéciale (IEEE754) (Nombre flottant)]]

# Exo
Nous utilisons une représentation similaire à IEEE 754, avec des tailles réduites de mantisse et d'exposant
\
Soit $M=3, E=2$ et un biais $B=4$. Il n’y a pas de valeurs spéciales ($NaN, +/- ∞$) et seule la représentation normalisée est supportée. 
\
Comment représenter les nombres suivants :
- 1,5 ?
- 0,625 ?
- 0,825 ?

### Cas 1 : 1,5
Comme on a $1,5$, c'est une représentation normalisée car $1$. La représentation normalisé est définie par $$x=(-1)^{{\color{purple}S}}.\left(1+\frac{{\color{red}m}}{2^{\color{red}M}}\right).2^{{\color{lightgreen}e}-{\color{blue}B}}\quad\text{ où }\begin{cases}0\le {\color{red}m}\le2^{\color{red}M}-1\\0< {\color{lightgreen}e}<2^{{\color{lightgreen}E}}-1\end{cases}$$ L'objectif est représenter en $1,5$ en représentation normalisée : $$1,5=(-1)^{{\color{purple}S}}.\left(1+\frac{{\color{red}m}}{2^{\color{red}M}}\right).2^{{\color{lightgreen}e}-{\color{blue}B}}$$ En sachant que $1,5=1+0,5=1+\frac{1}{2}$, on doit faire en sorte que $$e-B=0$$ Or, on a que $B=4$ et $0\le e\le 3$ donc $$e-B\neq 0$$ Le nombre ne peut être représenté en représentation normalisée avec $M=3, E=2$ et $B=4$. Sinon en conversion binaire, on a `1.1` (déjà normalisée)

### Cas 2 : 0,625
Comme on sait que $$0,625=0,5+0,125=\frac{1}{2}+\frac{1}{8}$$ donc en conversion binaire, on a `0.101` car $x={\color{purple}m}.2^{{\color{orange}-M}}=\frac{{\color{purple}m}}{2^{\color{orange}M}}$ donc $e=0$ i.e. `00`. On peut normaliser cette représentation binaire, on obtient donc `1.01` car on multiplie le nombre par $2$ i.e. un décalage d'une unité vers la gauche et on soustrait un bit dans l'exposant $e$ de $E$ bits donc $e=-1$ i.e. `11` qui est équivalent à $e=3$. Donc on peut utiliser la représentation normalisée, on a $$x=(-1)^{{\color{purple}S}}.\left(1+\frac{{\color{red}m}}{2^{\color{red}M}}\right).2^{{\color{lightgreen}e}-{\color{blue}B}}\quad\text{ où }\begin{cases}0\le {\color{red}m}\le2^{\color{red}M}-1\\0< {\color{lightgreen}e}<2^{{\color{lightgreen}E}}-1\end{cases}$$ Il faut que $$0,625=\frac{1}{2}+\frac{1}{8}=(-1)^{{\color{purple}S}}.\left(1+\frac{{\color{red}m}}{2^{\color{red}M}}\right).2^{{\color{lightgreen}e}-{\color{blue}B}}$$ l’exposant $e-B$ doit valoir $-1$, par conséquent $$e=-1+4=3$$ Le nombre peut être représenté avec $m=010$ et $e=11$ 
### Cas 3 : 0,815
Grâce à l’algorithme suivant : 
```python
# Précondition : x < 1

w = "" 
bits = 0 
while x > 0 and bits < M: 
	x = x * 2 
	bits += 1 
	if int(x) > 0: # retourne la partie entière
		x = x – 1 
		w = w + "1" 
	else: 
		w = w + "0"
```
On obtient en binaire : $$0.1101000010100011110101110$$ Impossible à représenter exactement sur $M=3$ bits
