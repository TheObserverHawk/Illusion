---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Propriétés des algorithmes itératifs_
1. [[Python]]
2. [[8.1.1 - Preuve d'exactitude d'un algorithme itératif]]
3. [[8.1.2 - Invariant de boucle]]

**Introduction**
Soit $a$ un nombre réel et $n$ un entier $≥ 0$. Comment calculer $a^n$ ? 
1. Approche classique : utiliser une boucle pour calculer $a×a×...×a$, ce qui revient à faire $n−1$ multiplications 
2. Exponentielle rapide : exploiter le fait que 
	1. si $n$ est pair, alors $a^n = (a^2 )^{\frac{n}{2}}$ 
	2. si $n$ est impair, alors $a^n = a · a^{n−1}$ 
		1. _Exemple_ : $a^9 = a · a^8 = a · (a^2 )^4 = a ·((a^2 )^2 )^2$, ce qui revient à 4 multiplications au lieu de 8

# Prouver l'exactitude de l'algorithme calcul de l'exposant
```python
def expo(a, n): 
	r = 1 
	b = a 
	i = n 
	while i > 0: 
		if i % 2 == 0: 
			b = b * b 
			i = i // 2
		else: 
			r = r * b 
			i = i - 1 
	return r

expo(3,3)  # 27 
expo(2,0)  # 1
```

## A) Preuve d'arrêt
Soit $n ≥ 0$. Par récurrence sur $n$.
1. _Cas de base_ :
Si $n = 0$, la boucle n’est pas exécutée

2. _Cas général_ :
Soit $n > 0$ 
Par récurrence, supposons que la boucle s’arrête pour tout $i ≤ n−1$ ;  
1. Si $i$ est pair, l’instruction (8) i.e. `i = i//2` diminue strictement sa valeur ; 
2. Si $i$ est impair, l’instruction (11) i.e. `i = i-1` diminue strictement sa valeur ;

Par induction, la boucle s’arrête donc également quand $i = n$.

## B) Invariant de boucle
Montrons que l’assertion suivante est un invariant de la boucle `while` : $$a^n = r · b^i$$
**Exemple**

| $r$ | $b$ | $i$ | Formule : $r . b^i$ |
| --- | --- | --- | ------------------- |
| 1   | 2   | 9   | $1.2^9=512$         |
| 2   | 2   | 8   | $2.2^8 = 512$       |
| 2   | 4   | 4   | $2.4^4 =512$        |
| 2   | 16  | 2   | $2.16^2 = 512$      |
| 2   | 256 | 1   | $2.256^1 =512$      |
| 512    | 256    | 0    | $512.256^0=512$                    |
1. Si $i$ est pair
	1. $r_1 = r_0$
	2. $b_1 = b_0^2$ 
	3. $i_1 = \frac{i_0}{2}$ 
2. Si $i$ est impair
	1. $r_1 = r_0 . b_1$ 
	2. $b_1 = b_0$ 
	3. $i_1 = i_0 -1$ 

### _Initialisation (avant d'entrer dans la boucle)_ :
L’initialisation des variables (instr. 2 à 4) donne $r · b^i = 1 · a^n = a^n$ et l’assertion est vraie.

### _Prouver que c'est vrai après chaque itération de la boucle_ :
Considérons une itération donnée de la boucle et vérifions que l’assertion reste vraie à la fin de cette itération.
Les variables $a$ et $n$ ne sont pas modifiées par la boucle. 
On va utiliser les notations $i_0$, $b_0$ et $r_0$ pour les valeurs des variables $i$, $b$ et $r$ au début de l’itération et $i_1$, $b_1$ et $r_1$ pour leurs valeurs à la fin de l’itération.

_Par hypothèse d'induction_ : $a^n = r_0 . b_0^{i_0}$ 
1. Si $i_0$ est pair, alors
	1. les instr. 7 et 8 donnent $b_0 = √ b_1, i_0 = 2i_1$ et $r_0 = r_1$
	2. Donc, $a^n = r_0 · b^{i_0}_0 = r_1 · √ b_1^{2i_1} = r_1 · b^{\frac{1}{2} ·2i_1}_1 = r_1 · b^{i_1}_1$ 
2. Si $i_0$ est impair, alors
	1. les instr. 10 et 11 donnent $b_0 = b_1, i_0 = i_1 +1$ et $r_0 = \frac{r_1}{b_1}$ 
	2. Donc, $a^n = r_0 · b^{i_0}_0 = \frac{r_1}{b_1}.b_1^{(i_1+1)}= \frac{r_1}{b_1}.b_1.b_1^{i_1} =r_1.b_1^{i_1}$ 

Quelle que soit la parité de $i_0$, l’assertion reste vraie après l’itération considérée et $a^n = r · b^i$ est donc bien un invariant de la boucle

## C) Preuve de l’exactitude
La preuve complète de l’exactitude de la fonction expo est donc : 
1. preuve de l’arrêt : (A)
2. preuve que $a^n = r · b^i$ est un invariant de la boucle : (B) 
3. Preuve de l'exactitude i.e. le résultat retourné (valeur de $r$) est correct car :
	1. quand la boucle se termine, on a $i = 0$ ;
	2. après la boucle, l’invariant devient donc : $$r =\frac{a^n}{b^i}= \frac{a^n}{b^0}= \frac{a^n}{1}=a^n$$
	3. la valeur retournée est donc bien $a^n$ .