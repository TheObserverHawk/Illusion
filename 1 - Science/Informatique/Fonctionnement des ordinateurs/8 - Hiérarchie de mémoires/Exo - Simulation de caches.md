---
tags:
  - Note_done
  - Informatique
source: UMons - Fonctionnement des ordinateurs
---

Link :
_Fonctionnement des ordinateurs : Représentation des nombres naturels & entiers_
1. [[../2 - Représentation des nombres naturels & entiers/2.3.2.1 - Bit|2.3.2.1 - Bit]]
2. [[../2 - Représentation des nombres naturels & entiers/2.3.2.2 - Octet|2.3.2.2 - Octet]]
3. [[../2 - Représentation des nombres naturels & entiers/2.3.3 - Représentation hexadécimale|2.3.3 - Représentation hexadécimale]]

_Fonctionnement des ordinateurs : Processeur_
1. [[../5 - Processeur/5.4.6.6.5 - Adressage indirect indexé (MIPS)|5.4.6.6.5 - Adressage indirect indexé (MIPS)]]

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
## Déterminez le hit ratio pour chaque cache 
Par défaut la cache $A$ et la cache $B$ sont vides.
### Cache $A$ : 4-way set-associative
**Illustration du Modèle de la cache** : ![[IMG_5322.jpeg]]
On sait que la cache $A$ : cache 4-way set-associative 128 octets, 16 lignes de 8 octets :
1. $$128\text{ B}= 2^7\text{ B}\quad \text{ Taille de la cache sans tag + bit de validité }$$
2. $$\text{ sets = }\frac{16\text{ lignes }}{4}=4\quad\Rightarrow\quad \log_2\left(4\right)=\log_2\left(2^2\right)=2\text{ bits de set}$$
3. $$\text{Taille 1 ligne = 8 octets }\quad\Rightarrow\quad \log_2(8)=\log_2\left(2^3\right)=3\text{ bits d’offset}$$
4. $$\text{16 - 2 - 3 = 11 bits de tag}$$

**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240429114959.png]]
Nous avons :
- `0xA3C9` i.e. `1010 0011 1100 1001` :
	- Offset : `001`
	- Set : `01`
	- Tag : `1010 0011 110` i.e. `101 0001 1110` i.e. `0x51E`

C’est un miss, vu que par défaut, la cache est vide. De plus, la cache $A$ a 4 cellules (`BL=4`) en lecture rafale. (car mémoire en 16 bits = 2 octets puisque une adresse est composée de 16 bits = 2 octets et une ligne de cache contient 8 octets)

Hit ratio = 7/14 = 50%
### Cache $B$ : Direct-mapped
**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240429115200.png]]
Hit ratio = 5/14 = 35,7%