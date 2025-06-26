**Titre : Exercice : Créer un bot ou un jeu pour Démineur**

---

### Partie 1 : Créer ou automatiser le jeu de base

**Objectif :**
Créer un petit jeu interactif en Python où le joueur clique sur une grille pour révéler des cases, en évitant les mines cachées.

---

**Description du jeu :**
Le **Démineur** est un jeu de stratégie où le joueur doit cliquer sur des cases d’une grille sans tomber sur une mine.
Chaque case vide affiche un chiffre qui indique le nombre de mines dans les cases voisines.
Le joueur gagne s’il découvre toutes les cases sans mines. Il perd dès qu’il clique sur une case contenant une mine.

---

**Étapes à suivre :**

1. Créer une **grille carrée (ex : 8x8)** avec des boutons ou des cases cliquables.
2. **Placer aléatoirement des mines** dans certaines cases.
3. Lorsqu’un joueur clique sur une case :

   * Si c’est une **mine** → le jeu s’arrête (perdu).
   * Si ce n’est pas une mine → afficher le **nombre de mines autour**.
4. Si le joueur clique sur une case avec **zéro mines autour**, révéler **automatiquement les voisines**.
5. Afficher un message **"Gagné"** si toutes les cases sûres sont découvertes.

---

**Résultat attendu :**
Le joueur peut cliquer pour explorer la grille, éviter les mines, et le jeu se termine avec une victoire ou une défaite selon ses choix.

---

### Partie 2 : Ajouter une logique intelligente simple

**Objectif :**
Créer un **bot** qui joue automatiquement au démineur à ta place en suivant une logique basique.

---

**Étapes IA :**

1. Créer une fonction qui choisit **aléatoirement une case non cliquée** au début.
2. Une fois quelques cases révélées :

   * Si une case a un **chiffre** (ex : 1), et qu’elle a **exactement 1 case cachée voisine**, le bot marque cette case comme **mine**.
   * S’il reste des cases sûres (selon la logique) → les cliquer automatiquement.
3. Répéter ce raisonnement tant qu’il y a des cases sûres.
4. Si aucune certitude → choisir une case au hasard parmi les non explorées.

---

**Résultat attendu :**
Le bot commence à jouer, clique automatiquement, marque les mines, et essaie de gagner sans intervention humaine.

---

### Bonus :

* Ajouter un **chrono** pour mesurer le temps du joueur ou du bot.
* Proposer différents **niveaux de difficulté** (taille de la grille, nombre de mines).
* Ajouter une **fonction de sauvegarde et de reprise**.
* Implémenter un **algorithme plus avancé** pour rendre l’IA plus performante.

---

### Pré-requis techniques :

* Python installé
* Bibliothèque **tkinter** (fournie avec Python) ou **Pygame** si tu préfères une interface graphique personnalisée.

---

### Conclusion :

Ce projet te permettra de mieux comprendre la logique conditionnelle, les boucles, les tableaux et la manipulation de l’interface graphique. C’est un excellent exercice pour développer ta réflexion algorithmique, avec ou sans IA.
Prends ton temps et surtout… **ne clique pas sur une mine** ! 💥
