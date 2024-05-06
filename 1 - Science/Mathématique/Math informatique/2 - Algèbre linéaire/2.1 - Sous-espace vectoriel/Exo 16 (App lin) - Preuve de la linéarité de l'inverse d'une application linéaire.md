---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Algèbre linéaire : SEV_
1. [[2.1.1 - Sous-espace vectoriel]]
2. [[2.1.15 - Application linéaire]]

_Math élémentaire : Logique_
1. [[0.5.8 - Composition de fonctions]]
# Exo 16
## Enoncé : Soit $f:E_1\to E_2$ une application linéaire où $E_1$ et $E_2$ sont des R-espaces vectoriels. Sous l'hypothèse où $f$ admet une fonction inverse $g:E_2\to E_1$. Prouvez que $g$ est une application linéaire 
Soient $a,b\in E_2$, on sait que $$\exists c\in E_1, f(c)=a\quad\wedge\quad\exists d\in E_1,f(d)=b$$
1. On a $$\begin{aligned}g(a+b)&=g(f(c)+f(d))\\&=g(f(c+d))\quad\text{ car }f\text{ est une AL}\\&=c+d\quad\text{ car }\forall v\in E_1, (g\circ f)(v)=v\\&=g(f(c))+g(f(d))\\&=g(a)+g(b) \end{aligned}$$
2. On a $$\begin{aligned}g(\lambda.a)&=g(\lambda.f(c))\\&=g(f(\lambda.c))\quad\text{ car } f\text{ est une AL}\\&=\lambda.c\\&=\lambda.g(f(c))\\&=\lambda.g(a)\end{aligned}$$
