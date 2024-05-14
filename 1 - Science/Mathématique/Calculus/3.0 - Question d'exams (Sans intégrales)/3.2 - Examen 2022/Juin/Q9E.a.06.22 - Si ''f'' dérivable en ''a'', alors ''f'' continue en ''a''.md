---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Continuité d'une fonction_
1. [[1.4.1 - Déf = Continuité d'une fonction]]

_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]

# Question 9 point $a$ d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case appropriée selon que vous pensez qu’elle est vraie ou fausse. Justifiez votre réponse par un bref argument (rigoureux) ou un contre-exemple. La qualité de vos justifications est importante
### Soit $f:\mathbb{R}\to\mathbb{R}$ une application et $a\in\mathbb{R}$. Si $f$ est dérivable en $a$, alors $f$ est continue en $a$
_Réponse_ : Vrai
\
On sait que la dérivabilité est plus forte que continuité. 
Soit $f:\mathbb{R}\to\mathbb{R}$ une application et $a\in\mathbb{R}$ 
Supposons que $f$ dérivable en $a$ i.e. $$\underset{x\to a}{\operatorname{lim}}=\frac{f(x)-f(a)}{x-a}= \partial f(a)$$
On veut montrer que $$\underset{x\to a}{\operatorname{lim}}f(x)=f(a)$$
On a que $$\begin{aligned}f(x)-f(a)&=(x-a).\frac{f(x)-f(a)}{x-a}\\\iff \underset{x\to a}{\operatorname{lim}}(f(x)-f(a))&=\underset{x\to a}{\operatorname{lim}}\left((x-a).\frac{f(x)-f(a)}{x-a}\right)\\&=\underbrace{\underset{x\to a}{\operatorname{lim}}(x-a)}_{=0}.\underset{x\to a}{\operatorname{lim}}\frac{f(x)-f(a)}{x-a}\end{aligned}$$
	car $$\underset{x\to a}{\operatorname{lim}}(x-a)$$ existe et vaut 0 et car $$\underset{x\to a}{\operatorname{lim}}\frac{f(x)-f(a)}{x-a}$$ existe par hypothèse et vaut 0. On a donc $$\underset{x\to a}{\operatorname{lim}}f(x)-f(a)=0\iff \underset{x\to a}{\operatorname{lim}}f(x)-\underset{x\to a}{\operatorname{lim}}f(a)=0\iff\underset{x\to a}{\operatorname{lim}}f(x)=\underset{x\to a}{\operatorname{lim}}f(a)=f(a)$$
	