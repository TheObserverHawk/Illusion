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

# Prouvez que si $R$ est une relation réflexive alors $R^n\ (n\ge 1)$ est également réflexive
Supposons que $R$ est réflexive, montrons que $\forall n\ge 1,\ R^{n}$ réflexive
Soit $n\in\mathbb{N}$ tel que $n\ge 1$ 
##### Cas de base : $n=1$ 
Montrons que $R^1$ est réflexive
On a que $R^1=R$ et par hypothèse, $R$ est réflexive
##### Cas général : $\forall k\in\mathbb{N}^{\ge 1},\ P(k)\Rightarrow P(k+1)$ 
Soit $k\in\mathbb{N}^{\ge 1}$ 
Supposons $R^k$ est réflexive, montrons que $R^{k+1}$ est réflexive
On a $$R^{k+1}=R^{k}\circ R=\{(a,c)\in A\times A|\ \exists b\in A, (a,b)\in R\wedge(b,c)\in R^k\}$$
Montrons que $\forall a\in A,(a,a)\in R^{k+1}$ 
Soit $a\in A$ 
On sait que $R$ et $R^{k}$ sont réflexives, donc $(a,a)\in R$ et $(a,a)\in R^k$ 
pour $b= a\in A$, on a bien $(a,a)\in R^{k+1}$, donc $R^{k+1}$ est réflexive 
D'où $\forall n\ge 1, R^{k+1}$ est réflexive.