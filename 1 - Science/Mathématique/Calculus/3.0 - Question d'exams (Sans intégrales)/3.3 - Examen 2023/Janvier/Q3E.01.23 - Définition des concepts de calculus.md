---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Convergence d’une suite de réel_
1. [[../../../1.1 - Convergence/1.1.5 - Déf = Sous-suite|1.1.5 - Déf = Sous-suite]]

_Calculus : Caractéristique d'une suite_
1. [[1.2.1 - Prop = Suite bornée]]
2. [[1.2.4 - Prop = Suite majorée]]
3. [[1.2.5 - Prop = Suite minorée]]
4. [[1.2.7 - Thm = (Convergence bornée)]]

_Math discrète : Relation d'ordre_
1. [[../../../../Math informatique/1 - Math discrète/1.4 - Relation d'ordre/1.4.8.3 - Minimum|1.4.8.3 - Minimum]]
# Question 3 point $a$ d'examen de janvier 2023
## Enoncé :
### $a$) Soient $(x_n)_{n∈\mathbb{N}}$ et $(y_n)_{n∈\mathbb{N}}$ des suites réelles, $f : \mathbb{R} → \mathbb{R}$ une fonction et $a ∈ \operatorname{Dom} f$ . 
#### Définissez $(x_n)_{n∈\mathbb{N}}$ est non bornée : 
$$\begin{aligned}\text{bornée }&\to\exists R_1,R_2\in\mathbb{\mathbb{R}},\forall n\in\mathbb{N},\quad R_1 \le x_n\le R_2\quad\text{ i.e. }\quad R_1\le x_n\cap x_n\le R_2\\\text{non bornée }&\to\forall R_1, R_2\in\mathbb{R},\exists n\in\mathbb{N},\quad R_1>  x_n\cup x_n>R_2\end{aligned}$$
#### Définissez $(y_n)_{n∈\mathbb{N}}$ est une sous-suite de $(x_n)_{n∈\mathbb{N}}$ :
$$\exists\varphi:\mathbb{N}\to\mathbb{N}, \text{ strictement croissante  tels que }\forall n\in\mathbb{N}, y_n=x_{\varphi(n)}$$
#### Définissez $a$ est un point minimum de $f$
$$\forall x\in\operatorname{Dom}f, f(x)\ge f(a)$$
### $b)$ Donnez un exemple d'une suite $(x_n)_{n\in\mathbb{N}}$ non bornée qui possède une sous-suite $(y_n)_{n\in\mathbb{N}}$ converge au sens strict. Le fait que votre exemple satisfasse ce qui est demandé doit être rigoureusement établi
(Pas sûr, à voir)
\
Prenons $$x_n=\begin{cases}n\quad\text{ si }n\in3n\\1\quad\text{ si }n\in3n+1\\-n\quad\text{ si } n\in3n+2\end{cases}$$ On a bien que $x_n$ est non bornée, prouvons le
Soient $R_1,R_2\in\mathbb{N}$, supposons par l'absurde que $x_n$ est bornée i.e. $$\exists R_1,R_2\in\mathbb{R},\quad R_1\le x_n\cap x_n\le R_2$$ prenons $$R_1=-2\quad\text{ et }\quad R_2=2$$ On a alors $$-2\le x_n\le 2$$ Or, pour $n=1$ on a que $$\begin{aligned}x_n&=-5\quad\text{ pour }n\in3n+2\\x_n&=3\quad\text{ pour }n\in3n\end{aligned}$$ ce qui est une contradiction, par conséquent, $x_n$ est non bornée
Prenons $$(y_n)_{n\in\mathbb{N}}=(x_{3n+1})_{n\in\mathbb{N}}$$ qui est une sous-suite de $(x_n)_{n\in\mathbb{N}}$ car
1. Prenons $$\varphi:\mathbb{N}\to\mathbb{N}:n\mapsto3n+1$$Montrons que $\varphi$ est strictement croissante i.e. $$\forall x_1,x_2\in\operatorname{Dom}\varphi,\quad x_1<x_2\quad\Rightarrow\quad \varphi(x_1)<\varphi(x_2)$$ Soit $n\in\mathbb{N}$, on a $$\begin{aligned}n_1<n_2\quad\Rightarrow\quad 3n_1+1&<3n_2+1\\\varphi(n_1)&<\varphi\end{aligned}$$