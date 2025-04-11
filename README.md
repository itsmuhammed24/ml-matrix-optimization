# Optimisation en apprentissage automatique

Ce projet explore plusieurs techniques d’optimisation fondamentales pour l’apprentissage automatique, à travers la régression linéaire et la factorisation matricielle (rang 1, rang faible, régularisée). L’objectif est d’analyser les effets de la surparamétrisation, de la régularisation et des méthodes de descente (batch vs stochastique) sur la qualité des solutions obtenues.

> Projet réalisé dans le cadre du Master IASD , encadré par [Clément Royer](https://www.lamsade.dauphine.fr/~croyer/).

## Contenu

### Régression linéaire
- Formulation classique :  
  $$
  \min_{w \in \mathbb{R}} \frac{1}{2n} \|wx - y\|^2
  $$
- Formulation surparamétrée (matricielle) :  
  $$
  \min_{W \in \mathbb{R}^{n \times n}} \frac{1}{2n} \|Wx - y\|^2
  $$
- Comparaison entre solution analytique et optimisation par descente de gradient (GD).

---

### Factorisation matricielle
- Approximation de rang 1 :
  $$
  \min_{u \in \mathbb{R}^{n_1}, v \in \mathbb{R}^{n_2}} \frac{1}{2n} \|uv^\top - X\|_F^2
  $$
- Descente de gradient classique (GD) vs stochastique (SGD).
- Étude de l’effet de la taille de batch sur la convergence.

---

### Factorisation matricielle de rang \( r \)
- Approche généralisée :
  $$
  \min_{U \in \mathbb{R}^{n_1 \times r}, V \in \mathbb{R}^{n_2 \times r}} \frac{1}{2n} \|UV^\top - X\|_F^2
  $$
- Étude comparative GD / SGD pour différentes structures de rang.

---

### Factorisation régularisée
- Formulation régularisée :
  $$
  \min_{U, V} \frac{1}{2n} \|UV^\top - X\|_F^2 + \frac{\lambda}{2} \|U\|_F^2 + \frac{\lambda}{2} \|V\|_F^2
  $$
- Étude de l’impact du paramètre de régularisation \( \lambda \) sur le rang effectif.
- Comparaison des dynamiques d’optimisation GD vs SGD en présence de bruit.
