---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]
2. [[1.5.8 - Prop Prop 5 = Dériv fonc de puissance]]

_Calculus : Théorème de la moyenne_
1. [[1.6.3.4 - Prop = Si ''f'' décroissante, alors dériv de ''f'' sur ''I'' est négatif]]

_Calculus : Dérivée d'ordre supérieure_
1. [[1.7.1 - Prop = Classe de fonctions]]
2. [[1.7.3 - Déf = (Classe de fonctions dérivables)]]

_Math élémentaire : Inégalité_
1. [[1.2.4 - Fonction strictement décroissante]]

_Math élémentaire : Logique_
1. [[0.2.5 - Preuve qu'une formule est fausse]]

# Question 8 point c d'examen du janvier 2022
## Enoncé : Supposons que $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$. Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse. Justifiez vos réponses par une preuve ou un contre-exemple.
### Question 8.$a$ : Si $f$ est strictement décroissante, alors $\forall x \in \mathbb{R},\ \partial f(x) < 0$ 
_Réponse_ : Faux
Donnons un contre-exemple, c’est-à-dire une fonction $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$ qui soit strictement décroissante mais qui ne vérifie pas $$∀x ∈ \mathbb{R}, ∂ f(x) < 0$$
\
Autrement dit, on veut une fonction strictement décroissante $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$ qui vérifie la négation de la thèse, à savoir $$∃x ∈ \mathbb{R}, ∂ f(x) ⩾0$$ 

Prenons $-x^3$ 
Cette fonction possède bien une dérivée continue sur $\mathbb{R}$ et est strictement décroissante.
Cette fonction vérifie aussi $$∃x ∈ \mathbb{R}, ∂ f(x) ⩾ 0$$ 
Il suffit en effet de prendre $x = 0$ et de constater que $$\left.\partial f(0) = -3x^2 \right|_{x=0} = 0 \ge0$$
