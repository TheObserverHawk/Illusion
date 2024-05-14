---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]

_Calculus : Continuité d'une fonction_
1. [[1.4.1 - Déf = Continuité d'une fonction]]

# Question 1 d'examen du juin 2022
## Enoncé : Soit $f : \mathbb{R}\to\mathbb{R}$ et $a\in\operatorname{Dom}f$. Posons $g : \mathbb{R}\to\mathbb{R} : x \to f(x+a)$. En utilisant la définition en termes de suites de la continuité (à rappeler), montrez que si $f$ est continue en $a$, alors $g$ est continue en 0. 
 Soit $f :\mathbb{R}\to\mathbb{R}, a\in\operatorname{Dom}f$ et $g : \mathbb{R}\to\mathbb{R} : x \to f(x+a)$ 
 Supposons que $f$ est continue en $a$ i.e. $$\forall (x_n)\subseteq\operatorname{Dom}f, (x_n\to a)\Rightarrow (f(x_n)\to f(a)$$
 Montrons que $g$ est continue en 0 i.e. $$\forall (x_n)\subseteq\operatorname{Dom}f, (x_n\to 0)\Rightarrow (f(x_n)\to f(0)$$
 Soit $(x_n)\subseteq \operatorname{Dom}g$ 
 Supposons que $$x_n\to 0$$ 
 Montrons que $$f(x_n) = f(0)$$
 On a $$g(x_n) =f(x_n+a)$$
 Comme $x_n\to 0$ par hypothèse, on a $$f(a)=g(0)$$ car $$g(0)=f(0+a)=f(a)$$
 