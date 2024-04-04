---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Fonctions_
1. [[3.3.2 - Définition une fonction (python)]]

_Python : Instructions conditionnelle_
1. [[4.1.5 - Instruction conditionnelle]]
2. [[4.2.1 - Fonction input()]]

_Python : Itérations et Chaînes de caractères_
1. [[6.1.2 - Incrémenter & Décrémenter]]
2. [[6.3.2 - Boucle ''for'']]
3. [[6.3.3 - Opérateur ''in'']]

_Python : Liste_
1. [[Python]]
2. [[7.1.1 - Liste (python)]]
3. [[7.2.1 - Méthode 'append']]
4. [[7.2.3 - Méthode 'sort']]
5. [[7.2.4 - Méthode 'isalnum']]
6. [[7.2.5 - Méthode 'split']]
7. [[7.2.8 - Méthode 'lower']]

_Python : Fichiers et exceptions_
1. [[12.3.3 - Fonction with open()]]

# Exercice
1. Ecrire un script qui demande à l’utilisateur le nom d’un fichier de texte (.txt), affiche les mots contenus dans le fichier par ordre alphabétique (en minuscules). 
2. Un même mot ne peut pas être affiché deux fois. 
3. Tous les caractères qui ne sont pas des lettres ou des chiffres seront supprimés dans la création de la liste de mots.

## Résolution
```python
def clean(s): 
	res = ''
	for letter in s: 
		if letter.isalnum(): 
			res = res + letter 
	return res.lower()

clean('He#23.?6Xth')  # he236xth


filename = input('Nom du fichier: ') 
with open(filename) as file: 
	wordsList = [] 
	for line in file: 
		for word in line.split(): 
			cleanWord = clean(word) 
			if not cleanWord in wordsList:
				wordsList.append(cleanWord)

wordsList.sort() 
print(wordsList)
```