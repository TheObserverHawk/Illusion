---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]

_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]

_Calculus : Théorème de la moyenne_
1. [[1.6.3.4 - Prop = Si ''f'' décroissante, alors dériv de ''f'' sur ''I'' est négatif]]

_Calculus : Dérivée d'ordre supérieure_
1. [[1.7.1 - Prop = Classe de fonctions]]
2. [[1.7.3 - Déf = (Classe de fonctions dérivables)]]

_Math élémentaire : Inégalité_
1. [[1.2.4 - Fonction strictement décroissante]]

# Question 8 point a d'examen du janvier 2022
## Enoncé : Supposons que $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$. Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse. Justifiez vos réponses par une preuve ou un contre-exemple.
### Question 8.$a$ : Si $f$ est strictement décroissante, alors $\forall x \in \mathbb{R},\ \partial f(x) \le 0$ 
_Réponse_ : Vrai
Sous l'hypothèse de décroissance stricte de $f$ i.e. $$\forall x_1,\ x_2 \in \operatorname{Dom}f,\ x_1 < x_2 \Rightarrow f(x_1) < f(x_2)$$
On veut montrer que $$\forall x \in \mathbb{R},\ \underset{t\to x}{\operatorname{lim}}\frac{f(t)-f(x)}{t-x} \le0$$
Cette limite existe car on a supposé que $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$ et donc $f$ est dérivable en tout point de $\mathbb{R}$ 
Puisque cette limite existe, alors la même limite avec une contrainte additionnelle existe aussi et vaut la même valeur. En particulier, on a $$\partial f(x)=\lim\limits_{t\to x}\frac{f(t)-f(x)}{t-x}=\lim\limits_{\overset{t\to x}{t > x}}\frac{f(t)-f(x)}{t-x}$$
Pour les $t ∈ \mathbb{R}$ tels que $t > x$, la décroissance de $f$ implique qu’on aie $f(t) < f(x)$ ou encore $f(t)− f(x) < 0$. 
Donc $$\forall t>x,\quad\frac{f(t)-f(x)}{t-x}<0$$
En passant à la limite lorsque $t → x$, on obtient bien $$\begin{aligned}\partial f(x)=\lim_{\overset{t\to x}{t > x}}\frac{f(t)-f(x)}{t-x}\leqslant0\end{aligned}$$
