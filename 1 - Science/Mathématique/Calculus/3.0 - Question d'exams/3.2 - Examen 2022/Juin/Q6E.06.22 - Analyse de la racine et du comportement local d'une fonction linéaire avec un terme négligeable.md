---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.13 - Déf = Petit-o]]



# Question 6 d'examen du juin 2022
## Enoncé : Soit $f:\mathbb{R}\to\mathbb{R}$ une application et $a ∈ \mathbb{R}$. Supposons qu’il existe $m,p\in\mathbb{R}$ tels que $m>0$ et $f(x)=mx+p+o(x +p/m)$ 
### a) Soit $g:\mathbb{R}\to\mathbb{R}$ une fonction et $x_0\in\mathbb{R}$. Définissez « $g$ est un $o(x−x_0)$ »
### b) Montrez que $x_0 :=-p/m$ est une racine de $f$ 
### c) Montrez qu'il existe un $r > 0$ tel que $∀x ∈ ]x_0, x_0 +r[, f(x) > 0$ où $x_0 := −p/m$.
**_a)_** On dit que $g$ est un $o(x-x_0)$ si 
1. $x_0 \in\operatorname{Dom}g$ et $g(x_0)=0$ 
2. $\underset{x\to x_0}{\operatorname{lim}}\frac{g(x)}{x-x_0}=0$ 

\
**_b)_** $\frac{-p}{m}$ est une racine de $f(x)$ si $f(x_0)=0$ 
On a $$\begin{aligned}f(x_0)&=m.\left(\frac{-p}{m}\right)+p+o(x-x_0)\\&=o(x-x_0)=0\end{aligned}$$
Regardons si $0=o(x-x_0)$
Posons $h(x)=0$, on a $$\begin{aligned}&0\in\operatorname{Dom}h\quad\text{ et }\quad h(0)=0\\&\underset{x\to x_0}{\operatorname{lim}}\frac{0}{x-x_0}=0\end{aligned}$$
On a donc bien que $\frac{-p}{m}$ est une racine de $f(x)$ 
\
**_c)_** $$\text{Commentaire de l'auteur : J'arrive pas}$$
