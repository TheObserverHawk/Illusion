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
1. [[4.4 - Porte logique]]
2. [[4.4.0 - Table de vérité (Fonc ordi)]]
3. [[4.5 - Logique combinatoire]]
4. [[4.5.1 - Circuit logique]]
5. [[4.5.2 - Combinaisons de portes]]

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

# Question 2 partie 2 d'exam de juin 2019
## Question : 
Cette question vise à implémenter un circuit logique permettant de comparer entre eux deux nombres entiers $a$ et $b$. Le comparateur dispose à cet effet de $2N$ entrées booléennes correspondant aux deux nombres représentés chacun sur $N$ bits en complément à deux. Ces entrées sont nommées $$a_{N−1} . . . a_0$$ pour les bits du nombre $a$ et $$b_{N−1} . . . b_0$$ pour les bits du nombre $b$. Le comparateur dispose également de deux sorties booléennes définies comme suit : 
1. **eq** indique si les deux nombres sont égaux, i.e. $$eq ⇔ (a = b)$$ 
2. **less** indique si $a$ est strictement inférieur à $b$, i.e. $$less ⇔ (a < b)$$ 

Afin de limiter le nombre d’entrées et la complexité du circuit logique du comparateur, la question considère des nombres représentés sur $N = 2$ bits. Il dispose donc de $4$ entrées $a_1, a_0, b_1$ et $b_0$.
### $a$) Etablir la table de vérité de `less` et `eq` en fonction des entrées $a_1, a_0, b_1$ et $b_0$. La même table est utilisée pour les 2 sorties (`less` et `eq`). Dans la colonne intitulée « valeur », indiquez la valeur des nombres représentés en binaire.

| Valeur | $a_1$ | $a_0$ | Valeur | $b_1$ | $b_0$ | less $(a<b)$ | eq $(a=b)$ |
| ------ | ----- | ----- | ------ | ----- | ----- | ------------ | ---------- |
|        |       |       |        |       |       |              |            |

### $b$) Dérivez une expression logique pour `less` et `eq`. Il vous est conseillé d’utiliser pour cela les sommes ou produits canoniques. A vous de choisir entre somme et produit, de façon à minimiser le nombre de termes de l’expression.

### $c$) Fournissez le schéma du circuit logique correspondant au test d’égalité. Ce circuit logique possèdera 4 entrées $a_1, a_0, b_1$ et $b_0$ ainsi qu’une sortie unique $eq$. Veillez à utiliser les symboles standards pour exprimer les portes logiques AND, OR et NOT. Veillez également à la propreté et la clarté de votre schéma.
