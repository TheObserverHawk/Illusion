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

Nous avons :
- `0xA3C9` i.e. `1010 0011 1100 1001` :
	- Offset : `001`
	- Set : `01`
	- Tag : `1010 0011 110` i.e. `101 0001 1110` i.e. `0x51E`

C’est un **miss** (Compulsory miss), vu que par défaut, la cache est vide. De plus, la cache $A$ a 4 cellules (`BL=4`) en lecture rafale. (car mémoire en 16 bits = 2 octets puisque une adresse est composée de 16 bits = 2 octets et une ligne de cache contient 8 octets). 
\
Pour accéder la première cellule, on a une valeur d'offset égale à `000`, la 2ème cellule a une valeur d'offset égale à `010`, la 3ème cellule a une valeur d'offset égale à `100` et la 4ème cellule a une valeur d'offset égale à `110`. 
\
Donc, la 1ère cellule stocke `0xA3C8` car l'offset vaut `000`, la 2ème cellule stocke `0xA3CA` car l'offset vaut `010`, la 3éme cellule stocke `0xA3CC` car l'offset vaut `100`, la 4ème cellule stocke `0xA3CE` car l'offset vaut `110`. 
\
Comme `0xA3C9` a une offset de `001`, l'adresse se trouve alors dans la 1ère cellule de la ligne 0, de plus la cache charge les adresses suivants `0xA3CB`, `0xA3CD` et `0xA3CF` dans la ligne 0

- `0xA3CB` i.e. `1010 0011 1100 1011` :
	- Offset : `011`
	- Set : `01`
	- Tag : `101 0001 1110` i.e. `0x51E`

C'est **hit**, car mémoire cache à multiple cellules dans une entrée (2ème cellule de la ligne 0) 


- `0xB5EA` i.e. `1011 0101 1110 1010` : 
	- Offset : `010`
	- Set : `01`
	- Tag : `1011 0101 111` i.e. `101 1010 1111` i.e. `0x5AF`

C'est un **miss** (Compulsory miss), donc l'adresse `0xB5EA` se charge dans le set 1 à la ligne 1 de la cache car ligne 0 déjà occupé. La cache va charger dans les 4 cellules de la ligne 1 du set 1 les adresses suivants : `0xB5E8` (offset = `000`), `0xB5EA` (offset = `010`), `0xB5EC` (offset = `100`) et `0xB5EE` (offset = `110`) 

- `0xB5E1` i.e. `1011 0101 1110 0001` 
	- Offset : `001`
	- Set : `00`
	- Tag : `1011 0101 111` i.e. `101 1010 1111` i.e. `0x5AF`

C'est un **miss** (Compulsory miss), donc l'adresse `0xB5E1` se charge à la ligne 0 du set 0 de la cache. De plus, la cache va charger dans les 4 cellules de la ligne 0 les adresses suivants : `0xB5E0` (offset = `000`) mais c'est `0xB5E1` (offset = `001`), `0xB5E2` (offset = `010`), `0xB5E4` (offset = `100`) et `0xB5E6` (offset = `110`) 

- `0xB7E5` i.e. `1011 0111 1110 0101` :
	- Offset : `101`
	- Set : `00`
	- Tag : `1011 0111 111` i.e. `101 1011 1111` i.e. `0x5BF` 

C'est un **miss** (Compulsory miss), donc l'adresse `0xB7E5` se charge à la ligne 1 du set 0 de la cache. De plus, la cache va charger dans les 4 cellules de la ligne 1 les adresses suivants : `0xB7E0` (offset = `000`), `0xB7E2` (offset = `010`), `0xB7E4` (offset = `100`) mais c'est `0xB7E5` (offset = `101`) et `0xB7E5` (offset = `110`)

- `0xB9C9` i.e. `1011 1001 1100 1001` :
	- Offset : `001`
	- Set : `01`
	- Tag : `1011 1001 110` i.e. `101 1100 1110` i.e. `0x5CE`

C'est un **miss** (Compulsory miss), donc l'adresse `0xB9C9` se charge à la ligne 2 du set 1 de la cache. De plus, la cache va charger dans les 4 cellules de la ligne 2 les adresses suivants : `0xB9C8` (offset = `000`) mais c'est `0xB9C9` (offset = `001`), `0xB9CA` (offset = `010`), `0xB9CC` (offset = `100`) et `0xB9CE` (offset = `110`)

- `0xA3C9` i.e. `1010 0011 1100 1001` :
	- Offset : `001`
	- Set : `01`
	- Tag : `1010 0011 110` i.e. `101 0001 1110` i.e. `0x51E`

C'est un **hit**, puisque se trouve dans la ligne 0 du set 1 de la cache

- `0xB5E1` i.e. `1011 0101 1110 0001` 
	- Offset : `001`
	- Set : `00`
	- Tag : `1011 0101 111` i.e. `101 1010 1111` i.e. `0x5AF`

C'est un **hit**, puisque se trouve dans la ligne 0 du set 0 de la cache

- `0xB5EA` i.e. `1011 0101 1110 1010` : 
	- Offset : `010`
	- Set : `01`
	- Tag : `1011 0101 111` i.e. `101 1010 1111` i.e. `0x5AF`

C'est un **hit**, puisque se trouve dans la ligne 1 du set 1 de la cache

- `0x12AA` i.e. `0001 0010 1010 1010` :
	- Offset : `010`
	- Set : `01`
	- Tag : `0001 0010 101` i.e. `000 1001 0101` i.e. `0x095`

C'est un **miss** (Compulsory miss), donc l'adresse `0x12AA` se charge à la ligne 3 du set 1 de la cache. De plus, la cache va charger dans les 4 cellules de la ligne 3 les adresses suivants : `0x12A8` (offset = `000`) , `0x12AA` (offset = `010`), `0x12AC` (offset = `100`) et `0x12AE` (offset = `110`)

- `0x122A` i.e. `0001 0010 0010 1010` :
	- Offset : `010`
	- Set : `01`
	- Tag : `0001 0010 001` i.e. `000 1001 0001` i.e. `0x091`

C'est un miss (Conflict miss), donc l'adresse `0x12AA` se charge à la ligne 2 du set 1 de la cache car stratégie de remplacement est LRU (Least Recently Used) et l'adresse `0xB9C9` sera éjecté de la cache.  De plus, la cache va charger dans les 4 cellules de la ligne 3 les adresses suivants : `0x1228` (offset = `000`) , `0x122A` (offset = `010`), `0x122C` (offset = `100`) et `0x122E` (offset = `110`)

**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240429114959.png]]

C'est un $$\text{Hit ratio}= \frac{N_{\text{hit}}}{N_{\text{hit}}+N_{\text{Miss}}}=7/14 = 50\text{\%}$$
### Cache $B$ : Direct-mapped
**Illustration du Modèle de la cache** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240509160408.png]]
**Illustration** : ![[../../../../0 - Dossier Template/Dossier IMage/Pasted image 20240429115200.png]]
C'est un $$\text{Hit ratio}= \frac{N_{\text{hit}}}{N_{\text{hit}}+N_{\text{Miss}}}=5/14 = 35,7\text{\%}$$