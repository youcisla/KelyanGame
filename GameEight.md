**Titre : Exercice : Créer un bot ou un jeu pour Sudoku simplifié**

---

**Partie 1 : Créer ou automatiser le jeu de base**

**Objectif :**
Apprendre à créer une version simplifiée du jeu Sudoku en Python, avec une grille 4x4 (au lieu de 9x9), en utilisant des listes, des boucles, et des conditions simples.

**Description du jeu :**
Le Sudoku est un jeu de logique où le but est de remplir une grille avec des chiffres sans répéter les mêmes chiffres sur une ligne, une colonne, ou une région (dans notre version simplifiée, des carrés 2x2).
Dans ce projet, nous allons construire une grille 4x4 où chaque ligne, colonne, et carré 2x2 doit contenir les chiffres de 1 à 4 sans répétition.

**Étapes à suivre :**

1. Créer une grille 4x4 vide (liste de listes) et y insérer quelques chiffres prédéfinis.
2. Afficher la grille de façon lisible dans le terminal.
3. Permettre à l’utilisateur de remplir une case en choisissant la ligne, la colonne et le chiffre.
4. Vérifier si la position choisie est valide (case vide).
5. Répéter jusqu’à ce que la grille soit remplie.

**Résultat attendu :**
À la fin, l’utilisateur peut compléter un Sudoku 4x4 avec des entrées valides. Le programme affiche la grille après chaque coup et s’assure que l’utilisateur remplit uniquement les cases vides.

---

**Partie 2 : Ajouter une logique intelligente simple**

**Objectif :**
Permettre au programme de vérifier si les règles du Sudoku sont respectées à chaque insertion, et refuser une entrée incorrecte.

**Étapes IA :**

1. Ajouter une fonction pour vérifier si un chiffre est déjà présent dans la ligne.
2. Ajouter une fonction pour vérifier la colonne.
3. Ajouter une fonction pour vérifier le carré 2x2 correspondant.
4. Lorsqu’un joueur propose un chiffre, utiliser ces fonctions pour valider ou refuser l’entrée.
5. Informer l’utilisateur si l’entrée est invalide, avec un message clair.

**Résultat attendu :**
Le programme devient plus intelligent : il empêche l’utilisateur de tricher en insérant un chiffre qui viole les règles du Sudoku. L’expérience est plus interactive et éducative.

---

**Bonus :**

* Ajouter un minuteur pour chronométrer la partie.
* Créer plusieurs grilles de départ (aléatoires ou préprogrammées).
* Ajouter une option "solution" pour afficher la grille complète.
* Utiliser Tkinter pour créer une interface graphique simple.

---

**Pré-requis techniques :**

* Python 3
* Aucune bibliothèque externe n’est nécessaire pour la version en terminal.
* Optionnel : `tkinter` pour une interface graphique.

---

**Conclusion :**
Félicitations ! En réalisant ce projet, tu as non seulement compris les bases de la programmation en Python (listes, boucles, conditions), mais tu as aussi recréé un jeu de logique universellement reconnu. Garde l’élan et amuse-toi à améliorer ton programme ! Chaque ligne de code que tu ajoutes t’approche un peu plus du niveau expert.
