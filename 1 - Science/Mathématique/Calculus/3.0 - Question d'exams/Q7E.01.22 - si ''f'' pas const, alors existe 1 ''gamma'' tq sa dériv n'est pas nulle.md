---
tags:
  - Note_done
  - Math
source: UMons - Calculus
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]

_Calculus : Théorème de la moyenne_
1. [[1.6.3 - Thm = Théorème de la moyenne]]
2. [[1.6.3.2 - Prop = Si dériv de ''f'' sur ''I'' est 0, alors ''f'' est const sur ''I'']]

_Calculus : Dérivée d'ordre supérieure_
1. [[1.7.1 - Prop = Classe de fonctions]]
2. [[1.7.3 - Déf = (Classe de fonctions dérivables)]]

_Math élémentaire : Logique_
1. [[0.2.8 - Preuve par l'absurde]]

# Question 7 d'examen du janvier 2022
## Enoncé : Soit $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$. Montrez que si $f$ n’est pas constante, alors il existe nécessairement au moins un $γ ∈ \mathbb{R}$ tel que $∂ f(γ) \neq 0$. Expliquez votre démarche. Indication : La question 6 peut vous être utile.
Soit $f$ n'est pas constante
Argumentons par contradiction et supposons au contraire que la thèse n’est pas vérifiée, à savoir : 
1. $f$ n'est pas constante et $∀γ ∈ \mathbb{R}, ∂ f(γ) = 0$. 

On a vu au cours que cela impliquait que $f$ est constante, ce qui donne la contradiction recherchée. 
Montrons cette dernière implication : soient $x_1 \neq x_2$ deux réels arbitraires et prouvons que $$f(x_1) = f(x_2)$$ Puisque $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$, elle est en particulier continue sur $[x_1, x_2]$ et dérivable sur $]x_1, x_2[$. 
On peut donc appliquer le théorème de la moyenne i.e. 

---
Soit $f : [a;b] \to \mathbb{R}$ 
1. une fonction continue sur $[a;b]$ et 
2. dérivable sur $]a;b[$ (avec $a < b$ ou $a >b$)

alors il existe $\xi \in\ ]a;b[$ tel que $$\begin{align*}f(b)-f(a) &=\partial f(\xi)(b-a) \\ \iff \frac{f(b)-f(a)}{b-a} &= \partial f(\xi)  \end{align*}$$

---

et on obtient l’existence d’un $ξ ∈\ ]x_1, x_2[$ tel que $$f(x_2)-f(x_1)=\partial f(\xi)(x_2-x_1)$$Comme la dérivée est nulle partout, on a en particulier que $∂ f(ξ ) = 0$ et donc que $$f(x_2)− f(x_1) = 0$$, ce qu’on voulait démontrer
