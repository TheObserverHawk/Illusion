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
# Définition
Soient $E_1, E_2$ et $E_3$ 3 R-espaces vectoriels. 
Soient $f:E_1\to E_2$ et $g:E_2\to E_3$ deux applications linéaires
Prouvez que $g\circ f$ est une application linéaire
_Remarque_ : $$\forall x\in E_1, g\circ f(x)=g(f(x))$$
Montrons que $$\begin{aligned}\forall u,v\in E_1, (g\circ f)(u+v)&=(g\circ f)(u)+(g\circ f)(v)\\\forall x\in E_1,\forall \lambda\in\mathbb{R},(g\circ f)(\lambda. x)&=\lambda(g\circ f)(x)\end{aligned}$$
##### $\forall u,v\in E_1, (g\circ f)(u+v)=(g\circ f)(u)+(g\circ f)(v)$ 
Soient $u,v\in E_1$ 
On a $$g(f(u+v))=g(f(u)+f(v))$$ car $f$ est une application linéaire et $u,v\in E_1$  $$g(f(u+v))=g(f(u))+g(f(v))$$ car $f(u), f(v)\in E_2$ et $g$ est une application linéaire 
##### $\forall x\in E_1,\forall \lambda\in\mathbb{R},(g\circ f)(\lambda. x)=\lambda(g\circ f)(x)$ 
Soient $x\in E_1,\lambda x\in\mathbb{R}$  
On a $$g(f(\lambda .x))=g(\lambda.f(x))$$ car $f$ est une application linéaire $$g(\lambda.f(x))=\lambda.g(f(x))$$ car $g(f(x))$ est une application linéaire
