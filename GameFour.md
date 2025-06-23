## 🎮 Exercice : Crée un Jeu de Type **Tic Tac Toe (XO)** avec une IA

### 🧑‍💻 Partie 1 : Créer le Jeu Vidéo de Base

### 🎯 Objectif

Développer une version graphique du célèbre jeu **Tic Tac Toe (XO)** en Python avec **Pygame**, permettant à deux joueurs de s’affronter tour par tour.

---

### 🕹️ Description du jeu

* Une **grille 3x3** s’affiche à l’écran.
* Deux joueurs (X et O) jouent à tour de rôle.
* Le joueur clique sur une case pour y placer son symbole.
* Le premier à aligner **3 symboles** (horizontalement, verticalement ou en diagonale) gagne.
* En cas de grille remplie sans gagnant → **égalité**.

---

### 🔧 Étapes à suivre

1. Créer une **fenêtre 600x600 pixels** avec Pygame.
2. Dessiner une **grille 3x3** avec des lignes.
3. Gérer les **clics de souris** pour détecter la case sélectionnée.
4. Afficher un **X ou O** selon le tour du joueur.
5. Vérifier **les conditions de victoire ou d’égalité** après chaque coup.
6. Afficher un **message de fin** (Victoire X, Victoire O, Égalité).
7. Ajouter un bouton **"Rejouer"** pour relancer la partie.

---

### ✅ Résultat attendu

* Les joueurs peuvent cliquer pour jouer.
* Le jeu annonce le gagnant ou une égalité.
* Possibilité de rejouer plusieurs parties facilement.

---

## 🤖 Partie 2 : Ajouter une IA comme adversaire

### 🎯 Objectif

Remplacer un des joueurs humains par une **IA qui joue intelligemment**.

---

### 🧠 Étapes IA

1. Choisir si **l’humain commence** ou **l’IA commence**.
2. Implémenter une IA utilisant l’algorithme **Minimax** avec élagage alpha-bêta.
3. À chaque tour IA, calculer le **meilleur coup possible**.
4. L’IA joue automatiquement son tour après le joueur.

---

### 🎁 Bonus

* Ajouter **un niveau de difficulté** :

  * **Facile** : coups aléatoires.
  * **Moyen** : coups semi-stratégiques.
  * **Difficile** : IA parfaite (Minimax complet).
* Afficher **l’arbre de décision** utilisé par l’IA (optionnel).
* Implémenter un **mode 2 joueurs** versus **IA** ou **local**.

---

### 📦 Pré-requis techniques

* Python
* Pygame :

```bash
pip install pygame
```

---

### 🚀 Bonne chance !

🧠 Amuse-toi à combiner **réflexion algorithmique** et **design interactif** pour créer un jeu de stratégie intemporel… et pourquoi pas battre ton IA ?