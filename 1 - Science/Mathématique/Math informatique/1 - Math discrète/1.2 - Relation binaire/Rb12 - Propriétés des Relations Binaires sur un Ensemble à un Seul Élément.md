---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Math discrète : Relation binaire_
1. [[1.2.3 - Relation réflexive]]
2. [[1.2.4 - Relation symétrique]]
3. [[1.2.5 - Relation transitive]]

_Math élémentaire : Logique_
1. [[0.1.2 - Formule de la logique propositionnelle]]
2. [[0.1.3 - Sémantique (Logique)]]
# Rb12 
## énoncé : Soit $A$ un ensemble contenant un seul élément i.e. $A=\{a\}$. Déterminez si les propositions suivantes sont vraies ou fausses 
### a) Toute relation binaire $R\subseteq A\times A$ est transitive 
_Réponse_ : Vraie
\
$R\subseteq A\times A$ est transitive i.e. $$\forall a,b,c\in A, aRb\wedge bRc \Rightarrow aRc$$ Soient $a,b,c\in A$ i.e. $a=b=c=x$ 
Supposons que $$xRx\wedge xRx$$ Montrons que $$xRx$$ Ok

### b) Toute relation binaire $R\subseteq A\times A$ est réflexive 
_Réponse_ : Fausse
\
Si $R=\{(a,b)|\ a<b\}$, on a $$R=\varnothing$$ prenons $A=\{1\}$, on a $\neg(1R1)$ car $1<1$ impossible

### c) Toute relation binaire $R\subseteq A\times A$ est symétrique 
_Réponse_ : Vraie
\
Deux situations possibles :
1. $$R=\{(x,x)\}$$ qui est symétrique et transitive
2. $$R=\varnothing$$ qui est aussi symétrique et transitive car la prémisse de l’implication est fausse i.e. $aRb$ et donc l’implication est vraie. 