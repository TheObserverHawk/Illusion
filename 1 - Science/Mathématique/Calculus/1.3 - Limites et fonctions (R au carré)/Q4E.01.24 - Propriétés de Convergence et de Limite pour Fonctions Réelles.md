---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]
2. [[1.3.2 - Déf = Voisinage (Calculus)]]
3. [[1.3.3 - Déf = Adhérence]]
4. [[1.3.4 - Thm = Théorème de localité]]


# Question  4 d'examen du janvier 2024
## Enoncé :
### $a)$ Soient $(x_n)_{n\in\mathbb{N}}\subseteq\mathbb{R}$ et $a\in\mathbb{R}$. Traduisez la phrase suivante en une formule quantifiée : "Quel que soit l'intervalle centré en $a$, il existe un moment à partir duquel les éléments de la suite appartiennent à cet intervalle"
### $b)$ Soient $f:\mathbb{R}\to\mathbb{R}$ une fonction; $a\in\operatorname{adh(Dom}f)$ et $b\in\mathbb{R}$. Montrez que $\underset{x\to a}{\operatorname{lim}}f(x)=b$ si et seulement si $\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$. INDICATION : vous pouvez utiliser, sans le démontrer, le fait que si une suite $(x_n)_{n\in\mathbb{N}}$ converge vers un réel $a$, alors la formule donnée au point $(a)$ est vérifiée
#### $a)\text{ traduction}$
$$\forall r> 0,\exists n^*\in\mathbb{N},\forall n\ge n^*,\ x_n\in[a-r,a+r]$$
#### $b) \underset{x\to a}{\operatorname{lim}}f(x)=b\quad\iff\quad\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$
##### $$\underset{x\to a}{\operatorname{lim}}f(x)=b\quad\Rightarrow\quad\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$$
Supposons que $$\underset{x\to a}{\operatorname{lim}}f(x)=b$$ i.e. $$\forall(x_n)\subseteq \operatorname{Dom}f, (x_n\to a)\Rightarrow (f(x_n)\to f(a)=b)\quad\color{red}(*)$$
Montrons que $$\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$$ i.e. $$\forall(y_n)\subseteq \operatorname{Dom}f\cap[a-r,a+r], (y_n\to a)\Rightarrow (f(y_n)\to f(a)=b)\quad$$
Soit $(y_n)_{n\in\mathbb{N}}\subseteq\operatorname{Dom}f\cap[a-r,a+r]$ 
Montrons que $$y_n\to a\Rightarrow f(y_n)\to b$$
Supposons $$y_n\to a$$
Montrons que $$f(y_n)\to b$$
Par l'hypothèse $\color{red}(*)$ avec $(x_n)=(y_n)$, on a, comme $$(y_n)\subseteq\operatorname{dom}f\quad\text{ et }\quad y_n\to a$$ on a que $$f(y_n)\to b$$
##### $$\underset{x\to a}{\operatorname{lim}}f(x)=b\quad\Leftarrow\quad\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$$
Supposons que $$\underset{\overset{x\to a}{x\in[a-2,a+2]}}{\operatorname{lim}}f(x)=b$$ i.e. $$\forall(y_n)\subseteq \operatorname{Dom}f\cap[a-r,a+r], (y_n\to a)\Rightarrow (f(y_n)\to f(a)=b)\quad\color{red}(**)$$
Montrons que $$\underset{x\to a}{\operatorname{lim}}f(x)=b$$ i.e. $$\forall(x_n)\subseteq \operatorname{Dom}f, (x_n\to a)\Rightarrow (f(x_n)\to f(a)=b)\quad$$
Soit $(x_n)_{n\in\mathbb{N}}\subseteq\operatorname{Dom}f$
Montrons que $$x_n\to a\Rightarrow f(x_n)\to b$$
Supposons que $$x_n\to a$$ 
Montrons que $$f(x_n)\to b$$ Comme $x_n\to a$, on a par le point $(a)$ que $$\forall r> 0,\exists n^*\in\mathbb{N},\forall n\ge n^*,\ x_n\in[a-r,a+r]$$ En particulier, pour $r=2>0$, on sait qu'il existe un $n^*\in\mathbb{N}$ tel que $$\forall n\ge n^*, x_n\in[a-2,a+2]$$
On considère $$(z_n)_{n\ge N}=(x_n)_{n\ge n^*}$$ on a que $$(z_n)_{n\ge N}\subseteq (x_n)_{n\in\mathbb{N}}$$ Donc, $z_n\to a$ par propriétés de sous-suites
De plus, $$\forall n\in\mathbb{N}, z_n\in[a-2,a+2]\cap\operatorname{dom}f$$ par $\color{red}(**)$, avec $(y_n)=(z_n)$, on a $f(z_n)\to b$ 
Comme $(z_n)$ est une sous-suite exhaustive de $(x_n)$ 
On a que $(f(z_n))$ est une sous-suite exhaustive de $(f(x_n))$ 
Comme $$f(z_n)\to b$$, on a lorsque $$f(x_n)\to b$$
