---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]
2. [[1.3.1.1 - Déf = Limite à gauche & Limite à droite]]

# Question 6 point $a$ d'examen du janvier 2024
## Enoncé : Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu'elle est vraie ou fausse. Justifiez votre réponse rigoureusement. Une affirmation telle que "vu au cours" n'est pas une justification
### Si $a\in\operatorname{Dom}f$, alors on a unicité de la limite et $b=f(a)$ 
_Réponse_ : Faux
\
On peut reformuler l'affirmation en $$\forall a\in\operatorname{Dom}f,\underset{x\to a}{\operatorname{lim}}f(x)=f(a)$$
Ce qui est faux, considérons $$f:\mathbb{R}\to\mathbb{R}:x\mapsto\begin{cases}1\quad\text{ si }x\ge 0\\-1\quad\text{ si } x < 0\end{cases}$$
Prenons $a=0$, montrons que $\underset{x\to a}{\operatorname{lim}}f(x)$ n'existe pas
On a $$\underset{\overset{x\to a}{\ge 0}}{\operatorname{lim}}f(x)=\underset{\overset{x\to a}{\ge 0}}{\operatorname{lim}}1=1\quad\wedge\quad \underset{\overset{x\to a}{\le 0}}{\operatorname{lim}}f(x)=\underset{\overset{x\to a}{\le 0}}{\operatorname{lim}}-1=-1$$
Comme $1\neq-1$, on en déduit que $\underset{x\to a}{\operatorname{lim}}f(x)$ n'existe pas