---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Théorème de la moyenne_
1. [[../../../1.6 - Théorème de la moyenne/1.6.3 - Thm = Théorème de la moyenne|1.6.3 - Thm = Théorème de la moyenne]]
2. [[../../../1.6 - Théorème de la moyenne/1.6.3.3 - Prop = Si ''f'' croissante, alors dériv de ''f'' sur ''I'' est positif|1.6.3.3 - Prop = Si ''f'' croissante, alors dériv de ''f'' sur ''I'' est positif]]

_Calculus : Dérivée d'ordre supérieur_
1. [[1.7.1 - Prop = Classe de fonctions]]
2. [[1.7.3 - Déf = (Classe de fonctions dérivables)]]

_Math élémentaire : Inégalité_
1. [[../../../../Math élémentaire/1 - Fonction et Inéquation/1.2 - Fonction/1.2.2 - Fonction strictement croissant|1.2.2 - Fonction strictement croissant]]

# Question 8 d'examen du janvier 2020
## Enoncé : Soit $f ∈ \mathscr{C}^1 ([a,b];\mathbb{R})$ où $a < b$ sont deux réels.
### Définissez « $f$ est strictement croissante sur $[a,b]$ »
$$∀ x_1,\ x_2 ∈ [a,b] ∩ \operatorname{dom} f, x_1 < x_2 ⇒ f(x_1) < f(x_2)$$ 
### Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse.
#### a) $(\forall x\in\ ]a,b[, \partial f(x)>0)\quad\Rightarrow\quad f$ est strictement croissante sur $[a,b]$ 
_Réponse_ : Vrai
\
Supposons que $$\forall x \in\ ]a,b[\ ,\ \partial f(x)>0$$Montrons que $f$ est strictement croissante sur $[a,b]$ i.e. $$\forall x_1, x_2 \in\ [a,b],\ x_1 < x_2 \Rightarrow f(x_1) < f(x_2)$$
Soient $x_1,\ x_2 \in\ [a,b]$ tels que $$x_1 < x_2$$Montrons que $$f(x_1) < f(x_2)$$
Appliquons le théorème de la moyenne sur $[x_1, x_2]$
On a donc un $\xi \in\ ]x_1, x_2[$ tel que $$f(x_2) - f(x_1) = \underbrace{\partial f(\xi)}_{> 0 \text{ par hyp }}\underbrace{(x_2-x_1)}_{> 0} > 0$$D'où $f(x_2) - f(x_1) > 0$ i.e. $f(x_2) > f(x_1)$ 
#### b) $(\forall x\in\ ]a,b[, \partial f(x)>0)\quad\Leftarrow\quad f$ est strictement croissante sur $[a,b]$ 
_Réponse_ : Faux, si $\forall n \in \mathbb{N},\ x_n > 0$ a-t-on $\operatorname{lim} x_n > 0$ ? Non car par passage de la limite, les sens d'inégalités deviennent larges !
\
Donnons un contre-exemple i.e. que 
1. $f$ est strictement croissante sur $[a,b]$ et $\exists x \in\ ]a,b[\ ,\ \partial f(x) \le 0$ 

Prenons $f(x) = x^3$
Cette fonction possède bien une dérivée continue sur $\mathbb{R}$ et est strictement croissante.
Cette fonction vérifie aussi $$∃x ∈ \mathbb{R}, ∂ f(x) \le 0$$ Il suffit en effet de prendre $x = 0$ et de constater que $$\left.\partial f(0) = 3x^2 \right|_{x=0} = 0 \le0$$