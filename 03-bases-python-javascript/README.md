# Bases de Python et JavaScript 🚀

L'objectif de cette étape était de configurer mon environnement de développement Python sur Ubuntu en installant les outils et bibliothèques nécessaires.

## Python 🐍

### Étapes de configuration 🛠️

1. **Installation de Visual Studio Code** 📥
   - J'ai téléchargé la version Ubuntu compatible ARM de Visual Studio Code depuis [le site officiel](https://code.visualstudio.com/download#).
   - J'ai ouvert le terminal et navigué vers le répertoire contenant le fichier d’installation de Visual Studio Code.
   - J'ai installé Visual Studio Code en exécutant la commande suivante :
     ```bash
     sudo apt install ./nom_du_fichier_d’installation.deb
     ```

2. **Configuration de Visual Studio Code** ⚙️
   - J'ai lancé Visual Studio Code et installé l'extension Python pour bénéficier de fonctionnalités comme la coloration syntaxique et l'autocomplétion.

3. **Installation de Git** 🛠️
   - J'ai installé Git en exécutant la commande suivante dans le terminal :
     ```bash
     sudo apt-get install git
     ```
   - J'ai vérifié l'installation de Git avec la commande :
     ```bash
     git --version
     ```

4. **Installation de Python** 🐍
   - J'ai installé Python en exécutant la commande suivante dans le terminal :
     ```bash
     sudo apt install python3
     ```
   - J'ai vérifié l'installation de Python avec la commande :
     ```bash
     python3 --version
     ```

## Revoyez les concepts fondamentaux de Python

Cette section couvre les concepts de base de Python, incluant la syntaxe, les structures de données, les boucles, les fonctions, et la gestion des exceptions.

### Exécution d'un programme Python

- Pour exécuter un programme Python, j'ai utilisé la commande suivante :
  ```bash
  python3 nom_du_fichier.py
  ```

### Variables et types de données

- **Déclaration de variables** :
  ```python
  nom_utilisateur = "iliass"  # type str
  age_utilisateur = 32        # type int
  taille_utilisateur = 1.86   # type float
  utilisateur_est_majeur = True  # type bool
  ```

- **Vérification du type de variable** :
  ```python
  type(nom_utilisateur)  # Retourne le type de la variable
  ```

### Listes et tuples

- **Listes** (modifiables) :
  ```python
  plateformes_sociales_liste = ["Facebook", "Instagram", "Snapchat", "Twitter"]
  ```

- **Tuples** (immuables) :
  ```python
  plateformes_sociales_tuple = ("Facebook", "Instagram", "TikTok", "Twitter")
  ```

- **Méthodes de liste courantes** :
  - `extend()`, `insert()`, `pop()`, `index()`, `count()`, `reverse()`

### Dictionnaires

- **Déclaration d'un dictionnaire** :
  ```python
  infos_utilisateur = {
      "prenom": "iliass",
      "age": 32,
  }
  ```

- **Méthodes de dictionnaire courantes** :
  - `keys()`, `values()`, `items()`, `get(clé)`, `pop(clé)`, `clear()`

### Conditions

J'ai utilisé les conditions en Python pour exécuter du code en fonction de certaines conditions. Voici un exemple utilisant une condition `if` pour vérifier si un utilisateur est majeur :

```python
nom_utilisateur = 'iliass'
age_utilisateur = 20

if age_utilisateur >= 18:
    print(f'{nom_utilisateur} est majeur.')
else:
    print(f'{nom_utilisateur} est mineur.')
```

**Résultat** : `iliass est majeur.`

### Boucles

J'ai utilisé les boucles pour répéter des actions. Python propose les boucles `for` et `while`.

- **Boucle for** : Itère sur une séquence (comme une liste ou un range).

```python
print('Boucle For:')
for i in range(5):
    print(i)
```

- **Boucle while** : Continue tant qu'une condition est vraie.

```python
print('\nBoucle While:')
compte = 0
while compte < 5:
    print(compte)
    compte += 1
```

**Résultat** :
```
Boucle For:
0
1
2
3
4

Boucle While:
0
1
2
3
4
```

### Fonctions

J'ai regroupé du code réutilisable en définissant des fonctions. Voici un exemple de définition et d'appel d'une fonction :

```python
def saluer(nom):
    print(f'Bonjour, {nom}!')

saluer('iliass')
```

**Résultat** : `Bonjour, iliass!`

### Commenter le code

J'ai utilisé des commentaires pour expliquer le code, qui sont ignorés par l'interpréteur Python. J'ai utilisé `#` pour ajouter un commentaire :

```python
# Ceci est un commentaire
print("Ceci n'est pas un commentaire")
```

### Erreurs et exceptions

J'ai géré les erreurs potentielles dans le code en utilisant `try` et `except` pour capturer les exceptions :

```python
try:
    resultat = 10 / 0
except ZeroDivisionError:
    print("Erreur : division par zéro.")
```

**Résultat** : `Erreur : division par zéro.`

### Modules et packages

J'ai structuré le code Python en utilisant des modules et packages. J'ai utilisé `import` pour inclure des modules :

```python
import math

print(math.sqrt(16))  # Utilisation d'une fonction du module math
```

**Résultat** : `4.0`

### Extraction et transformation de données

J'ai utilisé des bibliothèques comme `requests` et `Beautiful Soup` pour récupérer et analyser des données en ligne. Voici un exemple simplifié :

```python
import requests
from bs4 import BeautifulSoup

response = requests.get('https://example.com')
soup = BeautifulSoup(response.text, 'html.parser')

print(soup.title.string)
```

### Lecture et écriture de fichiers

J'ai utilisé la fonction `open()` pour lire et écrire des fichiers :

```python
# Écriture dans un fichier
with open('exemple.txt', 'w') as fichier:
    fichier.write('Bonjour, monde!')

# Lecture d'un fichier
with open('exemple.txt', 'r') as fichier:
    contenu = fichier.read()
    print(contenu)
```

**Résultat** : `Bonjour, monde!`

Ces étapes et concepts m'ont fourni une base solide pour le développement en Python sur Ubuntu.
