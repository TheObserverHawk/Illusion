---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Fonctions_
1. [[3.3.2 - Définition une fonction (python)]]

_Python : Itérations et Chaînes de caractères_
1. [[6.1.2 - Incrémenter & Décrémenter]]
2. [[6.2.2 - Fonction range()]]
3. [[6.3.2 - Boucle ''for'']]

_Python : Liste_
1. [[Python]]
2. [[7.1.1 - Liste (python)]]
3. [[7.2.1 - Méthode 'append']]
4. [[7.3.1 - Fonction list()]]

# Exo
Ecrire une fonction 
1. qui prend une liste de nombres entiers en paramètres et 
2. qui retourne la somme cumulative, c-à-d une nouvelle liste telle que l’élément d’indice $i$ soit la somme des $i +1$ premiers éléments. 
	1. Par exemple, la somme cumulative de $[1,2,3]$ est $[1,3,6]$.

## Résolution
```python
def cumul_sum(t): 
	res = [] 
	s = 0 
	for x in t: 
		s += x 
		res.append(s) 
	return res 
	
cumul_sum([1,2,3])  # [1, 3, 6] 
cumul_sum(list(range(10)))  
# [0, 1, 3, 6, 10, 15, 21, 28, 36, 45]
```