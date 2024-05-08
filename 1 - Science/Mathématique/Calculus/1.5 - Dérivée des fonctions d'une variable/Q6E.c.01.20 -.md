---
## Metadata
tags : 
 - Note_done Note_WIP Math
 - 
source : UMons - Calculus Examen
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.13 - Déf = Petit-o]] 

# Question  d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case appropriée selon que vous pensez qu’elle est vraie ou fausse. Justifiez votre réponse par un bref argument (rigoureux) ou un contre-exemple.
### $\frac{o(x)}{1+o(x)}=o(x)$ lorsque $x\to 0$ 
_Réponse_ : Vrai
\
Posons $$g(x)=\frac{o(x)}{1+o(x)}$$ Regardons si $$\begin{cases}\quad \frac{g(x)}{x-0}\to0\quad\text{ }\quad{\color{red}\text{I.}}\\g(0)=0\quad\text{ si }0\in\operatorname{Dom}g\quad{\color{red}\text{II.}}\end{cases}$$ Chaque $o(x)$ désigne une fonction quelconque qu'on ne connaît pas. Nous avons donc que $$g(x)=\frac{f_1(x)}{1+f_2(x)}$$ où $$f_1(x)=o(x)\quad\wedge\quad f_2(x)=o(x)$$ du coup on sait que $$\begin{cases}\frac{f_1(x)}{x-0}\to 0\quad\cap\quad\frac{f_2(x)}{x-0}\to0\\f_1(0)=0\quad\cap\quad f_2(0)=0\end{cases}$$
1. $${\color{red}\text{I.}}\quad \frac{g(x)}{x-0}=\frac{f_1(x)}{x.(1+f_2(x))}=\frac{f_1(x)}{x}.\frac{1}{1+f_2(x)}$$ et on a que $$1+f_2(x)\to 1$$ car $f_2(0)=0$ et $0\to0$, et $$\frac{f_1(x)}{x}\to0$$ car $f_1(x)=o(x)$. Donc $$\frac{g(x)}{x}\to 0.1=0$$ par règle de calculs sur les limites
2. $${\color{red}\text{II.}}\quad g(0)=\frac{f_1(0)}{1+f_2(0)}=\frac{0}{1+0}$$