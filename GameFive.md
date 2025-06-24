## 🎮 Exercice : Contrôle Minecraft avec Python (API + IA)

### 🧑‍💻 Partie 1 : Contrôler Minecraft avec Python

### 🎯 Objectif

Apprendre à **contrôler Minecraft depuis un script Python**, comme placer des blocs, bouger ton personnage, ou déclencher des événements automatiquement.

---

### 🕹️ Description du projet

Tu vas utiliser une version spéciale de Minecraft (**Minecraft Java Edition + Mod RaspberryJuice** ou **Minecraft Pi**) pour pouvoir contrôler le jeu via Python.

Exemples de ce que tu peux faire :

* Placer automatiquement des blocs.
* Faire bouger ton joueur.
* Créer des structures (ex : une maison).
* Réagir à ce que le joueur fait (ex : afficher un message quand il saute).

---

### 🔧 Étapes à suivre

#### 🧰 Étape 1 : Préparer Minecraft

1. Télécharge **Minecraft Java Edition**.
2. Installe **Forge** ou **Spigot Server** avec le **plugin RaspberryJuice**.
3. Lance le jeu en multijoueur local sur ce serveur modifié.

#### 🐍 Étape 2 : Installer l’API Python

Installe la bibliothèque `mcpi` :

```bash
pip install minecraftstuff
```

Tu peux aussi utiliser `mcpi` depuis [ce dépôt GitHub non-officiel](https://github.com/martinohanlon/mcpi).

#### 📜 Étape 3 : Ton premier script

Voici un exemple de code qui connecte Python à Minecraft et place un bloc :

```python
from mcpi.minecraft import Minecraft
mc = Minecraft.create()

# Place un bloc de pierre sous le joueur
x, y, z = mc.player.getTilePos()
mc.setBlock(x, y - 1, z, 1)  # ID 1 = Pierre
```

---

### ✅ Résultat attendu

* Ton script Python **modifie le monde Minecraft en direct**.
* Tu peux interagir avec l’environnement, créer des structures ou lire les actions du joueur.

---

## 🤖 Partie 2 : Ajouter une IA pour Interagir avec le Monde

### 🎯 Objectif

Utiliser une **IA ou logique simple** pour que ton personnage agisse tout seul :

* Explorer automatiquement.
* Construire des murs ou tours.
* Réagir quand un joueur saute, avance ou tape.

---

### 🧠 Étapes IA

1. Ajoute une boucle qui **lit en permanence la position du joueur**.
2. Ajoute des réactions conditionnelles :

   ```python
   pos = mc.player.getTilePos()
   if pos.y > 50:
       mc.postToChat("Tu es très haut !")
   ```
3. Implémente des **actions automatiques** :

   * L’IA construit une maison.
   * L’IA suit le joueur (pathfinding simple).
   * L’IA place des blocs selon un motif.

---

### 🎁 Bonus

* Crée un **bot constructeur** (mur, escalier, tour).
* Crée un **mini-jeu dans Minecraft** (labyrinthe, challenge, etc.).
* Utilise de l’**IA réelle** avec un modèle entraîné (ex : Reinforcement Learning avec `Gym-Minecraft`).

---

### 📦 Pré-requis techniques

* Minecraft Java Edition installé
* Serveur avec le plugin RaspberryJuice (ou Minecraft Pi pour les tests simples)
* Python 3.x
* Module `minecraftstuff` ou `mcpi`

---

### 🚀 Bonne chance !

Tu viens d’entrer dans le monde du **modding Minecraft avec Python** 🤖. C’est parfait pour apprendre la **programmation interactive**, automatiser des tâches, ou même t'amuser à créer ton assistant Minecraft personnel 🧱.