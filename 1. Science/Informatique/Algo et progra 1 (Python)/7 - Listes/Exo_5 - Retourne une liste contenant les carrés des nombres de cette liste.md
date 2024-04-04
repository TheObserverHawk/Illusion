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
5. [[7.3.2 - Fonction map()]]
6. [[7.3.3 - Fonction filter()]]
7. [[7.3.4 - Fonction lambda]]

# Définition
Ecrire une fonction qui, à partir d’une liste d’entiers en entrée, retourne une liste contenant les carrés des nombres de cette liste, mais uniquement si ceux-ci se terminent par le chiffre 6.
Challenge : le corps de votre fonction peut être écrit en une seule ligne !

## Résolution
```python
# Version longue
def square(x): 
		return x ** 2 
	
	def six_ended(x): 
		return x % 10 == 6 
		
	def six_ended_squares(t): 
		squares = list(map(square, t)) 
		res = list(filter(six_ended, squares)) 
		return res 
	
print(six_ended_squares(list(range(100))))


# Version une seule ligne 
def six_ended_squares(t): 
	return list(filter(lambda x: x % 10 == 6, list(map(lambda x: x ** 2, t)))) 

print(six_ended_squares(list(range(100))))
```