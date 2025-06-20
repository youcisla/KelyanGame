## 🎮 Exercice : Crée un Jeu de Type **Pac-Man** avec IA et Labyrinthe

### 🧑‍💻 Partie 1 : Créer le Jeu Vidéo de Base

### 🎯 Objectif

Fusionner les deux jeux précédents (plateforme + labyrinthe) pour créer un **jeu dans un labyrinthe** où le joueur contrôle un personnage qui doit **manger des points** tout en évitant des ennemis.

---

### 🕹️ Description du jeu

* Une **grille 10x10** forme le labyrinthe.
* Le joueur contrôle un **personnage rond** (Pac-Man style).
* Des **points** sont disposés dans les chemins du labyrinthe.
* Des **ennemis** (fantômes) se déplacent automatiquement dans le labyrinthe.
* Le joueur peut utiliser les **touches directionnelles** pour se déplacer.
* Le but est de **manger tous les points sans se faire attraper**.

---

### 🔧 Étapes à suivre

1. Générer un **labyrinthe simple** (avec DFS ou hardcodé).
2. Afficher les **points à collecter** sur les chemins.
3. Ajouter un **personnage contrôlable** (Pac-Man).
4. Implémenter des **ennemis qui bougent automatiquement**.
5. Gérer les **collisions** :

   * Pac-Man mange un point : +1 au score.
   * Pac-Man touche un ennemi : game over.
6. Afficher le **score** et l’état de la partie (en cours / gagné / perdu).

---

### ✅ Résultat attendu

* Le joueur peut explorer le labyrinthe.
* Le score augmente à chaque point collecté.
* Le jeu se termine quand tous les points sont mangés ou si un ennemi touche le joueur.

---

## 🤖 Partie 2 : Ajouter une IA Jouant à la Place du Joueur

### 🎯 Objectif

Créer une IA qui **joue au jeu Pac-Man automatiquement**, en collectant les points tout en **évitant les ennemis**.

---

### 🧠 Étapes simples

1. Remplacer les touches directionnelles par une **fonction IA**.
2. Utiliser un algorithme comme **A\*** ou **BFS** pour :

   * Trouver le **point le plus proche** à manger.
   * Éviter les positions des ennemis.
3. Faire avancer le personnage pas à pas selon ce plan.
4. Afficher le **chemin suivi par l’IA**.

---

### 🎁 Bonus

* Créer une IA pour les **fantômes** qui poursuivent le joueur (stratégie simple ou Q-Learning).
* Ajouter des **niveaux de difficulté**.
* Implémenter des **bonus spéciaux** (ex: invincibilité temporaire).
* Mode **1v1 : IA contre humain** pour voir qui nettoie le labyrinthe plus vite.

---

### 📦 Pré-requis techniques

* Python
* Pygame :

```bash
pip install pygame
```

---

### 🚀 Bonne chance !

Amuse-toi à mélanger **réflexion IA, gameplay et level design** pour donner vie à ton propre clone de **Pac-Man** revisité !
