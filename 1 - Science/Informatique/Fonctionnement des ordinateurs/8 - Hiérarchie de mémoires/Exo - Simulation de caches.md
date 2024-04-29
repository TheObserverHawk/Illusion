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
1. [[8.5 - Mémoire cache]]
2. [[8.5.1 - Cache miss (Mémoire cache)]]
3. [[8.5.2 - Cache hit (Mémoire cache)]]
4. [[8.8 - RAM vs Cache (Fonctionnement)]]
5. [[8.8.1 - Multiples cellules dans une entrée de cache]]
6. [[8.9 - Stratégie d'organisation d'une mémoire cache]]
7. [[8.9.2 - Cache direct-mapped]]
8. [[8.9.3 - Cache set-associative]]
9. [[8.9.4 - Stratégie de remplacement (Mémoire cache)]]

# Exo - Simulation de caches
Considérez les caches suivantes :
1. $A$ : cache 4-way set-associative 128 octets, 16 lignes de 8 octets 
2. $B$ : cache direct-mapped 128 octets, 16 lignes de 8 octets 
3. la stratégie de remplacement est LRU (Least Recently Used)

Le processeur effectue des lectures aux adresses suivantes et dans cet ordre : `0xA3C9`, `0xA3CB`, `0xB5EA`, `0xB5E1`, `0xB7E5`, `0xB9C9`, `0xA3C9`, `0xB5E1`, `0xB5EA`, `0xB5E1`, `0x12AA`, `0x122A`, `0xA3C8`, `0xA3CE`
Déterminez le hit ratio pour chaque cache 
