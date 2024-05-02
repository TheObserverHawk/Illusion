---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Math discrète : Relation binaire_
1. [[../1.2 - Relation binaire/1.2.3 - Relation réflexive|1.2.3 - Relation réflexive]]
2. [[../1.2 - Relation binaire/1.2.4 - Relation symétrique|1.2.4 - Relation symétrique]]
3. [[../1.2 - Relation binaire/1.2.5 - Relation transitive|1.2.5 - Relation transitive]]

_Math discrète : Relation d"équivalence_
1. [[1.3.1 - Relation d'équivalence]]
2. [[1.3.7 - Ensemble des parties]]

# Exo - Re 12
## Enoncé : La relation $R=\{(X,Y)\ |\ X,Y\subseteq \mathbb{N} \quad\wedge\quad X\cap Y \neq\varnothing \}$ est une relation équivalente sur $P(\mathbb{N} \text{ \\ } \{\varnothing\})$ ?

---
#### Exemple (test)
1. $$(\{1\},\{1\})\in R$$ car $\{1\}\subseteq\mathbb{N}$ et $\{1\}\cap\{1\}=\{1\}\neq\varnothing$ 
2. $$(\{1,2\},\{2,4\})\in R$$ car $\{1,2\}\wedge\{2,4\}\subseteq\mathbb{N}$ et $\{1,2\}\cap\{2,4\}=\{3\}\neq\varnothing$ 
3. $$(\{2,4\},\{1,2\})\in R$$

---
On a que 
1. Réflexive : $$A\cap A=A\neq\varnothing$$
2. Symétrique : $$A\cap B = B\cap A$$
3. Transitive : $$ARB\wedge BRC\quad\Rightarrow\quad ARC$$ ce qui n'est pas le cas. Prenons $$\begin{aligned}A&=\{1,2\}\subseteq\mathbb{N}\\B&=\{2,3\}\subseteq\mathbb{N}\\C&=\{3,4\}\subseteq\mathbb{N}\end{aligned}$$ On a $$ARB$$ car $\{1,2\}\cap\{2,3\}=\{2\}\neq\varnothing$ $$BRC$$ car $\{2,3\}\cap\{3,4\}=\{3\}\neq\varnothing$ $$\neg(ARC)$$ car $\{1,2\}\cap\{3,4\}=\varnothing$ 

Par conséquent, $R$ n'est pas une relation d'équivalence