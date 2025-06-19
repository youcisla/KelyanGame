## 🎮 Exercice : Crée un Jeu d'Évasion Labyrinthe avec IA

### 🧑‍💻 Partie 1 : Créer le Jeu Vidéo de Base

### 🎯 Objectif

Créer un jeu où un **personnage doit sortir d’un labyrinthe** généré aléatoirement.

---

### 🕹️ Description du jeu

* Un labyrinthe est généré dans une grille (ex. 10x10 cases).
* Le joueur commence en haut à gauche (0,0).
* La sortie est en bas à droite (9,9).
* Le joueur peut se déplacer avec les flèches directionnelles (haut, bas, gauche, droite).
* Chaque déplacement est limité aux chemins disponibles (pas à travers les murs).
* Le but est d’atteindre la sortie le plus vite possible (nombre de mouvements minimum).

---

### 🔧 Étapes à suivre

1. Créer une grille de 10x10 cases.
2. Générer un labyrinthe simple (utilise un algo comme DFS ou hardcode un pour débuter).
3. Placer un personnage au point de départ.
4. Contrôler le personnage avec les flèches du clavier.
5. Empêcher le joueur de traverser les murs.
6. Vérifier si le joueur est arrivé à la sortie.
7. Afficher le nombre de mouvements effectués.

---

### ✅ Résultat attendu

* Le joueur peut se déplacer dans le labyrinthe.
* Le jeu affiche le nombre de mouvements.
* Le jeu s’arrête ou affiche un message quand la sortie est atteinte.

---

## 🤖 Partie 2 : Ajouter une IA pour Résoudre le Labyrinthe

### 🎯 Objectif

Remplacer le joueur par une IA qui trouve le **plus court chemin** vers la sortie.

---

### 🧠 Étapes simples

1. Supprimer les commandes clavier (ou commenter).
2. Implémenter une fonction `solve_maze()` utilisant **l’algorithme A\*** ou **BFS**.
3. La fonction retourne une liste des mouvements à suivre.
4. Exécuter les mouvements un à un dans la boucle du jeu.
5. Afficher le chemin suivi et le nombre total de pas.

---

### ✅ Résultat attendu

* L’IA bouge seule dans le labyrinthe.
* Elle atteint la sortie automatiquement.
* Tu peux visualiser le chemin suivi par l’IA.

---

### 🎁 Bonus (facultatif)

* Génération aléatoire de labyrinthes.
* Ajouter des obstacles ou ennemis mobiles.
* Créer un mode **compétition IA vs humain** (le plus rapide gagne).
* Ajouter une animation de traînée sur le chemin parcouru par l'IA.

---

### 📦 Pré-requis techniques

* Python installé
* Pygame :

```bash
pip install pygame
```

---

### 🚀 Bonne chance !

Ce jeu t’apprend à :

* Manipuler des grilles et algorithmes de pathfinding,
* Visualiser les décisions d'une IA en action,
* Créer une interface simple mais stratégique.