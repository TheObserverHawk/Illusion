---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.11.3.1 - Dérivée des fonctions hyperboliques]]
2. [[1.5.13 - Déf = Petit-o]]

_Calculus : Développement de Taylor_
1. [[1.8.1 - Formule = Développement de Taylor d'ordre ''n'' de ''f'']]
2. [[1.8.1.2 - Développement limité]]
3. [[1.8.2 - Thm = (Formule polynomiale de Taylor)]]


# Question  7 d'examen du janvier 2024
## Enoncé : Soit $g:\mathbb{R}\to\mathbb{R}$ une application telle que $g(x)=2x +\frac{1}{4}x^2+o(x^3)$ lorsque $x\to 0$. Donnez le développement de Taylor d’ordre 3 en 0 de la fonction $f:\mathbb{R}\to\mathbb{R}$ définie, pour tout $x\in\mathbb{R}$, par $f(x)=\sin(\cosh(g(x))+x^5)-2x^3+x+\frac{\pi}{2}-1$. Justifiez vos calculs en citant (sans démonstration) les règles de calcul sur les petits-o. La qualité de votre rédaction est importante. Rappel : pour tout $x\in\mathbb{R},\cosh(x)=\frac{e^x+e^{-x}}{2}$
Soit $g:\mathbb{R}\to\mathbb{R}$ tel que $$g(x)=2x+\frac{1}{4}x^2+o(x^3)$$ et $$f(x)=\underbrace{\underbrace{\sin}_{(4)}(\overbrace{\overbrace{\underbrace{\cosh}_{(2)}(\underbrace{g(x)}_{(1)}}^{(2.5)})+\overbrace{x^5-2x^3+x+\frac{\pi}{2}-1)}^{(3)}}^{(3.5)}}_{(4.5)}$$
On va calculer le développement de Taylor de $f(x)$ en le décomposant en plusieurs sous fonctions i.e. $$(1),(2), (2.5),(3),(3.5),(4)$$et de calculer leur développement de Taylor. 
\
_**(1) : Développement de Taylor de $g(x)$ d’ordre 3 en 0**_
Par definition du développement de $g(x)$ d’ordre 3 en 0, on en déduit qu’il vaut $$p(x)=2x+\frac{1}{4}x^2$$
\
_**(2) : Développement de Taylor de $\cosh(x)$ d’ordre 3 en $g(0)=2.0+\frac{1}{4}.0=0$**_
On a $$\begin{aligned}\partial\cosh(x)&=\sinh(x)\\\partial^2\cosh(x)&=\cosh(x)\\\partial^3\cosh(x)&=\sinh(x)\end{aligned}$$ Donc le développement de Taylor d’ordre 3 en 0 vaut $$\begin{aligned}\frac{\cosh(0)}{0!}x^0+\frac{\partial\cosh(0)}{1!}x^1+\frac{\partial^2\cosh(0)}{2!}x^2+\frac{\partial^3\cosh(0)}{3!}x^3&=\cosh(0)+\sinh(0)x+\frac{\cosh(0)}{2}x^2+\frac{\sinh(0)}{6}x^3\\&=\frac{e^0+e^{-0}}{2}+\frac{e^0-e^{-0}}{2}x+\frac{\frac{e^0+e^{-0}}{2}}{2}x^2+\frac{\frac{e^0-e^{-0}}{2}}{6}x^3\\&=1+0+\frac{1}{2}x^2+0\end{aligned}$$
Donc on a $$\cosh(x)=1+\frac{x^2}{2}+o(x^3)$$
\
_**(2.5) : Développement de Taylor de $h(x)=\cosh(g(x))$ d’ordre 3 en 0**_
Comme $$\cosh(x)=1+\frac{x^2}{2}+o(x^3)$$ et que $$g(x)=2x+\frac{1}{4}x^2$$On en déduit que $$\begin{aligned}\cosh(g(x))&=1+\frac{1}{2}.\left(2x+\frac{1}{4}x^2\right)^2+o(x^3)\\&=1+\frac{1}{2}.\left(4x^2+x^3+\frac{1}{16}x^4\right)+o(x^3)\\&=1+2x^2+\frac{x^3}{2}+o(x^3)\end{aligned}$$ car par les règles du petit-o :
1. $$x^m=o(x^n)\quad\text{ si }m>n$$
2. $$k.o(x^n)=o(x^n)\quad\forall k\in\mathbb{R}$$
3. $$o(x^n)+o(x^n)=o(x^n)$$

\
_**(3) : Développement de Taylor de $i(x)=x^5-2x^3+x+\frac{\pi}{2}-1$ d’ordre 3 en 0**_
On a $$i(x)=x^5-2x^3+x+\frac{\pi}{2}-1$$ par la règle du petit-o : $$x^m=o(x^n)\quad\text{ si }m>n$$ on obtient donc $$i(x)=-2x^3+x+\frac{\pi}{2}-1$$
\
_**(3.5) : Développement de Taylor de $j(x)=h(x)+i(x)$ d'ordre 3 en 0**_
Comme on sait que $$i(x)=-2x^3+x+\frac{\pi}{2}-1$$ et que $$h(x)=1+2x^2+\frac{x^3}{2}+o(x^3)$$ Donc, on a $$j(x)=\frac{\pi}{2}+x+2x^2-\frac{3}{2}x^3+o(x^3)$$
\
_**(4) : Développement de Taylor $\sin(x)$ d'ordre 3 en $$j(0)=\frac{\pi}{2}+0+2.0^2-\frac{3}{2}.0^3=\frac{\pi}{2}$$**_
On a $$\begin{aligned}\partial\sin(x)&=\cos(x)\\\partial^2\sin(x)&=-\sin(x)\\\partial^3\sin(x)&=-\cos(x)\end{aligned}$$Donc le développement de Taylor d’ordre 3 en $\frac{\pi}{2}$ vaut $$\begin{aligned}\frac{\sin(\frac{\pi}{2})}{0!}.\left(x-\frac{\pi}{2}\right)^0+\frac{\partial\sin(\frac{\pi}{2})}{1!}.\left(x-\frac{\pi}{2}\right)^1+\frac{\partial^2\sin(\frac{\pi}{2})}{2!}.\left(x-\frac{\pi}{2}\right)^2+\frac{\partial^3\sin(\frac{\pi}{2})}{3!}.\left(x-\frac{\pi}{2}\right)^3&=\sin\left(\frac{\pi}{2}\right).1+\cos\left(\frac{\pi}{2}\right).\left(x-\frac{\pi}{2}\right)-\frac{\sin(\frac{\pi}{2})}{2}.\left(x-\frac{\pi}{2}\right)^2-\frac{\cos(\frac{\pi}{2})}{6}.\left(x-\frac{\pi}{2}\right)^3\\&=1.1+0.\left(x-\frac{\pi}{2}\right)-\frac{1}{2}.\left(x-\frac{\pi}{2}\right)^2-0.\left(x-\frac{\pi}{2}\right)^3\\&=1-\frac{1}{2}.\left(x-\frac{\pi}{2}\right)^2\end{aligned}$$
Donc on a $$\sin(x)=1-\frac{1}{2}.\left(x-\frac{\pi}{2}\right)^2$$
\
_**(4.5) : Développement de Taylor $f(x)=\sin(\cosh(g(x))+x^5)-2x^3+x+\frac{\pi}{2}-1$ d’ordre 3 en 0**_
Comme on a $$j(x)=\frac{\pi}{2}+x+2x^2-\frac{3}{2}x^3+o(x^3)$$ et $$\sin(x)=1-\frac{1}{2}.\left(x-\frac{\pi}{2}\right)^2$$ on a que $$\begin{aligned}f(x)&=1-\frac{1}{2}.\left(\frac{\pi}{2}+x+2x^2-\frac{3}{2}x^3-\frac{\pi}{2}\right)^2+o(x^3)\\&=1-\frac{1}{2}.\left(x+2x^2-\frac{3}{2}x^3\right)^2+o(x^3)\\&=1-\frac{1}{2}.\left(x^2+2x^3-\frac{3}{2}x^4+2x^3+4x^4-3x^5-\frac{3}{2}x^4-3x^5+\frac{9}{4}x^6\right)+o(x^3)\\&=1-\frac{x^2}{2}-2x^3+o(x^3)\end{aligned}$$ par par les règles du petit-o :
1. $$x^m=o(x^n)\quad\text{ si }m>n$$
2. $$k.o(x^n)=o(x^n)\quad\forall k\in\mathbb{R}$$
3. $$o(x^n)+o(x^n)=o(x^n)$$

On a donc que le développement de Taylor de $f(x)$ d’ordre 3 en 0 : $$f(x)=1-\frac{x^2}{2}-2x^3$$
