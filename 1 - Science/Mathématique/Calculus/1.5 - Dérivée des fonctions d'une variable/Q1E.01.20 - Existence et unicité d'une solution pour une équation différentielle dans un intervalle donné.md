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

# Question 1 d'examen du janvier 2020
## Enoncé : soit $f:\mathbb{R}\to\mathbb{R}$ la fonction définie par $f(x)=2\cos^2(x)-\lambda.e^x$ où $\lambda\in\ \left]0,1\right]$ est un paramètre. Montrez que l’équation $\partial_x f(x)= 0$ possède un unique solution dans $[\frac{-\pi}{4},0]$ 
On a que $$\partial_x f(x)=-4\cos(x).\sin(x)-\lambda.e^x$$ On a que $\partial f(a)$ est continue car la multiplication et la dérivation de fonction continue est continue. 
1. $$\begin{aligned}\partial f\left(\frac{-\pi}{4}\right)&=-4\cos\left(\frac{-\pi}{4}\right).\sin\left(\frac{-\pi}{4}\right)-\lambda.e^{\frac{-\pi}{4}}\\&=-4.\frac{\sqrt{2}}{2}.\left(-\frac{\sqrt{2}}{2}\right)-\lambda.e^{\frac{-\pi}{4}}\\2&>2-\frac{\lambda}{e^{\frac{\pi}{4}}}\ge 2-\frac{1}{e^{\frac{\pi}{4}}}>2-\frac{1}{2}\quad\Rightarrow\quad \partial f\left(\frac{-\pi}{4}\right)> 0\end{aligned}$$
2. $$\begin{aligned}\partial f\left(0\right)&=-4\cos\left(0\right).\sin\left(0\right)-\lambda.e^{0}\\&=-4.1.0-\lambda.1=-\lambda\\ 0<\lambda\le 1&\iff -1\le-\lambda<0\quad\Rightarrow\quad \partial f\left(\frac{-\pi}{4}\right)< 0\end{aligned}$$

On peut donc appliquer le théorème des valeurs intermédiaires et il nous dit que dans nos conditions, il existe un $\xi\in$ tel que $$$$