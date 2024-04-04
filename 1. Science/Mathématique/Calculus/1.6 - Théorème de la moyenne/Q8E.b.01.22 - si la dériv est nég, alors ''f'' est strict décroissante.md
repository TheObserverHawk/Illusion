---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Dérivée de fonctions d'une variable_
1. [[1.5.1 - Déf = Dérivée d'une fonction en ''a'']]

_Calculus : Théorème de la moyenne_
1. [[1.6.3 - Thm = Théorème de la moyenne]]
2.  [[1.6.3.4 - Prop = Si ''f'' décroissante, alors dériv de ''f'' sur ''I'' est négatif]]

_Calculus : Dérivée d'ordre supérieure_
1. [[1.7.1 - Prop = Classe de fonctions]]
2. [[1.7.3 - Déf = (Classe de fonctions dérivables)]]

_Math élémentaire : Inégalité_
1. [[1.2.4 - Fonction strictement décroissante]]


# Question 8 point b d'examen du janvier 2022
## Enoncé : Supposons que $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$. Pour chacune des affirmations suivantes, cochez la case adéquate selon que vous pensez qu’elle est vraie ou fausse. Justifiez vos réponses par une preuve ou un contre-exemple.
### Question : Si $∀x ∈ \mathbb{R}, ∂ f(x) < 0$, alors $f$ est strictement décroissante
_Réponse_ : Vrai 
Supposons que $f$ vérifie $∀x ∈ \mathbb{R}, ∂ f(x) < 0$ 
On doit établir $$\forall x_1,\ x_2 \in \operatorname{Dom}f,\ x_1 < x_2 \Rightarrow f(x_1) > f(x_2)$$
Soient $x_1,\ x_2 \in \operatorname{Dom}f = \mathbb{R}$ 
Supposons que $x_1 < x_2$ 
Montrons que $$f(x_1) > f(x_2)$$
Comme $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$, on a $f$ continue sur $[x_1; x_2]$ et dérivable sur $]x_1;x_2[$ 
On peut donc appliquer le théorème de la moyenne i.e. 

---
Soit $f : [a;b] \to \mathbb{R}$ 
1. une fonction continue sur $[a;b]$ et 
2. dérivable sur $]a;b[$ (avec $a < b$ ou $a >b$)

alors il existe $\xi \in\ ]a;b[$ tel que $$\begin{align*}f(b)-f(a) &=\partial f(\xi)(b-a) \\ \iff \frac{f(b)-f(a)}{b-a} &= \partial f(\xi)  \end{align*}$$

---
Celui-ci nous dit qu'il existe $\xi \in\ ]x_1;x_2[$ tel que $$f(x_2)-f(x_1) =\partial f(\xi)(x_2-x_1)$$
L'hypothèse que $∀x ∈ \mathbb{R}, ∂ f(x) < 0$ particularisée au cas $x = \xi$ nous donne $f(\xi) < 0$ 
Par ailleurs, vu que $x_1 < x_2$, on a $x_2 - x_1 > 0$ 
L'égalité $f(x_2)-f(x_1) =\partial f(\xi)(x_2-x_1)$ implique alors que $$f(x_2)-f(x_1) < 0$$ i.e. $$f(x_1) < f(x_2)$$
_Remarque_ :
1. La fonction $f(x) = \frac{1}{x}$ n'est pas un contre-exemple, même si sa dérivée vaut $-\frac{1}{x^2} < 0,\ \forall x \in \mathbb{R}$, car cette fonction ne respecte pas la condition $f ∈ \mathscr{C}^1 (\mathbb{R};\mathbb{R})$. En effet, cette fonction n'est pas définie sur tout $\mathbb{R}$ 

