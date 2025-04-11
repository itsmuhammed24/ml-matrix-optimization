# Optimisation en apprentissage automatique

Ce projet explore plusieurs techniques d’optimisation fondamentales pour l’apprentissage automatique, à travers la régression linéaire et la factorisation matricielle (rang 1, rang faible, régularisée). L’objectif est d’analyser les effets de la surparamétrisation, de la régularisation et des méthodes de descente (batch vs stochastique) sur la qualité des solutions obtenues.

> Projet réalisé dans le cadre du Master IASD , encadré par [Clément Royer](https://www.lamsade.dauphine.fr/~croyer/).

## Contenu

- **Régression linéaire :**
  - Formulation classique vs surparamétrée (scalaire vs matrice).
  - Comparaison entre solution analytique et optimisation par descente de gradient.

- **Factorisation matricielle :**
  - Approximation de rang 1 via descente de gradient (GD) et descente stochastique (SGD).
  - Étude de l’effet de la taille de batch sur la convergence.

- **Factorisation matricielle de rang \( r \) :**
  - Implémentation de la factorisation \( UV^\top \) avec rang variable.
  - Comparaison GD/SGD sur des matrices de rang contrôlé.

- **Factorisation régularisée :**
  - Ajout de pénalités \( L_2 \) sur les matrices \( U \) et \( V \).
  - Étude de l’impact du paramètre de régularisation \( \lambda \) sur le rang effectif.


