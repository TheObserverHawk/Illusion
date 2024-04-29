---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Instruction conditionnelle_
1. [[4.1.2 - Opérateur de comparaison]]
1. [[4.1.5 - Instruction conditionnelle]]

_Python : Itérations et Chaînes de caractères_
1. [[6.1.2 - Incrémenter & Décrémenter]]
1. [[6.3.2 - Boucle ''for'']]

_Python : Fichiers et exceptions_
1. [[Python]]
2. [[12.3.3 - Fonction with open()]]
1. [[12.2.1.1 - Méthode 'strip']]

# Exercice
Ecrivez un script qui lit le fichier `words.txt` et qui n’affiche que le pourcentage de mots qui n'ont pas la lettre "e"

## Résolution
```python
with open('words.txt') as fichier: 
	total = 0 
	cnt = 0 
	for line in fichier: 
		total = total + 1 
		word = line.strip() 
		if not 'e' in word: 
			cnt = cnt + 1 
	percent = cnt / total * 100.0 

print('Pourcentage de mots sans e: %.2f' % percent)
```
