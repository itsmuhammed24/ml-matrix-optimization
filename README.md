# Optimisation en apprentissage automatique

Ce projet explore plusieurs techniques d’optimisation fondamentales pour l’apprentissage automatique, à travers la régression linéaire et la factorisation matricielle (rang 1, rang faible, régularisée). L’objectif est d’analyser les effets de la surparamétrisation, de la régularisation et des méthodes de descente (batch vs stochastique) sur la qualité des solutions obtenues.

> Projet réalisé dans le cadre du Master IASD , encadré par [Clément Royer](https://www.lamsade.dauphine.fr/~croyer/).

## Contenu

### Régression linéaire
- **Formulation classique** :  
  Minimiser la fonction  
  `f(w) = (1 / 2n) * ||w * x - y||^2`  
  où `w` est un scalaire réel.

- **Formulation surparamétrée (matricielle)** :  
  Minimiser la fonction  
  `f(W) = (1 / 2n) * ||W * x - y||^2`  
  où `W` est une matrice carrée de taille `n x n`.

- Comparaison entre solution analytique et optimisation par descente de gradient (GD).

---

### Factorisation matricielle (rang 1)
- Approximation d’une matrice `X` par un produit de vecteurs :  
  `X ≈ u * v^T`

- Objectif :  
  Minimiser  
  `f(u, v) = (1 / 2n) * ||u * v^T - X||_F^2`  
  où `||.||_F` désigne la norme de Frobenius.

- Méthodes utilisées :  
  - Descente de gradient (GD)  
  - Descente de gradient stochastique (SGD)

- Étude de l’effet de la taille de batch sur la convergence.

---

### Factorisation matricielle de rang r
- Généralisation avec matrices `U` et `V` :
  `X ≈ U * V^T` avec `U` de taille `(n1 x r)` et `V` de taille `(n2 x r)`

- Objectif :  
  Minimiser  
  `f(U, V) = (1 / 2n) * ||U * V^T - X||_F^2`

- Comparaison GD / SGD pour différentes valeurs de `r` et différents rangs de `X`.

---

### Factorisation régularisée
- Ajout d'une pénalité L2 sur les matrices `U` et `V`.

- Formulation :  
  Minimiser  
  `f(U, V) = (1 / 2n) * ||U * V^T - X||_F^2 + (λ/2) * ||U||_F^2 + (λ/2) * ||V||_F^2`

- Étude de l’impact du paramètre de régularisation `λ` sur le rang effectif.

- Comparaison GD / SGD en présence de bruit.