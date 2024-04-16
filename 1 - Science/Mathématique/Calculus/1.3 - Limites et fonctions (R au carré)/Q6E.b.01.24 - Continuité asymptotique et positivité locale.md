---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Convergence d’une suite de réel_
1. [[1.1.2 - Prop = Limites des inégalités larges d'une suite]]
2. [[1.1.3 - Thm = Théorème de Sandwich]]

_Calculus : Limite de fonctions_
1. [[1.3.5 - Thm = Cgce dominée d'une limite de fonc]]

_Math élémentaire : Logique_
1. [[0.2.8 - Preuve par l'absurde]]

# Question  d'examen du juin 2022
## Enoncé : Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu'elle est vraie ou fausse. Justifiez votre réponse rigoureusement. Une affirmation telle que "vu au cours" n'est pas une justification
### Si $0\in\operatorname{Dom}f, f(0)=0$ et $\frac{f(x)}{x}\to 1$ quand $x\to 0$, alors $\exists r>0,\forall x\in\ ]0,r[, f(x)>0$ 
_Réponse_ : Vrai
\
Montrons que par l'absurde i.e. supposons que $$0\in\operatorname{Dom}f, f(0)=0\text{ et }\frac{f(x)}{x}\to 1$$ et supposons que $$\forall r>0,\exists x\in\ ]0,r[, f(x)\le0\quad\color{red}\text{ (*)}$$
Particularisons $\color{red}\text{(*)}$ avec $r=1$, on sait qu'il existe $$x_1\in\ ]0,1[, f(x)\le0$$ Etape 2, particularisons $\color{red}\text{(*)}$ avec $r=\frac{1}{2}$, on sait qu'il existe $$x_2\in\ \left]0,\frac{1}{2}\right[, f(x)\le0$$ Même processus pour l'étape 3 et ainsi de suite... 
En général, pour l'étape $n\in\mathbb{N}_0$, on particularise $\color{red}\text{(*)}$ avec $r=\frac{1}{n}$, on sait alors qu'il existe $$x_n\in\ \left]0,\frac{1}{n}\right[,f(x)\le0$$ On a construit une suite $(x_n)_{n\in\mathbb{N}}$ tel que $$\forall n\in\mathbb{N}_0,0<x_n<\frac{1}{n}\quad\text{ et }\quad f(x_n)\le0$$ Par le théorème de Sandwich, comme $$\frac{1}{n}\to 0$$, on a $$x_n\to 0$$ 
On considère $\frac{f(x_n)}{x_n}$, comme $$\frac{f(x_n)}{x_n}\underset{x_n\to 0}{\longrightarrow}1$$, on a $$\forall (y_n)\subseteq\operatorname{Dom}f\text{ \\ \{0\}},y_n\to0\Rightarrow\frac{f(y_n)}{y_n}\to 1$$ En particulier, pour $(y_n)=(x_n)$, on a, comme $$x_n\to0,\frac{f(x_n)}{x_n}\to1$$ Comme $$\forall n\in\mathbb{N}_0,x_n>0\quad\text{ et }\quad f(x_n)\le0$$ On a que $$\forall n\in\mathbb{N}_0,\frac{f(x_n)}{x_n}\le0$$ Par la limite d'inégalité, on a $$1\le0$$, ce qui est contradictoire et donc vrai.
