---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Math discrète : Relation binaire_
1. [[1.2.2 - Relation binaire sur un ensemble]]
2. [[1.2.7 - Relation inverse]]
3. [[1.2.8 - Composition de relations]]

# Exo - Rb18
## Enoncé : Soit $A$ un ensemble et $R\subseteq A\times A$ une relation binaire sur $A$. Est-il toujours vrai que $R\circ R^{-1} = R^{-1}\circ R$ en sachant que $R^{-1}=\{(b,a)\in A\times A\ |\ (a,b)\in R \}$ ?
_Réponse_ : Faux
\
On a $$\begin{aligned}R\circ R^{-1}&=\{(a,c)\in A^2\ |\ \exists b \in A, (a,b)\in R^{-1}\wedge(b,c)\in R\}\\&=\{(a,c)\in A^2\ |\ \exists b\in A, ({\color{red}b},a)\in R\wedge ({\color{red}b},c)\in R\}\\R^{-1}\circ R&=\{(a,c)\in A^2\ |\ \exists b\in A, (a,b)\in R\wedge (b,c)\in R^{-1}\}\\&=\{(a,c)\in A^2\ |\ \exists b\in A, (a,{\color{red}b})\in R\wedge(c,{\color{red}b})\in R\}\end{aligned}$$ On a que $$R^{-1}\circ R\neq R\circ R^{-1}$$ en sachant que $$A\neq B\quad\iff\quad A\nsubseteq B\vee B\nsubseteq A$$ par exemple, prenons $$\begin{aligned}R&=\{(1,0),(2,0)\}\\R^{-1}&=\{(0,1),(0,2)\}\end{aligned}$$ on a que $$\begin{aligned}R\circ R^{-1}&=\{(0,0)\}\\R^{-1}\circ R&=\{(1,1),(2,2)\}\end{aligned}$$ par conséquent, $$R^{-1}\circ R\neq R\circ R^{-1}$$