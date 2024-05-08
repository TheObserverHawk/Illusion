---
## Metadata
tags : 
 - Note_done Note_WIP Math
 - 
source : UMons - Calculus Examen
---

Link :
_Calculus : Convergence d’une suite de réel_
1.

_Calculus : Caractéristique d'une suite_
1.

_Calculus : Limite de fonctions_
1. [[1.3.2 - Déf = Voisinage (Calculus)]]
1. [[1.3.3 - Déf = Adhérence]]

_Calculus : Continuité d'une fonction_
1.

_Math élémentaire : Logique_
1. [[../../Math élémentaire/0 - Logique/0.2 - Logique du 1er ordre et technique de preuve/0.2.8 - Preuve par l'absurde|0.2.8 - Preuve par l'absurde]]
# Question 9 d'examen du janvier 2020
## Enoncé : Soit $f : \mathbb{R} → \mathbb{R}$ une fonction et $a ∈ \operatorname{Dom} f$ . Prouvez l’équivalence suivante : $a\notin\operatorname{adh(Dom}f\text{ \\ }\{a\})\quad\iff\quad\exists r>0, [a-r,a+r]\cap\operatorname{Dom}f=\{a\}$
(Pas sûr, à voir)
\
On sait que par définition d'adhérence, on a $$\operatorname{(Dom}f\text{ \\ }\{a\})\subseteq\mathbb{R},\quad \operatorname{adh(Dom}f\text{ \\ }\{a\})= \{\ a \in \mathbb{R}\ |\ \exists\ (X_n) \subseteq \operatorname{(Dom}f\text{ \\ }\{a\}),\ X_n  \longrightarrow a\ \} $$ comme $a\notin\operatorname{adh(Dom}f\text{ \\ }\{a\})$, cela signifie que $$\operatorname{(Dom}f\text{ \\ }\{a\})\subseteq\mathbb{R},\quad \operatorname{adh(Dom}f\text{ \\ }\{a\})= \{\ a \in \mathbb{R}\ |\ \forall\ (X_n) \subseteq \operatorname{(Dom}f\text{ \\ }\{a\}),\ X_n  \nrightarrow a\ \}$$
### $a\notin\operatorname{adh(Dom}f\text{ \\ }\{a\})\quad\Rightarrow\quad\exists r>0, [a-r,a+r]\cap\operatorname{Dom}f=\{a\}$
Supposons que $$a\notin\operatorname{adh(Dom}f\text{ \\ }\{a\})$$ i.e. $$\operatorname{(Dom}f\text{ \\ }\{a\})\subseteq\mathbb{R},\quad \operatorname{adh(Dom}f\text{ \\ }\{a\})= \{\ a \in \mathbb{R}\ |\ \forall\ (X_n) \subseteq \operatorname{(Dom}f\text{ \\ }\{a\}),\ X_n  \nrightarrow a\ \}$$ Montrons que $$\exists r>0, [a-r,a+r]\cap\operatorname{Dom}f=\{a\}$$ 