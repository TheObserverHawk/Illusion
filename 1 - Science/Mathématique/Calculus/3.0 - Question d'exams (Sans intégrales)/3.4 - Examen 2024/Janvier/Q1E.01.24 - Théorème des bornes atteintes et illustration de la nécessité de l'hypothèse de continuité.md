---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Caractéristique d'une suite_
1. [[1.2.1 - Prop = Suite bornée]]
2. [[1.2.4 - Prop = Suite majorée]]
3. [[1.2.5 - Prop = Suite minorée]]

_Calculus : Continuité d'une fonction_
1. [[1.4.6 - Thm = Théorème des bornes atteintes]]

_Math élémentaire : Inégalité_
1. [[1.2.7 - Graphe d'une fonction]]

# Question 1 d'examen du janvier 2024
## Enoncé : 
### a) Enoncez le théorème des bornes atteintes. Interprétez le géométriquement en veillant à faire un lien explicite et argumenté entre l'énoncé et les objets géométriques 
#### Résolution du point $a$ 
Soient $a,b\in\mathbb{R}$ tel que $a<b$ 
Soit $f:[a,b]\to \mathbb{R}$ une application continue, alors $$\exists x_\min,x_\max\in[a,b],\forall x \in[a,b], f(x_\min)\le f \le f(x_\max)$$
**Interprétation géométrique** : ![[IMG_4952.jpeg]]
La fonction est bornée supérieurement et inférieurement et elle atteint les bornes. Le théorème nous affirme qu'il existe un point $$(x_\min,f(x_\min))$$ du graphes de ma fonction tel que le graphe de $f$ sera toujours au-dessus de la droite horizontale $$D_\min$$ passant par ce point. La Droite $D_\min$ ayant pour équation : $$D_\min\equiv y=f(x_\min)$$ On a donc que $$\forall x\in[a,b],\ f(x)\ge f(x_\min)$$ Donc de manière similaire, on a un point $$(x_\max,f(x_\max))$$ du graphe de $f$ tel que le graphe de $f$ sera toujours en dessous de la droite horizontale $$D_\max\equiv y=f(x_\max)$$ Cela se traduit par l'inégalité suivante : $$\forall x\in[a,b],\ f(x)\le f(x_\max)$$
### b) Donnez un exemple de fonction $f:\mathbb{R}\to\mathbb{R}$ qui illustre que si on retire l'hypothèse de continuité dans l'énoncé du théorème, alors la conclusion du théorème n'est plus vérifiée. Le fait que votre exemple satisfasse ce qui est demandé doit être rigoureusement établi.
#### Résolution du point $b$
On considère $a:1$ et $b=2$, on définit $$f:[1,2]\to\mathbb{R}:x\mapsto\begin{cases}x\quad\text{ si }x\neq 2\\ 1\quad\text{ si }x=2\end{cases}$$
**Illustration** : ![[IMG_4953.jpeg]]
Montrons que $$\forall x_\min,x_\max\in[1,2],\ \exists x\in[1,2]\text{ tel que }f(x_\min)> f(x)\text{ ou }f(x_\max)<f(x)$$
Soient $x_\min, x_\max\in[1,2]$, 
1. si $x_\max\neq 2$, alors prenons $$x=\frac{x_\max + 2}{2}\in[1,2]$$ car $$\begin{aligned}1\le\ &x_\max < 2\\\text{i.e. }3\le\ &x_\max+2 < 4\\\text{i.e. }\frac{3}{2}\le\ &\frac{x_\max+2}{2}<2\end{aligned}$$ Donc $$x\in[1,2[$$ On a que $$f(x)>f(x_\max)\text{ i.e. }x>x_\max$$ car $x\neq 2$ et $x_\max\neq 2$. Donc $$\begin{aligned}f(x)>f(x_\max)&\text{ i.e. }\frac{x_\max + 2}{2}>x_\max\\&\text{i.e. } 2>x_\max \end{aligned}$$ par hypothèse $x_\max \neq 2$ et donc ok
2. Si $x_\max = 2$, prenons $$x=\frac{3}{2}\in[1,2]$$ On a $$f(x)>f(x_\max)$$ car $\frac{3}{2}> 1$ 