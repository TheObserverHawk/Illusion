---
tags:
  - Note_done
  - Informatique
source: UMons - Algorithme et programmation 2
---

Link :
_Algèbre linéaire : Matrice_
1. [[2.2.1.3 - Opérations sur les matrices]]

_Java : Base en Java_
1. [[1.6.1 - Branchement conditionnel (Java)]]
2. [[1.7.1 - Boucle (Java)]]

_Java : Classes & Objets_
1. [[2.6 - Modificateur ''static'' (Java)]]

_Java : Tableaux_
1. [[Java]]
2. [[3.7 - Concaténation de 2 tableaux (Java)]]
3. [[3.8 - Tableaux multi-dimensionnels (Java)]]
4. [[3.8.1 - Initialisation d'un tableau multi-dimensionnel (Java)]]

# Exercice – Multiplication de matrices 
1. Donner une méthode de classe multiplier permettant d’effectuer la multiplication d’une matrice par une autre. 
2. Les matrices sont modélisées par des tableaux à 2 dimensions de `double`

```java
public static double[][] multiply(double[][] a, double[][] b){
		if (a[0].length != b.length)
		// a[0] : nbre de colonnes de la matrice A
		// b : nbre de lignes de la matrice B
				return null;
		double[][]p = new double[a.length][b[0].length];
		for (int i=0; i < a.length; i++){
				for (int j = 0; j < b[0].length; j++){
						double s = 0;
						for (int k=0; k < b.length, k ++){
								s += a.[i][k] * b.[k][j];
						}
						p[i][j]=s;
				}
		}
}
```