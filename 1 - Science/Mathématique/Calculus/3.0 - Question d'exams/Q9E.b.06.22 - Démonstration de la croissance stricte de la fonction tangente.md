---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Continuité d'une fonction_
1. [[1.4.1 - Déf = Continuité d'une fonction]]
2. [[1.4.3 - Déf = Application continue]]

_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.11 - Prop Prop 8 = Dériv des fonct trigonométriques]]

_Math élémentaire : Inégalité_ 
1. [[1.2.2 - Fonction strictement croissant]]
# Question  d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case appropriée selon que vous pensez qu’elle est vraie ou fausse. Justifiez votre réponse par un bref argument (rigoureux) ou un contre-exemple. La qualité de vos justifications est importante
### La fonction $f :\mathbb{R}\to\mathbb{R}:x\mapsto \tan(x)$ est strictement croissante car sa dérivée $\partial f(x)=\frac{1}{1+x^2}$ est strictement positive pour tout $x\in\operatorname{dom}f$
_Réponse_ : Faux
\
La fonction $\tan(x)$ n'est pas définie sur un intervalle de $\mathbb{R}$ car ça doit être une application continue,...
**Illustration** : ![[Pasted image 20240321205409.png]]
\
Donc, on va prouver que sa négation est vraie i.e. montrons que $$\exists x_1, x_2\in\operatorname{Dom}f\text{ tel que }x_1<x_2\wedge f(x_1)\ge f(x_2)$$ On choisit $x_1=\frac{-3\pi}{4}$ et $x_2=\frac{3\pi}{4}$
On a que $$\begin{aligned}x_1 < x_2 &\wedge f(x_1)\ge f(x_2)\\\iff \frac{-3\pi}{4}<\frac{3\pi}{4}&\wedge \tan\left(\frac{-3\pi}{4}\right)\ge\tan\left(\frac{3\pi}{4}\right)\\\iff \frac{-3\pi}{4}<\frac{3\pi}{4}&\wedge 1\ge -1\end{aligned}$$
Ce qui est vrai, donc $\tan(x)$ n'est pas strictement positif.
