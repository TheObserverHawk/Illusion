---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Développement de Taylor_
1. [[1.8.1 - Formule = Développement de Taylor d'ordre ''n'' de ''f'']]
2. [[1.8.2 - Thm = (Formule polynomiale de Taylor)]]

# Question 7 point $c$ d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse. Justifiez vos réponses par une preuve ou un contre-exemple explicite.
### Le développement de Taylor d’ordre 2 de la fonction $f(x) = x^2 − 1$ en $x = 1$ est $x^2 −1$ car c’est un polynôme de degré $⩽ 2$. Contrainte : Quelle que soit la case que vous avez cochée, votre justification doit utiliser la définition du développement de Taylor (et pas les théorèmes prouvés à ce propos).
_Réponse_ : Vrai (Non vérifié $\Rightarrow$ A voir avec les assistants ou professeurs)

- - -
On sait que par définition le développement de Taylor : 
Soit $f : \mathbb{R} \to \mathbb{R},\ a \in \mathbb{R}$ et $n \in \mathbb{N}$ 
On dit que $p$ est un développement de Taylor d'ordre $n$ de $f$ en $a$ si
1. $p \in \mathbb{P}^{\le n}$ i.e. $p$ est un polynôme de degré au plus $n$ et
2. $f(x)=p(x)+o\big((x-a)^n\big)$ lorsque $x \to a,\ x \in \operatorname{Dom}f$ 

où $$p:=\sum^{n}_{i=0} \partial_i f(a).\frac{(x-a)^i}{i!}$$
- - -
On veut prouver que le développement de Taylor d’ordre 2 de la fonction $$f(x) = x^2 − 1$$ en $x = 1$ est $$x^2 −1$$
Soit $$f:\mathbb{R}\to\mathbb{R} : x\mapsto x^2-1, \operatorname{Dom}f \cap\operatorname{adh(Dom}\mathbb{R}\text{ \\ } \{1\})=\mathbb{R}, 1\in\mathbb{R}, 2\in\mathbb{N}$$
On aurait que développement de Taylor de $f(x)=x^2-1$ en 1 d'ordre 2 est $$\begin{aligned}\frac{f(1)}{0!}.(x-1)^0+\frac{\partial f(1)}{1!}.(x-1)^1+\frac{\partial^2 f(1)}{2!}.(x-1)^2&=\\\frac{1^2-1}{0!}.(x-1)^0+\frac{2.1}{1!}.(x-1)^1+\frac{2}{2!}.(x-1)^2&=\\0+2.(x-1)+1.(x-1)^2=(2x-2)+(x^2-2x+1)&=x^2-1\end{aligned}$$Donc le développement de Taylor de $f$ d'ordre 2 en $1$ est $$x^2-1$$Par conséquent, c'est vrai.