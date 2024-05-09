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

# Exo13
Dans cet exercice, il vous est demande d’écrire un programme qui demande un entier à l’utilisateur et qui affiche cet entier en binaire. Utilisez à cet effet la méthode effectuant des divisions euclidiennes successives, vue au Chapitre 2 du cours. Pour résoudre cet exercice, vous aurez besoin de l’instruction `divu x, y`. 
\
Pour rappel, cette instruction calcule le quotient et le reste de la division de $x$ par $y$ (en considérant que ces nombres sont non-signés). Le quotient est placé dans le registre `LO` tandis que le reste est place dans le registre `HI`. Votre algorithme peut produire les bits de la représentation binaire en commençant par le bit de poids le plus faible. ´ Placez le programme résultant dans un fichier nommé `spim-to-binary.s`. Testez ce programme avec plusieurs nombres naturels.
### Résolution
```mips
# Conversion en binaire avec div. euclid. 

	.data 
endl: .asciiz "\n"

	.text 
main: 
	li $v0, 5 
	syscall 
	move $a1, $v0 
	
	bne $a1, $zero, non_zero   
	# Vérifie si la valeur dans le registre $a1 != $zero
	# Si oui, alors branchement vers non_zero
	
	li $v0, 1
	li $a0, 0 
	syscall 
	b end 
	
non_zero: 
	andi $a0, $a1, 1 
	li $v0, 1 
	syscall 
	li $a2, 1 
	srl $a1, $a1, $a2 
	bne $a1, $zero, non_zero 
	
end: 
	la $a0, endl 
	li $v0, 4 
	syscall 
	jr $ra
```