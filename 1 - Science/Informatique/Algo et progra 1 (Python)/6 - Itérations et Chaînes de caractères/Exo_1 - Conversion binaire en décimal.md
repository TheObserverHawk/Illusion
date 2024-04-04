---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 1
---

Link :
_Python : Types, variables et expressions_
1. [[2.1.1 - Valeur (python)]]

_Python : Fonctions_
1. [[3.3.2 - Définition une fonction (python)]]
2. [[3.3.6 - Valeur None (python)]]

_Python : Instruction conditionnelle_
1. [[4.1.2 - Opérateur de comparaison]]
2. [[4.1.3 - Opérateur logique]]
3. [[4.1.5 - Instruction conditionnelle]]

_Python : Itérations et Chaînes de caractères_
1. [[6.1.2 - Incrémenter & Décrémenter]]
2. [[6.1.3 - Boucle ''while'']]
3. [[6.1.4.1 - Opérateur ''crochets'']]
4. [[6.2.1 - Fonction len()]]
5. [[6.3.1 - Tranche de chaîne]]
# Exercice 
Ecrire une fonction qui prend un nombre binaire (entier) en argument (représenté sous la forme d’une chaîne de caractères) et qui retourne ce nombre en base 10 (sous la forme d’un entier). 
Cette fonction retourne `None` si la chaîne ne représente pas un nombre binaire.

## Résolution
```python
def find(word, letter): 
	i = 0 
	while i < len(word): 
		if word[i] == letter: 
			return i 
		i = i + 1 
	return None

mot = 'banane' 
find(mot, 'a')  # 1


def bin2dec_intPart(b): 
	res = 0 
	i = 0 
	n = len(b) 
	while i < n: 
		if b[n-i-1] == '1': 
			res = res + 2 ** i 
		elif b[n-i-1] != '0': 
			return None 
		i = i + 1 
	return res

bin2dec_intPart('101')  # 5


def bin2dec_fracPart(b): 
	f = 0.0 
	n = len(b) 
	i = 0 
	while i < n: 
		if b[i] == '1': 
			f = f + 1.0 / (2 ** (i+1)) 
		elif b[i] != '0': 
			return None 
		i = i + 1 
	return f

bin2dec_fracPart('01')  # 0.25


def bin2dec(b): 
	indexDot = find(b, '.') 
	if indexDot == None: 
		return bin2dec_intPart(b) 
	i = bin2dec_intPart(b[:indexDot]) 
	f = bin2dec_fracPart(b[indexDot + 1:]) 
	if i != None and f != None: 
		return i + f 
	else: 
		return None

bin2dec('101')  # 5 
bin2dec('.01')  # 0.25 
bin2dec('101.01')  # 5.25 
bin2dec('3.101')  # None
```