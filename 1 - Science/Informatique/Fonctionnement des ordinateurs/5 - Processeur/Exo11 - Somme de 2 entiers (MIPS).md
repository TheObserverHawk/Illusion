---
## Metadata
tags : 
 - Note_done Note_WIP Informatique
 - 
source : UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1.

_Fonctionnement des ordinateurs : Caractères & Chaînes de caractères_
1.

_Fonctionnement des ordinateurs : Eléments de conception logique_
1.

_Fonctionnement des ordinateurs : Processeur_
1.

_Fonctionnement des ordinateurs : Micro-architecture_
1.

_Fonctionnement des ordinateurs : Assemblage & Compilation_
1.

_Fonctionnement des ordinateurs : Hiérarchie de mémoires_
1.

_Fonctionnement des ordinateurs : Nombres flottants_
1.

# Exo 11
## Enoncé : Dans cet exercice, il vous est demande d’ écrire un programme qui demande deux entiers à l’utilisateur et qui en affiche la somme. Pour demander un entier a l’utilisateur, utilisez l’appel système n°5 ( `read int`). Celui-ci retourne l’entier lu à la console dans le registre `v0`. Si la chaîne ne correspond pas à un entier, l’appel système retourne 0. Nommez votre programme `spim-add-int.s` et testez-le programme avec plusieurs couples d’entiers.
```mips
# Effectue la somme de deux entiers demandes a l’utilisateur. 
# Subtilite : il faut parfois sauvegarder les entiers lus 
# car ils sont ecrases par des syscalls suivants. 
# ici, on utilise $t0 pour cette sauvegarde. 
	.data 
msg1: .asciiz "Entrez le premier entier: " 
msg2: .asciiz "Entrez le second entier: " 
msg3: .asciiz "La somme vaut : " 
endl: .asciiz "\n" 

	.text 
main: 
	la $a0, msg1 
	li $v0, 4 
	syscall 
	
	li $v0, 5 
	syscall 
	move $t0, $v0 
	
	la $a0, msg2 
	li $v0, 4 
	syscal
```