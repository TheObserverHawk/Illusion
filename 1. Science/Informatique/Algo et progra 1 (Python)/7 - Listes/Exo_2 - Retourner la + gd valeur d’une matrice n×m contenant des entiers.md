---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Instructions conditionnelle_
1. [[4.1.2 - Opérateur de comparaison]]
2. [[4.1.5 - Instruction conditionnelle]]

_Python : Itérations et Chaînes de caractères_
1. [[6.2.2 - Fonction range()]]
1. [[6.3.2 - Boucle ''for'']]

_Python : Liste_
1. [[Python]]
2. [[7.1.1 - Liste (python)]]
3. [[7.1.2 - Liste multidimensionnelle]]

# Exercice
Ecrire une fonction qui retourne la plus grande valeur d’une matrice $n×m$ contenant des entiers. 
Précondition : on suppose que $n$ et $m$ sont $≥ 1$ et que la matrice donnée en entrée est correctement codée (c’est à dire une liste de $n$ listes de $m$ entiers).

## Résolution
```python
def max_matrix(A): 
	n = len(A) 
	m = len(A[0]) 
	max = A[0][0] 
	for i in range(n): 
		for j in range(m): 
			if A[i][j] > max: 
				max = A[i][j] 
	return max 

A = [[1, 5, 3], [4, 2, 2], [3, 7, 9], [6, 8, 9]] print(max_matrix(A))  # 9
```