---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Limite de fonctions_
1. [[1.3.1 - Déf = Convergence de limite de fonctions]]
2. [[1.3.3 - Déf = Adhérence]]


# Question 4 d'examen du janvier 2023
## Enoncé : 
### a) Soient $E ⊆ \mathbb{R}, f : \mathbb{R} → \mathbb{R}$ une fonction, $a ∈ \operatorname{adh}E$ et $b ∈ \mathbb{R}$. Définissez $\underset{\overset{x\to a}{x\in E}}{\lim}f(x)=b$ 
$$\forall (x_n)\subseteq\operatorname{Dom}f\cap E,\quad x_n\to a\quad\Rightarrow\quad f(x_n)\to f(x_n)=b$$
### b) Soient $A,B ⊆ \mathbb{R}, f : \mathbb{R} → \mathbb{R}$ une fonction, $a ∈ \operatorname{adh}B$ et $b ∈ \mathbb{R}$. Supposons que $B ⊆ A$.
#### i) Montrez que $a\in\operatorname{adh}A$
Comme on sait que $a\in\operatorname{adh}B$ et que $B\subseteq A$, on a que $$\exists (x_n)\subseteq B\subseteq A,\quad x_n\to a$$ et donc $$\exists(x_n)\subseteq A,\quad x_n\to a$$
#### ii) En utilisant la définition donnée au point (a), montrez que si $\underset{\overset{x\to a}{x\in A}}{\lim}f(x) = b$ alors on a $\underset{\overset{x\to a}{x\in B}}{\lim}f(x) = b$
Supposons que $$\underset{\overset{x\to a}{x\in A}}{\lim}f(x) = b$$ i.e. $$\forall (x_n)\subseteq\operatorname{Dom}f\cap A,\quad (x_n)\to a\quad\Rightarrow\quad f(x_n)\to f(a)=b$$ Montrons que $$\underset{\overset{x\to a}{x\in B}}{\lim}f(x) = b$$ i.e. $$\forall (x_n)\subseteq\operatorname{Dom}f\cap B,\quad (x_n)\to a\quad\Rightarrow\quad f(x_n)\to f(a)=b$$ Soit $(x_n)\subseteq B\cap\operatorname{Dom}f$, on a que $$(x_n)\subseteq A\cap\operatorname{Dom}f$$ car $(x_n)\subseteq B\subseteq A,\quad x_n\to a$ et $(x_n)\subseteq\operatorname{Dom} f$, donc on a $$(x_n)\subseteq A\cap\operatorname{Dom}f$$, de plus on a que par hypothèse $$\forall (x_n)\subseteq\operatorname{Dom}f\cap A,\quad (x_n)\to a\quad\Rightarrow\quad f(x_n)\to f(a)=b$$
#### iii) La réciproque de cette implication est-elle vraie ? Justifiez votre réponse.
Non, elle ne l'est pas. Prenons le contre-exemple suivant : $$f(x)=\begin{cases}x-1\quad\text{ si } n\ge 2\\x^2\quad\text{ si } x< 2\end{cases}$$
- $$\underset{\overset{x\to 2}{x<2}}{\lim}f(x)=\underset{\overset{x\to2}{x\in\ ]-\infty,2[}}{\lim}x^2=4$$
- $$\underset{\overset{x\to 2}{x\le 2}}{\lim}f(x)=\underset{\overset{x\to2}{x\in\ ]-\infty,2]}}{\lim}x-1=1$$ Regardons cette limite quand $x\in\ ]-\infty,2[$ et quand $x\in\{2\}$ :
	- $$\underset{\overset{x\to2}{x\in\ ]-\infty,2[}}{\lim}f(x)=4 \quad\text{ déjà calculé}$$
	-  $$\underset{\overset{x\to2}{x=2}}{\lim}f(x)=\underset{\overset{x\to2}{x=2}}{\lim}x-1=1$$

On a que $\underset{\overset{x\to 2}{x<2}}{\lim}f(x)$ existe et que $\underset{\overset{x\to 2}{x\le 2}}{\lim}f(x)$ n’existe pas car pas d’unicité, alors que pourtant $$]-\infty,2[\ \subseteq\ ]-\infty,2]$$