## 🎮 Exercice : Crée un Bot Python pour **le jeu Dino** avec IA (Edge Compatible, Sans Installation Supplémentaire)

### 🧑‍💻 Partie 1 : Contrôler le Jeu Dino via Microsoft Edge

### 🎯 Objectif

Créer un bot Python qui joue automatiquement au jeu [Dino](https://chromedino.com/) dans **Microsoft Edge**, sans installer de driver manuellement, en commençant par une simple stratégie réflexe.

---

### 🕹️ Description du projet

* Le jeu Dino se joue en **appuyant sur la barre d’espace** pour sauter.
* Le but est d’**éviter les obstacles** (cactus, oiseaux).
* Le jeu se relance automatiquement si tu appuies à nouveau.

---

### 🔧 Étapes à suivre

1. Installer la bibliothèque Selenium :

```bash
pip install selenium
```

2. Utiliser Microsoft Edge (aucun téléchargement requis) :

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys

# Lancement de Microsoft Edge sans EdgeOptions
driver = webdriver.Edge()
driver.get("https://chromedino.com/")
```

3. Cliquer sur le canvas du jeu (zone du dino), puis sauter :

```python
import time

canvas = driver.find_element(By.TAG_NAME, "body")
canvas.send_keys(Keys.SPACE)  # Démarre le jeu
time.sleep(1)
```

4. Boucle de jeu automatique (stratégie simple → sauts aléatoires) :

```python
import random

while True:
    time.sleep(random.uniform(0.8, 1.5))  # délai entre sauts
    canvas.send_keys(Keys.SPACE)  # saute pour éviter obstacles
```

---

### ✅ Résultat attendu

* Le dino commence à courir automatiquement.
* Il saute tout seul (même si c’est aléatoire au début).
* Tu peux ensuite améliorer sa précision en ajoutant une IA de détection d’obstacle.

---

## 🤖 Partie 2 : Ajouter une IA basique

### 🎯 Objectif

Créer une **IA visuelle** qui détecte les obstacles et saute au bon moment.

---

### 🧠 Étapes IA

1. Utiliser **PyAutoGUI** ou **Pillow + pywin32** pour faire des captures d’écran :

   * Détecter un pixel ou une forme devant le dino.
   * Sauter seulement si un obstacle est détecté.

2. Exemple (optionnel, si `pyautogui` est autorisé) :

```python
import pyautogui

def detect_obstacle():
    pixel = pyautogui.pixel(500, 400)
    if pixel[0] < 100:  # détecte un obstacle foncé
        return True
    return False
```

3. Remplacer la boucle de saut aléatoire :

```python
while True:
    if detect_obstacle():
        canvas.send_keys(Keys.SPACE)
```

> ⚠️ Tu peux aussi t’amuser à tester des IA plus avancées (réseaux de neurones + vision).

---

### 📦 Pré-requis techniques

* Python 3.x
* `selenium`
* Navigateur **Microsoft Edge** installé (aucun driver à télécharger)
* (Facultatif) `pyautogui` ou `opencv-python` si tu veux une IA visuelle

---

### 🚀 Bonne chance !

Tu apprendras à :

* Automatiser un jeu jouable sur navigateur sans rien installer
* Simuler des touches pour interagir avec le jeu
* Ajouter une détection intelligente pour améliorer les performances du bot
