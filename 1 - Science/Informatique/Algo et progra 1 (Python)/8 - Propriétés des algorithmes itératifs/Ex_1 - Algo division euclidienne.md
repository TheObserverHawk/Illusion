---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Math discrète : Arithmétique_
1. [[1.1.2 - Division euclidienne]]

_Python : Propriétés des algorithmes itératifs_
1. [[Python]]
2. [[8.1.1 - Preuve d'exactitude d'un algorithme itératif]]
3. [[8.1.2 - Invariant de boucle]]

**Introduction**
Soit $a$ et $b$ deux entiers tels que $a ≥ 0$ et $b > 0$. Comment déterminer le quotient (entier) et le reste de la division de $a$ par $b$ ? 
1. Idée de l’algorithme de division euclidienne : 
	1. Initialiser le reste à $a$. 
	2. Ensuite, soustraire $b$ au reste tant que celui-ci est plus grand que $b$. Le nombre de soustractions est égal au quotient.
# Prouver l'exactitude de l'algorithme division euclidienne  
```python
def division(a, b): 
	r = a 
	q = 0 
	while r >= b: 
		r = r - b 
		q = q + 1 
	return (q, r)
```
## A) la fonction division s’arrête-t-elle toujours ? (preuve de l’arrêt)
Soient $a \ge 0$ et $b >  0$
1. _Cas de base_ :
Soit $a < b$
Dans ce cas, comme $r$ est initialisé à $a$, le test (4) de la boucle est faux donc la boucle n'est jamais exécutée.

2. _Cas général_ :
Par récurrence, supposons que la boucle s'arrête pour tout $r \le k$ où $k \in \mathbb{R_0}$
La boucle s'arrête aussi pour $r = k+1$ car instruction (5) diminue strictement la valeur de $r$ car $b > 0$ et $b$ n'est jamais modifié dans la boucle.

## B) Invariant de boucle
Formule de la division euclidienne : $a = b . q + r$ où
1. $q$ est le quotient
2. $r$ est le reste

Est-ce que $a = b . q + r$ est un invariant de boucle ? 
**Exemple**

| $a$ | $b$ | $q$ (quotient) | $r$ (reste) | Formule : $a = b. q+r$ |
| --- | --- | -------------- | ----------- | ---------------------- |
| 14  | 5   | 0              | 14          | 14 = 5.0 +14           |
| 14  | 5   | 1              | 9           | 14 = 5.1 + 9           |
| 14    | 5    | 2               | 4            | 14 = 5.2 + 4                       |

1. _Initialisation (avant d'entrer dans la boucle)_ :
On sait que $q$ est initialisé à 0 et $r$ est initialisé à $a$
Donc on a $b.q+r=b.0+a=a$, par conséquent l'assertion est vraie

2. _Prouver que c'est vrai après chaque itération de la boucle_ :
Considérons une itération donnée de la boucle et vérifions que l'assertion reste vraie jusqu'à la fin de cette itération.
Les variables $q$ et $r$ étant modifiées dans la boucle, on peut utiliser les notations suivantes :
$q_0$ et $r_0$ : valeurs de $q$ et de $r$ au début de l'itération
$q_1$ et $r_1$ : valeurs de $q$ et de $r$ à la fin de l'itération
Prouvons que l’assertion est toujours vraie après une itération donnée :
Par hypothèse d'induction : $a=b.q_0+r_0$ 
On a $r_0 = r_1 + b$ et $q_0 = q_1-1$ car instructions 5 et 6
Donc $a = b.q_0+r_0= b.(q_1-1)+(r_1+b)$ i.e. $a = b.q_1+r_1$
Par conséquent l'assertion est vraie après l'itération considérée et donc$a = b . q + r$ est bien un invariant de la boucle "`while`".

## C) Après l’exécution de la fonction division les valeurs retournées correspondent elles bien au quotient de $a$ par $b$ et au reste ? (preuve de l’exactitude)
Le résultat retourné est correct car 
1. la boucle se termine quand la condition est fausse i.e. quand $r < b$
2. Vu que $a = b . q + r$ est vrai, alors $q= \frac{a-r}{b}$ et $r < b$, ce qui correspond à la définition du quotient et du reste d'une division

**Conclusion**
La preuve complète de l’exactitude de la fonction division est donc :
1. Preuve d'arrêt : (A)
2. Invariant de boucle : (B)
3. Résultat retourné : (C)