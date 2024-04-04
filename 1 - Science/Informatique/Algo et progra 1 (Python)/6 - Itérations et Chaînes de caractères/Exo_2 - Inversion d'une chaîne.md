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
2. [[6.1.3 - Boucle ''while'']]
3. [[6.1.4 - Chaînes de caractères (python)]]
4. [[6.1.4.1 - Opérateur ''crochets'']]
5. [[6.2.1 - Fonction len()]]

# Exercice 
Ecrire une fonction qui prend une chaîne en argument et qui retourne une chaîne constituée des caractères de la chaîne dont l’ordre est inversé

## Résolution
```python
def invert(w):
	res = '' 
	i = len(s) - 1 
	while i >= 0: 
		res = res + s[i] 
		i = i - 1 
	return res

invert('algorithme')  # 'emhtirogla'
```
