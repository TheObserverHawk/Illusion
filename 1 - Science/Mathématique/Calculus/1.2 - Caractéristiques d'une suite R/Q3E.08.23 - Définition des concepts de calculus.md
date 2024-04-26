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
1.

_Calculus : Continuité d'une fonction_
1.

_Calculus : Dérivée de fonctions d'une variable_
1.

_Calculus : Théorème de la moyenne_
1.

_Calculus : Dérivée d'ordre supérieur_
1.

_Calculus : Développement de Taylor_
1.

_Calculus : Série_
1. 

# Question 3 d'examen de août 2022
## Enoncé :
### $a$) Soient $(x_n)_{n∈\mathbb{N}}$ et $(y_n)_{n∈\mathbb{N}}$ des suites réelles, $f : \mathbb{R} → \mathbb{R}$ une fonction et $a ∈ \operatorname{Dom} f$ . 
#### Définissez $(x_n)_{n∈\mathbb{N}}$ est non bornée : 
$$\begin{aligned}\text{bornée }&\to\exists R_1,R_2\in\mathbb{\mathbb{R}},\forall n\in\mathbb{N},\quad R_1 \le x_n\le R_2\quad\text{ i.e. }\quad R_1\le x_n\cap x_n\le R_2\\\text{non bornée }&\to\forall R_1, R_2\in\mathbb{R},\exists n\in\mathbb{N},\quad R_1>  x_n\cup x_n>R_2\end{aligned}$$
#### Définissez $(y_n)_{n∈\mathbb{N}}$ est une sous-suite de $(x_n)_{n∈\mathbb{N}}$ :
$$\exists\varphi:\mathbb{N}\to\mathbb{N}, \text{ strictement croissante  tels que }\forall n\in\mathbb{N}, y_n=x_{\varphi(n)}$$
#### Définissez $a$ est un point minimum de $f$
$$\forall x\in\operatorname{Dom}f, f(x)\ge f(a)$$
### $b$) Donnez un exemple d’une suite $(x_n)_{n∈\mathbb{N}}$ non bornée qui possède une sous-suite $(y_n)_{n∈\mathbb{N}}$ convergeant au sens strict. Le fait que votre exemple satisfasse ce qui est demandé doit être rigoureusement établi.
Prenons $$x_n=\begin{cases}x\quad\text{ si } n\in2\mathbb{N}\\1\quad\text{ si }n\in2\mathbb{N}+1\end{cases}$$ On a bien que $x_n$ est non bornée, et prouvons le 
Soient $R_1, R_2\in\mathbb{R}$ 
Prenons $$n=[2R_2]$$ On a : $$x_n> R_2\iff [2R_2]\ge R_2$$ car $|2R_1|>R_2$ et par la définition de la partie entière
\
Prenons $$(y_n)_{n\in\mathbb{N}}=(x_{2n})_{n\in\mathbb{N}}$$ on a bien que $(y_n)_{n\in\mathbb{N}}$ est une sous-suite de $(x_n)_{n\in\mathbb{N}}$ car 
1. Prenons $$\varphi:\mathbb{N}\to\mathbb{N}:n\mapsto 2n$$ Montrons que $\varphi$ est strictement croissante i.e. $$\forall$$