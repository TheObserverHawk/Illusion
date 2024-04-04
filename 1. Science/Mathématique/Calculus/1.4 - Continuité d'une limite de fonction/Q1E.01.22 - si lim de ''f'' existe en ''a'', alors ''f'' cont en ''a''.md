---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]

_Calculus : Continuité d’une fonction_
1. [[1.4.1 - Déf = Continuité d'une fonction]]

# Question 1 d’examen de Calculus du Janvier 2022 (01/22) : 
## Énoncé : Soit $f : \mathbb{R} → \mathbb{R}$ et $a ∈ \operatorname{Dom} f$. En utilisant la définition en termes de suites de la continuité (à rappeler),  montrez que si $\underset{x\to a}{\operatorname{lim}}f(x)$ existe, alors $f$ est continue en $a$ 
Comme l’énoncé le stipule, il s’agit d’utiliser la définition en termes de suite de la continuité de $f$ en $a$.
1. Rappelons de cette définition :
	La fonction $f$ est continue en $a$ si et seulement si $$\underset{x \to a}{\operatorname{lim}}f(x) = f(a)$$  i.e. $$\forall (x_n) \subseteq \operatorname{Dom}f,\ x_n \to a \Rightarrow f(x_n) \to f(a)$$
2. Il faut comprendre que l’hypothèse “$\underset{x \to a}{\operatorname{lim}}f(x)$ existe” veut dire $$\exists b \in \mathbb{R},\ \underbrace{\forall (x_n) \subseteq \operatorname{Dom}f,\ x_n \to a \Rightarrow f(x_n) \to b}_{(a)}$$

En comparant les deux définitions, on se rend compte que le travail à réaliser consiste à montrer que le $b$ dont $(2)$ affirme l’existence est en fait $f(a)$ puisqu’alors $(a)$ sera exactement la définition de continuité. 
Or, en particularisant $(2)$ à la suite constante $(x_n) := (a)$ 
(qui est bien dans le domaine de $f$ vu qu’on a supposé que $a ∈ \operatorname{Dom}f$), 
on a $$x_n → a ⇒ f(x_n) → b$$ 
Bien entendu, la suite constante $(x_n)=(a)$ converge vers $a$ et on a donc $$f(a)= f(x_n)→b$$
Mais la suite $(f(x_n))$ est la suite constante $( f (a))$ qui converge aussi vers $f (a)$
Par unicité de la limite $$b = f (a)$$


