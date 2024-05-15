---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Caractères & Chaînes de caractères_
1. [[3.2 - American Standard Code for Information Interchange (ASCII)|3.2 - American Standard Code for Information Interchange (ASCII)]]

_Fonctionnement des ordinateurs : Processeur_
1. [[5.4 - Architecture MIPS]]
2. [[5.4.2 - Registre d'usage général (GPR)]]
3. [[5.4.3 - Directives d'assemblage (MIPS)]]
4. [[5.4.4 - Etiquette (MIPS)]]
5. [[5.4.5 - Pseudo-instruction (MIPS)]]
6. [[5.4.6 - Jeu d'instructions (MIPS)]]
7. [[5.4.6.3.1 - Instruction Add Word (ADD) (MIPS)]]
8. [[5.4.6.3.5 - Instructions de type-R (MIPS)]]
9. [[5.4.6.12.2.1 - Instruction Jump And Link (JAL) (MIPS)]]
10. [[5.4.6.13 - Appel de systèmes (Syscall) (MIPS)]]

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

	li $v0, 5 
	syscall 
	
	add $t0, $t0, $v0 
	
	la $a0, msg3 
	li $v0, 4 
	syscall 
	
	move $a0, $t0 
	li $v0, 1 
	syscall 
	
	la $a0, endl 
	li $v0, 4 
	syscall 
	
	jr $ra
```