---
tags:
  - Note_done
  - Math
source: UMons - Math pour l'informatique
---

Link :
_Math discrète : Relation binaire_
1. [[1.2.3 - Relation réflexive]]
2. [[1.2.8 - Composition de relations]]
3. [[1.2.9 - Composition d'une relation avec elle-même]]

# Prouvez que si $R$ est une relation symétrique alors $R^n\ (n\ge 1)$ est également symétrique
Supposons $R$ est symétrique, montrons que $\forall n\ge 1,\ R^n$ est symétrique 
Soit $n\in\mathbb{N}$ tel que $n\ge 1$ 
##### Cas de base : $n=1$ 
Montrons que $R^1$ est symétrique
On a que $R^1=R$ et par hypothèse, $R$ est symétrique
##### Cas général : $\forall k\in\mathbb{N}^{\ge 1},\ P(k)\Rightarrow P(k+1)$ 
Soit $k\in\mathbb{N}^{\ge 1}$ 
Supposons que $P(k)=R^k$ est symétrique
Montrons que $R^{k+1}$ est symétrique
On a $$R^{k+1}=R^k\circ R=\{(a,c)\in A\times A|\ \exists b\in A,\ (a,b)\in R\wedge (b,c)\in R^k\}$$
Montrons que $$\forall a,b\in A, (a,b)\in R^{k+1}\Rightarrow (b,a)\in R^{k+1}$$
Soient $a,b\in A$ 
Supposons que $(a,b)\in R^{k+1}$ i.e. $$\exists c\in A,\ (a,c)\in R\wedge (c,b)\in R^k$$
Montrons que $(b,a)\in R^{k+1}$ i.e. montrons que $$d\in A, (b,d)\in R^k\wedge (d,a)\in R$$
Prenons $d=c\in A$
On a $$(b,d)=(b,c)\in R^k$$
Comme $(c,b)\in R^k$, par symétrie $(b,c)\in R^k$ et $(d,a)\in R$ car $(c,a)\in R$ 
Vu que $(a,c)\in R$ et $R$ symétrique par hypothèse. 
D'où $R^{k+1}$ est symétrique