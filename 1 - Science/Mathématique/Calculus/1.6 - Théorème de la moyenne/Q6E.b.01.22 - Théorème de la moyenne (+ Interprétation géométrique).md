---
tags:
  - Note_done
  - Math
source: UMons - Calculus Examen
---

Link :
_Calculus : Continuité d'une fonction_
1. [[../1.4 - Continuité d'une limite de fonction/1.4.1 - Déf = Continuité d'une fonction|1.4.1 - Déf = Continuité d'une fonction]]

_Calculus : Dérivée de fonctions d'une variable_
1. [[../1.5 - Dérivée des fonctions d'une variable/1.5.1 - Déf = Dérivée d'une fonction en ''a''|1.5.1 - Déf = Dérivée d'une fonction en ''a'']]

_Calculus : Théorème de la moyenne_
1. [[1.6.3 - Thm = Théorème de la moyenne]] 

# Question 1 d'examen du janvier 2023
## Enoncé : Énoncez le théorème de la moyenne. Interprétez-le géométriquement en veillant à faire un lien explicite et argumenté entre l’énoncé et les objets géométriques.
Soit $f:[a,b]\to\mathbb{R}$,
- une fonction continue sur $[a,b]$ 
- dérivable sur $]a,b[$ 

alors il existe un $\xi\in\ ]a,b[$ tel que $$f(b)-f(a)=\partial f(\xi).(b-a)\quad\iff\quad\frac{f(b)-f(a)}{b-a}=\partial f(\xi)$$ **Interprétation géométrique** : ![[Pasted image 20231201103158.png]]
On remarque que 
- $$\partial f(\xi)$$ est une pente de la tangente passante par le point $(\xi,f(\xi))$ 
- $$\frac{f(b)-f(a)}{b-a}$$ est une pente de la droite passante par les points $(a,f(a))$ et $(b, f(b))$ 

Et donc dire que $$\frac{f(b)-f(a)}{b-a}=\partial f(\xi)$$ revient à dire que les 2 pentes sont parallèles