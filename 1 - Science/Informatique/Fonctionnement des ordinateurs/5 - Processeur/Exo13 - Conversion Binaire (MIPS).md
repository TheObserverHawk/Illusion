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
7. [[5.4.6.3.5 - Instructions de type-R (MIPS)]]
8. [[5.4.6.3.6 - Instructions de type-I (MIPS)]]
9. [[5.4.6.8.1 - Instruction de Type-J (MIPS)]]
10. [[5.4.6.8.2 - Instruction Jump (MIPS)]]
11. [[5.4.6.11 - Branchement conditionnel (MIPS)]]
12. [[5.4.6.11.1 - Pseudo-instruction de branchement conditionnel (MIPS)]]
13. [[5.4.6.12.2.1 - Instruction Jump And Link (JAL) (MIPS)]]
14. [[5.4.6.13 - Appel de systèmes (Syscall) (MIPS)]]

# Exo13
Dans cet exercice, il vous est demande d’écrire un programme qui demande un entier à l’utilisateur et qui affiche cet entier en binaire. Utilisez à cet effet la méthode effectuant des divisions euclidiennes successives, vue au Chapitre 2 du cours. Pour résoudre cet exercice, vous aurez besoin de l’instruction `divu x, y`. 
\
Pour rappel, cette instruction calcule le quotient et le reste de la division de $x$ par $y$ (en considérant que ces nombres sont non-signés). Le quotient est placé dans le registre `LO` tandis que le reste est place dans le registre `HI`. Votre algorithme peut produire les bits de la représentation binaire en commençant par le bit de poids le plus faible. ´ Placez le programme résultant dans un fichier nommé `spim-to-binary.s`. Testez ce programme avec plusieurs nombres naturels.
### Résolution
#### Solution 1
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
	# Operation bit-à-bit avec "and"
	
	li $v0, 1 
	syscall 
	li $a2, 1 
	srl $a1, $a1, $a2 
	# Subit un décalage d'une unité vers la droite de la représentation binaire stockée dans $a1

	bne $a1, $zero, non_zero 
	
end: 
	la $a0, endl 
	li $v0, 4 
	syscall 
	jr $ra
```
#### Solution 2
```mips
# Conversion en binaire avec masque binaire 

	.data 
endl: .asciiz "\n" 

	.text 
main: 
	li $v0, 5 
	syscall 
	move $a1, $v0
	
	li $a2, 1 
	li $a3, 31 
	sll $a2, $a2, $a3 
loop: 
	and $a3, $a1, $a2 
	bne $a3, $zero, is_one 
is_zero: 
	li $a0, 0 
	b print_int 
is_one: 
	li $a0, 1 
	
print_int: 
	li $v0, 1 # print_int 
	syscall 
	
	srl $a2, $a2, 1 
	bne $a2, $zero, loop 
	
	la $a0, endl 
	li $v0, 4 
	syscall 
	
	jr $ra
```
