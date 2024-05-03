---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Math discrète : Relation binaire_
1. [[1.2.3 - Relation réflexive]]
2. [[1.2.5 - Relation transitive]]

_Math élémentaire : Logique_
1. [[../../../Math élémentaire/0 - Logique/0.1 - Logique propositionnelle/0.1.3 - Sémantique (Logique)|0.1.3 - Sémantique (Logique)]]
# Exo - Rb13
## Enoncé : Soit $A$ un ensemble contient 2 éléments. Déterminez si les affirmations suivantes sont vraies ou fausses
### a) Toute relation binaire sur $A$ est transitive
_Réponse_ : Faux
\
Soit $R=\{(a,b)\in A\times A\ |\ a\neq b \}$ 
Prenons $$A=\{0,1\}$$ On a $$R=\{(0,1),(1,0)\}$$ par transitivité (négation), on a $$\exists c\in A,\exists x\in A, \exists y\in A,\quad cRx\wedge xRy\wedge\neg(cRy)$$ prenons $$c=0, x=1, y=0$$ On a $$0R1\wedge1R0\wedge 0R0$$

 
### b) Toute relation binaire sur $A$ qui est réflexive, est transitive
_Réponse_ : Vrai
\
Soit $R$ une relation binaire sur $A$ 
Supposons $R$ est réflexive i.e. $$\forall a\in A, aRa$$ Montrons que $R$ est transitive i.e. $$\forall a,b,c\in A, aRb\wedge bRc\Rightarrow aRc$$ Soient $a,b,c\in A$ 
1. Cas 1 : $$a=b=c$$ Supposons $$aRa\wedge aRa$$ Donc $$aRa$$
2. Cas 2 : $$a=c\wedge a\neq b$$ Supposons que $$aRb\wedge bRa$$ Montrons que $$aRc$$ i.e. $$aRa$$ Vrai car $R$ est réflexive
3. Cas 3 : $$a\neq b\wedge b=c$$ Supposons que $$aRb\wedge bRc$$ i.e. $$bRb$$ Montrons que $$aRb$$ Vrai par hypothèse $aRb$
4. Cas 4 : $$a\neq b\wedge b\neq c$$ Supposons que $$aRb\wedge bRc$$ Montrons que $$aRc$$ vrai car par hypothèse $aRb\wedge bRc$ 
### c) Toute relation binaire sur $A$ est symétrique, est transitive
_Réponse_ : Faux
\
Prenons le même exemple que $a)$ i.e. $$R=\{(a,b)\in A\times A\ |\ a\neq b \}$$Montrons que $R$ est symétrique i.e. $$\forall a\in A,\forall b\in A,\quad aRb\Rightarrow bRa$$ Soient $a,b\in A$ 
Supposons que $$aRb$$ i.e. $$\{(a,b)\in A\times A\ |\ a\neq b\}$$ Par hypothèse, on sait que $a\neq b$ et donc par symétrique, on a $$b\neq a$$ Montrons que $R$ est transitive, qui est déjà fait par $a)$ 