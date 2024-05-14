---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Continuité d'une fonction_
1. [[1.4.1 - Déf = Continuité d'une fonction]]



# Question 7 point $a$ d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse. Justifiez vos réponses par une preuve ou un contre-exemple explicite
### Soit $f : \mathbb{R} \to\mathbb{R}$ et $a\in\operatorname{Dom}f$. Si $\underset{\overset{x\to a}{x\neq a}}{\operatorname{lim}}f(x)$ existe, alors $f$ est continue en $a$
_Réponse_ : Faux
\
Montrons que sa négation est vraie i.e. $\underset{\overset{x\to a}{x\neq a}}{\operatorname{lim}}f(x)$ et $f$ n'est pas continue en $a$. Prenons $$f=\begin{cases}1 \quad\text{ si }x=0\\2\quad\text{ si }x\neq 0\end{cases}$$ et $$a=0\in\underbrace{\operatorname{Dom}f}_{=\mathbb{R}}$$ car $0\in\mathbb{R}$ 
On a que $$\underset{\overset{x\to 0}{x\neq 0}}{\operatorname{lim}}f(x)=\underset{\overset{x\to 0}{x\neq 0}}{\operatorname{lim}}f(0)=\underset{\overset{x\to 0}{x\neq 0}}{\operatorname{lim}}2=2\neq f(0) \text{ car } f(0)=1$$
Regardons $\underset{\overset{x\to 0}{x\neq 0}}{\operatorname{lim}}f(x)$ et $\underset{\overset{x\to 0}{x = 0}}{\operatorname{lim}}f(x)$ : $$\underset{\overset{x\to 0}{x= 0}}{\operatorname{lim}}f(x)=\underset{\overset{x\to 0}{x= 0}}{\operatorname{lim}}f(0)=\underset{\overset{x\to 0}{x= 0}}{\operatorname{lim}}1=1=f(0)$$on a déjà calculer que $$\underset{\overset{x\to 0}{x\neq 0}}{\operatorname{lim}}f(x)=2$$ i.e. $$\underset{\overset{x\to 0}{x < 0}}{\operatorname{lim}}f(x)=2\quad\text{ et }\quad \underset{\overset{x\to 0}{x> 0}}{\operatorname{lim}}f(x)=2$$
comme les 2 limites sont différentes, on a que $\underset{x\to 0}{\operatorname{lim}}f(x)$ n'existe pas et donc $f(x)$ n'est pas continue en 0