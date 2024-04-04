---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Fonctions_
1. [[3.3.2 - Définition une fonction (python)]]

_Python : Instruction conditionnelle_
1. [[4.1.2 - Opérateur de comparaison]]
2. [[4.1.5 - Instruction conditionnelle]]

_Python : Tuple_
1. [[11.1.1 - Tuple (Python)]]

_Python : POO_
1. [[13.1.3 - Méthode (python)]]
# Exercice
Ecrire une fonction qui permet de trier trois mots, quelle que soit la casse des mots.

## Résolution
```python
def trie2(mot1, mot2): 
	first = mot1 
	second = mot2 
	if mot1.lower() > mot2.lower(): 
		first = mot2 
		second = mot1 
	return (first, second)

trie2('Zebre','elephant')  # ('elephant', 'Zebre')
```
