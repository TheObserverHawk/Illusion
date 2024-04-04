---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Algèbre linéaire : Sous-espace vectoriel_
1. [[2.1.1 - Sous-espace vectoriel]]
2. [[2.1.15 - Application linéaire]]
3. [[2.1.16 - Noyau d'une application linéaire]]
4. [[2.1.17 - Image d'une application linéaire]]

# Définition
Soit $L : V_1 → V_2$ une application linéaire. 
1. $$\operatorname{Ker}(L)$$ est un sous-espace vectoriel de $V_1$. 
2. $$\operatorname{Im}(L)$$ est un sous-espace vectoriel de $V_2$

#### Preuve
Soient $L_1$ et $L_2$ deux sous-espaces vectoriels 
Soit $L: L_1\to L_2$ une application linéaire 


\
\
Préconditions : on suppose que ces conditions sont vraies (donc il faut à prouver si ces conditions ne sont pas présumés être vraies)
1. $${\color{red}a)}\quad f(0)=0$$
2. $${\color{red}b)}\quad \forall v\in V_1, f(-v)=-f(v)$$
##### $\operatorname{Ker}(L)$ est un sous-espace vectoriel de $L_1$
$\operatorname{Ker}(L)$ est un sous-espace vectoriel de $L_1$ i.e. 
1. $$\operatorname{Ker}(L)\neq \varnothing$$
2. $$\forall v_1\in \operatorname{Ker}(L),\forall v_2\in \operatorname{Ker}(L), v_1+v_2\in \operatorname{Ker}(L)$$
3. $$\forall v\in \operatorname{Ker}(L),\forall\lambda\in\mathbb{R},\ \lambda.v\in \operatorname{Ker}(L)$$

On sait que $$\operatorname{Ker}(L) =\{a\in L_1|\ L(a)=E\}$$ On a que :
1. $$\operatorname{Ker}(L)\neq\varnothing\text{ i.e. }\exists a\in\operatorname{Ker}(L)\text{ i.e. }\exists a\in L_1, L(a)=0_{L_2}$$ Prenons $a=0_{L_1}\in L_1$ 
On a $$L(0_{L_1})=0_{L_2}$$ par ${\color{red}a)}$ 
2. Soient $v_1,v_2\in\operatorname{Ker}(L)$ i.e. $$L(v_1)=0\wedge L(v_2)=0$$
Montrons que $v_1+v_2\in\operatorname{Ker}(L)$ i.e. $$L(v_1+v_2)=0$$
On a que $$\begin{aligned}L(v_1+v_2) &= L(v_1)+L(v_2)\quad \text{ car }L\text{ est une application linéaire}\\&=0 + 0 = 0\end{aligned}$$
3. Soit $\lambda\in\mathbb{R}$, soit $v\in\operatorname{Ker}(L)$ i.e. $$L(v)=0$$
Montrons que $\lambda.v\in\operatorname{Ker}(L)$ i.e. $$L(\lambda.v)=0$$
On a que $$\begin{aligned}L(\lambda.v)&=\lambda.L(v)\quad\text{ car }L\text{ est une application linéaire}\\&=\lambda.0=0\end{aligned}$$
##### $\operatorname{Im}(L)$ est un sous-espace vectoriel de $L_2$
 $\operatorname{Im}(L)$ est un sous-espace vectoriel de $L_2$ i.e. 
1. $$\operatorname{Im}(L)\neq \varnothing$$
2. $$\forall v_1\in \operatorname{Im}(L),\forall v_2\in \operatorname{Im}(L), v_1+v_2\in \operatorname{Im}(L)$$
3. $$\forall v\in \operatorname{Im}(L),\forall\lambda\in\mathbb{R},\ \lambda.v\in \operatorname{Im}(L)$$

On sait que $$\operatorname{Im}(L)=\{v_2\in L_2|\ \exists v_1\in L_1, L(v_1)=v_2\}$$
On a que 
1. $$\operatorname{Im}(L)\neq\varnothing\text{ i.e. }\exists v_2\in L_2\text{ i.e. }\exists v_2\in L_2|\ \exists L_1\in L_1, f(v_1)=v_2$$
Prenons $v_2=0_{L_2}$, on a que $$L(0_{L_1})=0_{L_2}$$ par ${\color{red}a)}$ 
2. Soient $v_1,v_2\in\operatorname{Im}(L)$ i.e. $$\begin{aligned}&\exists v_1'\in L_1, L(v_1')=v_1\text{ et }\\&\exists v_2'\in L_2, L(v_2')=v_2\end{aligned}$$
Montrons que $v_1+v_2\in\operatorname{Im}(L)$ i.e. $$\exists v_3\in L_1, L(v_3)=v_1+v_2$$
Prenons $v_3=v_1'+v_2'\in L_1$ 
On a que $$\begin{aligned}L(v_3)&=L(v_1'+v_2')=L(v_1')+L(v_2')\quad\text{ car }L\text{ une application linéaire}\\&=v_1+v_2\end{aligned}$$
3. Soit $\lambda\in\mathbb{R}$, soit $v\in\operatorname{Im}(L)$ i.e. $$\exists v_1'\in L_1, L(v_1')=v_1$$
Montrons que $\lambda.v\in\operatorname{Im}(L)$ i.e. $$\exists v_2'\in L_1, L(v_2')=\lambda.v$$ Prenons $v_2'=\lambda.v_1'\in\operatorname{Im}(L)$ 
On a $$\begin{aligned}L(v_2')&=L(\lambda.v_1')=\lambda.L(v_1')\quad\text{ car }L\text{ une application linéaire}\\&=\lambda.v_1\end{aligned}$$
