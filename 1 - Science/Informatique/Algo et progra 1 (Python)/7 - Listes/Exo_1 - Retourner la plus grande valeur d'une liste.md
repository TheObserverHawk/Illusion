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
1. [[6.3.2 - Boucle ''for'']]

_Python : Liste_
1. [[Python]]
2. [[7.1.1 - Liste (python)]]

# Exercice
Ecrire une fonction qui retourne la plus grande valeur d’une liste contenant des entiers. 
Précondition : on suppose que la liste n’est pas vide

## Résolution
```python
def max_liste(t): 
	max = t[0] 
	for x in t: 
		if x > max:
			max = x 
	return max
```