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
1. [[1.6.2 - Thm = Théorème de Rolle]]

# Question 1 d'examen du juin 2023
## Enoncé : Énoncez le théorème de Rolle. Interprétez-le géométriquement en veillant à faire un lien explicite et argumenté entre l’énoncé et les objets géométriques
Soit $f : [a, b] \to \mathbb{R}$ tel que
1. $f(a) = f(b)$
2. continue en $a$ et $b$
3. dérivable sur $]a,b[$ (avec $a < b$ ou $a > b$)

alors il existe un $\xi \in\ ]a,b[$ tel que $$f(\xi) = 0$$
**Interprétation géométrique** 
![[Pasted image 20231201100546.png]]
On a que 
1. 0 est la pente de la droite passante par les points $(a;f(a))$ et $(b;f(b))$ 
2. $\partial f(\xi)$ est la pente de la tangente au graphe de $f$ au point $(\xi;f(\xi))$ 

Et donc dire que $$\partial f(\xi)=0$$ reviens à dire que la pente de la tangente au graphe de $f$ au point $(\xi;f(\xi))$ est égale à la pente de la droite passante par $(a;f(a))$ et $(b;f(b))$. Donc que ces 2 droites ont une pente qui vaut 0 et sont donc parallèles entre elles et horizontales.