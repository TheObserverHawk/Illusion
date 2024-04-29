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
1. [[6.2.1 - Fonction len()]]
1. [[6.3.2 - Boucle ''for'']]

_Python : Fichiers et exceptions_
1. [[Python]]
2. [[12.3.3 - Fonction with open()]]
1. [[12.2.1.1 - Méthode 'strip']]

# Exo
Ecrivez un script qui lit le fichier `words.txt` et qui n’affiche que les mots qui ont plus de 20 caractères (sans compter les caractères blancs)

## Résolution
```python
with open('words.txt') as fichier: 
	for line in fichier: 
		word = line.strip() 
		if len(word) > 20: 
			print(word)
```
