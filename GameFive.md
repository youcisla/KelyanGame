## 🎮 Exercice : Crée un Bot Python pour **2048** avec IA

### 🧑‍💻 Partie 1 : Contrôler le Jeu en Ligne

### 🎯 Objectif

Créer un bot Python qui joue automatiquement au jeu [2048](https://play2048.co/) dans un navigateur web, en utilisant des stratégies simples au départ, puis une IA plus intelligente.

---

### 🕹️ Description du projet

* Le jeu se joue sur une **grille 4x4**.
* Tu dois **fusionner des cases de même valeur** (ex. 2+2 = 4) pour atteindre 2048.
* Les mouvements se font avec les **flèches directionnelles**.
* Le jeu se termine quand aucun mouvement n'est possible.

Ton bot devra :

* Lire l’état actuel de la grille
* Décider du meilleur mouvement (haut, bas, gauche, droite)
* Exécuter ce mouvement dans le navigateur

---

### 🔧 Étapes à suivre

1. Installer **Selenium** :

```bash
pip install selenium
```

2. Télécharger **ChromeDriver** ou **GeckoDriver** (selon ton navigateur), et place-le dans le même dossier que ton script.

3. Créer un script Python qui ouvre le jeu :

```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Chrome()
driver.get("https://play2048.co/")
game_area = driver.find_element("tag name", "body")
```

4. Simuler les flèches avec :

```python
game_area.send_keys(Keys.ARROW_UP)
```

5. Ajouter une boucle pour jouer automatiquement avec une logique simple :

```python
import random
moves = [Keys.ARROW_UP, Keys.ARROW_RIGHT, Keys.ARROW_LEFT, Keys.ARROW_DOWN]
while True:
    game_area.send_keys(random.choice(moves))
```

---

### ✅ Résultat attendu

* Le bot ouvre le jeu dans Chrome.
* Il joue automatiquement (même avec des mouvements aléatoires au départ).
* Tu peux observer sa progression et noter le score à la fin.

---

## 🤖 Partie 2 : Ajouter une IA pour Prendre les Meilleures Décisions

### 🎯 Objectif

Remplacer les mouvements aléatoires par une stratégie plus intelligente, avec une **fonction qui lit la grille** et choisit **le meilleur mouvement** à chaque tour.

---

### 🧠 Étapes IA

1. **Lire la grille** en extrayant les éléments HTML des cases :

```python
tiles = driver.find_elements("class name", "tile")
for tile in tiles:
    print(tile.get_attribute("class"))
```

2. **Créer une représentation 4x4 de la grille** dans Python.

3. Implémenter une **heuristique** simple (par exemple) :

   * Préférer les mouvements qui gardent les tuiles les plus hautes dans un coin
   * Éviter de bloquer la grille trop vite
   * Garder la ligne du bas remplie

4. Créer une fonction :

```python
def choose_best_move(board):
    # analyse le board et retourne Keys.ARROW_*
    return Keys.ARROW_LEFT  # par exemple
```

5. Remplacer les mouvements aléatoires par `choose_best_move(board)`.

---

### ✅ Résultat attendu

* Le bot joue seul de manière intelligente.
* Il atteint des scores supérieurs à la version aléatoire.
* Il peut relancer une partie automatiquement si la grille est pleine.

---

### 🎁 Bonus (facultatif)

* Implémenter un **algorithme Minimax avec élagage alpha-bêta**
* Enregistrer le **score final** dans un fichier ou base de données
* Ajouter un **mode compétition** : IA vs IA (différentes stratégies)
* Ajouter des **statistiques** après 100 parties (score moyen, max, taux de victoire)

---

### 📦 Pré-requis techniques

* Python 3.x
* Bibliothèque `selenium`
* Un navigateur installé (Chrome recommandé)
* ChromeDriver (ou équivalent)

---

### 🚀 Bonne chance !

Tu vas apprendre à :

* Contrôler un site web avec Python
* Lire des éléments d’interface avec Selenium
* Appliquer des algorithmes de prise de décision sur un jeu réel
