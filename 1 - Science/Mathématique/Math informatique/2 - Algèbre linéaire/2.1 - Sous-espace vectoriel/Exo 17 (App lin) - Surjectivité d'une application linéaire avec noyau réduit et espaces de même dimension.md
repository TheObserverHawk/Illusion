---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Algèbre linéaire : SEV_
1. [[2.1.0 - Espace vectoriel]]
2. [[2.1.7 - Dimension (Algèbre linéaire)]]
3. [[2.1.15 - Application linéaire]]
4. [[2.1.16 - Noyau d'une application linéaire]]
5. [[2.1.17 - Image d'une application linéaire]]
6. [[2.1.19 - Théorème de Rang]]

# Exo 17
## Enoncé : Soient $E_1,E_2$ des espaces vectoriels, $f:E_1\to E_2$ une application linéaire. Prouvez que si $\operatorname{Ker}(L)=\{0_{E_1}\}$ et $\operatorname{dim}E_1=\operatorname{dim}E_2$, alors $\operatorname{Im}(f)=E_2$ 
Le théorème de rang : $$\operatorname{Dim}(E_1)=\operatorname{Dim(Ker}(f))+\operatorname{Dim(Im}(f))$$ On sait que $$\operatorname{Dim}(E_1)=\operatorname{Dim}(E_2)$$ et $$\operatorname{Dim(Ker}(f))=0$$ car $\operatorname{Ker}(f)=\{0\}$
Donc $$\operatorname{Dim}(E_2)=\operatorname{Dim(Im}(f))$$ ici, $\operatorname{Im}\subseteq E_2$ et $\operatorname{Dim}(E_2)=\operatorname{Dim(Im}(f))$ donc $$\operatorname{Im}(f)=E_2$$
\
_Remarque_ :
1. $$\operatorname{Dim}(A)=\operatorname{Dim}(B)$$ ne veut pas dire que $$A=B$$

**Conclusion** : 
Soient $A$ et $B$ deux ensembles si $A\subseteq B$ et $\operatorname{Dim}(A)=\operatorname{Dim}(B)$, alors $$A=B$$