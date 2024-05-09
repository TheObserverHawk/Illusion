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

_Fonctionnement des ordinateurs : Micro-architecture_
1.

_Fonctionnement des ordinateurs : Assemblage & Compilation_
1.

_Fonctionnement des ordinateurs : Hiérarchie de mémoires_
1.

_Fonctionnement des ordinateurs : Nombres flottants_
1.

# Exo 12
Dans cet exercice, il vous est demandé de produire un programme qui demande, en boucle, un entier à l’utilisateur : 
1. Si cet entier est inférieur à 0, la boucle se termine. 
2. Si l’entier est strictement supérieur à 10, la chaîne de caractères ≪ `trop grand` ≫ est affichée à la console. 
3. Sinon, la chaîne de caractères  ≪ `valeur acceptee` ≫ est affichée à la console. 

Ce programme commence à devenir plus complexe. Il devrait s’étaler sur environ 30 lignes. Assurez-vous de bien le structurer, en employant l’indentation à bon escient, en insérant des lignes vides pour séparer les différentes tâches et en ajoutant éventuellement des commentaires (en utilisant le caractère spécial `#`).

- Pour demander un entier à l’utilisateur, utilisez l’appel système n°5 comme dans l’exercice 2.4. 
- Pour adapter le comportement du programme aux entiers fournis par l’utilisateur, il faut réaliser des comparaisons et l’équivalent de `if`/`else`, à l’aide d’instructions de branchement conditionnel telles que `beq` (branch on equal), `bne` (branch on not equal), `blt` (branch on less than), etc... 
- Pour afficher les chaînes de caractères, utilisez l’appel système n°4 comme dans l’exercice 2.3. 

Nommez votre programme `spim-read-int.s` et vérifiez-en le bon fonctionnement en le chargeant et l’exécutant à l’aide de SPIM. Fournissez des valeurs differentes permettant de tester toutes les conditions du programme.
### Résolution de l'exo 12
```mips
	.data 
msg1: .asciiz "Entrez un entier:\n" 
msg2: .asciiz "Trop grand.\n" 
msg3: .asciiz "Valeur acceptee: " 
endl: .asciiz "\n" 


	.text 
main: 
	la $a0, msg1 
	li $v0, 4 
	syscall 
	
	li $v0, 5 
	syscall 
	move $t0, $v0 
	
	bltz $v0, end_loop 
	bgt $v0, 10, too_large 
	
	la $a0, msg3 
	li $v0, 4 
	syscall 
	
	move $a0, $t0
	li $v0, 1 
	syscall 
	
	la $a0, endl 
	li $v0, 4 
	syscall 
	j main 

too_large: 
	la $a0, msg2 
	li $v0, 4 
	syscall 
	j main 

end_loop: 
	jr $ra
```