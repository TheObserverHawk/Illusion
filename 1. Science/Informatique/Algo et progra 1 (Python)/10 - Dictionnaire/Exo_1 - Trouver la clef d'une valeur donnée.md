---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Instruction conditionnelle_
1. [[4.1.2 - Opérateur de comparaison]]
2. [[4.1.5 - Instruction conditionnelle]]

_Python : Itérations et Chaînes de caractères_
1. [[6.3.2 - Boucle ''for'']]

_Python : Liste_
1. [[7.1.1 - Liste (python)]]
2. [[7.2.1 - Méthode 'append']]

_Python : Dictionnaire_
1. [[Python]]
2. [[10.1.1 - Dictionnaire (Python)]]

# Exercice
Comment trouver la (les) clef(s) d’une valeur donnée ?

## Résolution
```python
def get_keys(d, value): 
	res = [] 
	for k in d: 
		if d[k] == value: 
			res.append(k) 
	return res 
	
months = {'Jan' : 31, 'Feb' : 28, 'Mar' : 31, 'Apr' : 30, 'May' : 31, 'Jun' : 30, 'Jul' : 31, 'Aug' : 31, 'Sep' : 30, 'Oct' : 31, 'Nov' : 30, 'Dec' : 31} 
print('Months with 31 days:', get_keys(months, 31)) 
# Months with 31 days: ['Jan', 'Jul', 'Mar', 'Aug', 'Dec', 'May', 'Oct']
```