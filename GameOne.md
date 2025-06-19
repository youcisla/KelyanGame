
# 🎮 Exercice : Crée un Jeu avec une IA Simple

## 🧑‍💻 Partie 1 : Créer le Jeu Vidéo de Base

### 🎯 Objectif
Créer un mini-jeu en Python avec **Pygame** où un joueur contrôle une plateforme pour attraper une balle qui tombe.

### 🕹️ Description du jeu

- Une **plateforme** est contrôlée par le joueur avec les touches gauche/droite.
- Une **balle** tombe depuis le haut de l’écran.
- Le but est d’attraper la balle avec la plateforme.
- À chaque balle attrapée : le score augmente.

### 🔧 Étapes à suivre

1. Créer une fenêtre de jeu de **400x600 pixels**.
2. Dessiner une **balle** (cercle) qui tombe verticalement.
3. Dessiner une **plateforme** (rectangle) qui bouge avec le clavier.
4. Vérifier les collisions entre la balle et la plateforme :
   - Si la balle est attrapée : score +1, balle remonte.
   - Sinon : balle remonte sans ajouter de score.
5. Afficher le **score** à l’écran.

### ✅ Résultat attendu

- Tu peux contrôler la plateforme avec les touches gauche/droite.
- Le jeu tourne en boucle.
- Le score augmente à chaque balle attrapée.

---

## 🤖 Partie 2 : Ajouter une IA pour Jouer Automatiquement

### 🎯 Objectif
Créer une IA simple qui contrôle automatiquement la plateforme pour attraper la balle sans utiliser le clavier.

### 🧠 Étapes simples

1. Supprimer les commandes clavier (ou les commenter).
2. Ajouter une **fonction IA** qui lit la position de la balle.
3. Utiliser une **règle simple** pour déplacer la plateforme :
```python
if ball_x > platform_x: move right
elif ball_x < platform_x: move left
```
4. Appeler cette logique IA dans la boucle principale du jeu à la place des touches.

### ✅ Résultat attendu

- La plateforme bouge toute seule pour essayer d’attraper la balle.
- Le score augmente si l’IA réussit bien.
- Tu peux observer le comportement de l’IA et l’améliorer.

### 🎁 Bonus (facultatif)
Tu peux aller plus loin en remplaçant les règles manuelles par une vraie IA avec apprentissage (ex : Q-Learning avec `stable-baselines3`).

---

## 📦 Pré-requis techniques

- Python installé
- Installer Pygame :
```bash
pip install pygame
```

## 🚀 Bonne chance !
Amuse-toi à créer ton jeu et à entraîner ta propre IA. C’est le début de ton aventure dans le monde du **Game Dev + IA** !
