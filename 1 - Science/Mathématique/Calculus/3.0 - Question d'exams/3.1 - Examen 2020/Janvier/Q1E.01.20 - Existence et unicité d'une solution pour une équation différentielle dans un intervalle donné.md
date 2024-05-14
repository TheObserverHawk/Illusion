---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Continuité d'une fonction_
1. [[../../../1.4 - Continuité d'une limite de fonction/1.4.1 - Déf = Continuité d'une fonction|1.4.1 - Déf = Continuité d'une fonction]]
2. [[../../../1.4 - Continuité d'une limite de fonction/1.4.4 - Thm = Théorème des valeurs intermédiaires|1.4.4 - Thm = Théorème des valeurs intermédiaires]]

_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]
2. [[1.5.3 - Prop Prop 1 = Si ''f'' dériv en ''a'', alors ''f'' cont en ''a'']]
3. [[1.5.5 - Prop Prop 3 = Dériv des fonc composées]]
4. [[1.5.11 - Prop Prop 8 = Dériv des fonct trigonométriques]]

# Question 1 d'examen du janvier 2020
## Enoncé : soit $f:\mathbb{R}\to\mathbb{R}$ la fonction définie par $f(x)=2\cos^2(x)-\lambda.e^x$ où $\lambda\in\ \left]0,1\right]$ est un paramètre. Montrez que l’équation $\partial_x f(x)= 0$ possède un unique solution dans $[\frac{-\pi}{4},0]$ 
On a que $$\partial_x f(x)=-4\cos(x).\sin(x)-\lambda.e^x$$ On a que $\partial f(a)$ est continue car la multiplication et la dérivation de fonction continue est continue. 
1. $$\begin{aligned}\partial f\left(\frac{-\pi}{4}\right)&=-4\cos\left(\frac{-\pi}{4}\right).\sin\left(\frac{-\pi}{4}\right)-\lambda.e^{\frac{-\pi}{4}}\\&=-4.\frac{\sqrt{2}}{2}.\left(-\frac{\sqrt{2}}{2}\right)-\lambda.e^{\frac{-\pi}{4}}\\2&>2-\frac{\lambda}{e^{\frac{\pi}{4}}}\ge 2-\frac{1}{e^{\frac{\pi}{4}}}>2-\frac{1}{2}\quad\Rightarrow\quad \partial f\left(\frac{-\pi}{4}\right)> 0\end{aligned}$$
2. $$\begin{aligned}\partial f\left(0\right)&=-4\cos\left(0\right).\sin\left(0\right)-\lambda.e^{0}\\&=-4.1.0-\lambda.1=-\lambda\\ 0<\lambda\le 1&\iff -1\le-\lambda<0\quad\Rightarrow\quad \partial f\left(\frac{-\pi}{4}\right)< 0\end{aligned}$$

Donc on a bien $$\partial f\left(\frac{-\pi}{4}\right).\partial f(0)<0$$On peut donc appliquer le théorème des valeurs intermédiaires et il nous dit que dans nos conditions, il existe un $\xi\in\ ]\frac{-\pi}{4},0[$ tel que $$\partial f(\xi)=0$$