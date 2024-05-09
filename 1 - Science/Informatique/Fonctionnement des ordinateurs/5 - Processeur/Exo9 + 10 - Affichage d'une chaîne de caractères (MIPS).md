---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1. [[../2 - Représentation des nombres naturels & entiers/2.3.3 - Représentation hexadécimale|2.3.3 - Représentation hexadécimale]]

_Fonctionnement des ordinateurs : Caractères & Chaînes de caractères_
1. [[../3 - Caractères & Chaînes de caractères/3.2 - ASCII|3.2 - ASCII]]

_Fonctionnement des ordinateurs : Eléments de conception logique_
1. [[../4 - Eléments de conception logique/4.6.6.4.2 - Adressage de données multi-octets (Endianness)|4.6.6.4.2 - Adressage de données multi-octets (Endianness)]]

_Fonctionnement des ordinateurs : Processeur_
1. [[5.4 - Architecture MIPS]]
2. [[5.4.2 - Registre d'usage général (GPR)]]
3. [[5.4.3 - Directives d'assemblage (MIPS)]]
4. [[5.4.4 - Etiquette (MIPS)]]
5. [[5.4.5 - Pseudo-instruction (MIPS)]]
6. [[5.4.6 - Jeu d'instructions (MIPS)]]
9. [[5.4.6.12.2.1 - Instruction Jump And Link (JAL) (MIPS)]]
10. [[5.4.6.13 - Appel de systèmes (Syscall) (MIPS)]]

# Exo 9 + Exo 10
Dans cet exercice, il vous est demandé d’utiliser l’appel système n°4 ( `print string`, Section A.5) afin d’afficher la chaîne de caractères de votre choix à la console. Cet appel système prend un seul argument qui est l’adresse du premier caractère de la chaîne à afficher. Cet argument est passe dans le registre `a0`.
\
La première étape pour résoudre cet exercice est de définir une chaîne de caractères en mémoire. La Figure 5 illustre la représentation  en mémoire de la chaîne de caractères ≪ `Hello World of MIPS` ≫. Chaque caractère est représenté par son code ASCII et occupe un octet  en mémoire. Par exemple, le caractère ’`H`’ est représenté par le code ASCII `0x48`. Les codes des caractères successifs de la chaîne sont places en mémoire à des adresses consécutives. Ainsi, dans l’exemple, le premier caractère est stocké à l’adresse `0x10010000`, le second à l’adresse `0x10010001`, etc... Ces adresses peuvent être différentes dans votre programme. Un label `str` permet de designer l’adresse du premier caractère de la chaîne, soit `0x10010000`. 
\
Il est important de remarquer que la longueur de la chaîne n’est pas stockée en mémoire. En revanche, la fin de la chaîne est indiquée par le code `0`. Ce code est visible a la Figure 5 : le dernier caractère de la chaîne, ’`S`’, est suivi par le code `0`. Cette représentation de chaînes de caractères est appelée chaîne à zéro terminal (nul/zero-terminated string).
**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240509135403.png]]
Définir une telle chaîne en mémoire peut être réalisée à l’aide de directives du langage d’assemblage (voir Section A.2), comme montré à la Figure 6. La directive `.asciiz` crée une chaîne à zéro terminal en mémoire, sur base d’un littéral chaîne de caractères entouré de guillemets (" "). La chaîne est définie dans le segment de données du programme, grâce à la directive `.data`. Ce qui est déclaré dans le segment de données est placé en mémoire RAM. De même, la directive `.text` indique que ce qui suit est place dans le segment d’instructions (et est typiquement place en mémoire ROM/Flash). Afin de pouvoir faire référence à la chaîne de caractères, elle est précédée d’un label (`str`). L’adresse mémoire de la chaîne de caractères peut ainsi être récupérée et copiée dans un registre à l’aide de la pseudo-instruction `la` (Load Address). Nommez votre programme `spim-print-str.s` et vérifiez son bon fonctionnement en le chargeant et l’exécutant à l’aide de SPIM.
### Résolution de l'exo 9
```mips
	.data 
	.globl str 
str:.asciiz "Hello World of MIPS\n" 

	.text 
main: 
	la $a0, str 
	li $v0, 4
	syscall
	jr $ra
```
Afin de vérifier votre compréhension de l’encodage d’une chaîne de caractères en mémoire, veuillez donner la valeur du mot de 32 bits stocké à l’adresse désignée par le label `str`.  Afin d’obtenir l’adresse à laquelle correspond le label `str`, vous pouvez exécuter votre programme jusqu’à passer la pseudo-instruction `la $a0, str`. L’adresse sera alors chargée dans le registre `a0`. Une autre possibilité consiste à définir `str` comme un symbole global (voir directive `.globl` en Section A.2) et lister les symboles avec le menu `Simulator / Display Symbols`. Allez ensuite voir dans la zone de mémoire de données via le panneau central du simulateur, onglet `Data`. Dans ce panneau, chaque ligne donne le contenu de 16 octets consécutifs en mémoire. L’adresse du premier de ces octets est en début de ligne.
\
Notez ci-dessous, en hexadécimal, l’adresse correspondant à `str` et le mot de 32 bits situé à cette adresse. Comment interprétez - vous la valeur de ce mot ?
### Résolution de l'exo 10
Le label `str` désigne l’adresse `0x10010000`. Le mot de 32 bits (4 octets) situé à cette adresse vaut `6c6c6548`. Il s’agit des codes ASCII des 4 premiers caractères de la chaîne

| Caractère | Code ASCII |
| --------- | ---------- |
| H         | `0x48`     |
| e         | `0x65`     |
| l         | `0x6c`     |

Ces caractères semblent apparaître en ordres opposés dans le mot de 32 bits et dans la chaîne. Ceci est dû au fait que sur les processeurs que nous utilisons, le simulateur SPIM utilise la convention **little-endian** pour représenter des mots de plusieurs octets. L’octet de plus petite adresse (`H` / `0x48`) est donc celui de plus faible poids dans le mot `6c6c6548`
