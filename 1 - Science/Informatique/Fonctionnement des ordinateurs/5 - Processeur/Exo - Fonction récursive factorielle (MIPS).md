---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Processeur_
1. [[5.4 - Architecture MIPS]]
2. [[5.4.2 - Registre d'usage général (GPR)]]
4. [[5.4.4 - Etiquette (MIPS)]]
5. [[5.4.5 - Pseudo-instruction (MIPS)]]
6. [[5.4.6 - Jeu d'instructions (MIPS)]]
7. [[5.4.6.3.3 - Instruction Add Word Immediate (ADDI) (MIPS)]]
8. [[5.4.6.3.4 - Instruction Add Word Immediate Unsigned (ADDIU) (MIPS)]]
9. [[5.4.6.3.5 - Instructions de type-R (MIPS)]]
10. [[5.4.6.6.6 - Instructions Load & Store (MIPS)]]
11. [[5.4.6.8 - Instruction de contrôle de flux (MIPS)]]
12. [[5.4.6.8.1 - Instruction de Type-J (MIPS)]]
13. [[5.4.6.12.2.1 - Instruction Jump And Link (JAL) (MIPS)]]
14. [[5.4.6.12.3 - Pile d'appel (MIPS)]]

_Math élémentaire : Logique_
1. [[0.6.1 - Factorielle]]
# Exercice – Fonction récursive : factorielle
On s’intéresse au calcul récursif de la factorielle $$n!~=~\begin{cases}n\left(n-1\right.)!&\text{si}\quad n>1\\1&\text{si}\quad n=0\quad\text{ou}\quad n=1&\end{cases}$$ Une implémentation récursive en langage C est donnée ci-dessous
```C
// pré-condition: n >= 0 
unsigned int fact(unsigned int n) { 
		if (n > 1) 
				return n * fact(n-1); 
		return 1; 
}
```

Supposons que l'argument `n` soit passé dans le registre `a0` et le résultat retourné dans `v0`. Observons le comportement de la fonction pour un l’appel `fact(4)`.
**Illustration** : ![[Pasted image 20240326202913.png]]
Deux approches sont possibles pour éviter de « perdre » la valeur de l’argument `n` (registre `a0`) lors des appels récursifs. 
1. Sauvegarde sur la pile :
	1. Sauvegarder `a0` sur la pile et le restaurer 
	2. Avantage : fonctionne dans tous les cas 
	3. Désavantage : accès mémoires supplémentaires 
2. Inverser la modification : 
	1. Effectuer la modification inverse de `a0`, i.e. calculer `a0=a0+1`  
	2. Avantage : pas d’accès mémoire supplémentaire 
	3. Désavantage : pas toujours applicable / pratique

## Sauvegarde sur la pile
Dans cette implémentation de la factorielle, la valeur de `n` (contenue dans `a0`) est sauvegardée sur la pile avant chaque appel récursif.
**Illustration** : ![[Pasted image 20240326203208.png]]
