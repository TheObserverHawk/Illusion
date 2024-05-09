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

# Exo 9
Dans cet exercice, il vous est demandé d’utiliser l’appel système n°4 ( `print string`, Section A.5) afin d’afficher la chaîne de caractères de votre choix à la console. Cet appel système prend un seul argument qui est l’adresse du premier caractère de la chaîne à afficher. Cet argument est passe dans le registre `a0`.
\
La première étape pour résoudre cet exercice est de définir une chaîne de caractères en mémoire. La Figure 5 illustre la représentation  en mémoire de la chaîne de caractères ≪ `Hello World of MIPS` ≫. Chaque caractère est représenté par son code ASCII et occupe un octet  en mémoire. Par exemple, le caractère ’`H`’ est représenté par le code ASCII `0x48`. Les codes des caractères successifs de la chaîne sont places en mémoire à des adresses consécutives. Ainsi, dans l’exemple, le premier caractère est stocké à l’adresse `0x10010000`, le second à l’adresse `0x10010001`, etc... Ces adresses peuvent être différentes dans votre programme. Un label `str` permet de designer l’adresse du premier caractère de la chaîne, soit `0x10010000`. 
\
Il est important de remarquer que la longueur de la chaîne n’est pas stockée en mémoire. En revanche, la fin de la chaîne est indiquée par le code `0`. Ce code est visible a la Figure 5 : le dernier caractère de la chaîne, ’`S`’, est suivi par le code `0`. Cette représentation de chaînes de caractères est appelée chaîne à zéro terminal (nul/zero-terminated string).
**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240509135403.png]]
Definir une telle chaîne en mémoire peut être réalisée à l’aide de directives du langage d’assemblage (voir Section A.2), comme montré à la Figure 6. La directive `.asciiz` crée une chaîne à zéro terminal en mémoire, sur base d’un litéral chaîne de caractères entouré de guillemets (" "). La chaîne est définie dans le segment de données du programme, grâce à la directive ` .data. Ce qui est declar ´ e dans le segment de donn ´ ees est plac ´ e en m ´ emoire RAM. De m ´ eme, la directive ˆ .text indique que ce qui suit est place dans le ´ segment d’instructions (et est typiquement place en m ´ emoire ROM/Flash). Afin de pouvoir faire r ´ ef´ erence ´ a la cha ` ˆıne de caracteres, elle ` est prec´ ed´ ee d’un label ( ´ str). L’adresse memoire de la cha ´ ˆıne de caracteres peut ainsi ` etre r ˆ ecup ´ er´ ee et copi ´ ee dans un registre ´ a l’aide ` de la pseudo-instruction la (Load Address). Nommez votre programme spim-print-str.s et verifiez son bon fonctionnement en le chargeant et l’ex ´ ecutant ´ a l’aide de ` SPIM.