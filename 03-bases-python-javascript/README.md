# Bases de Python et JavaScript 🚀

L'objectif de cette étape était de configurer les environnements de développement pour Python et JavaScript sur Ubuntu, en installant les outils et bibliothèques nécessaires tout en apprenant les bases de ces deux langages. Pour la partie Python, j’ai suivi le cours suivant du site OpenClassrooms : [Apprenez les bases du langage Python](https://openclassrooms.com/fr/courses/7168871-apprenez-les-bases-du-langage-python), qui m'a délivré le diplôme suivant : [Diplôme OpenClassrooms](https://github.com/ssaili/preparation-entretien-programmeur-junior-javascript-python/blob/main/03-bases-python-javascript/Diplo%CC%82me%20apprenez%20les%20bases%20du%20langage%20Python.pdf). Comme j'avais déjà une expertise en JavaScript, je détaillerai uniquement la partie de "configuration de l'environnement de développement JavaScript sur Ubuntu". 

## Python 🐍

## Configuration de l'environnement de développement pour Python sur Ubuntu 🛠️

1. **Installation de Visual Studio Code** 📥
   - J'ai téléchargé la version Ubuntu compatible ARM de Visual Studio Code depuis [le site officiel](https://code.visualstudio.com/download#).
   - J'ai ouvert le terminal et navigué vers le répertoire contenant le fichier d’installation de Visual Studio Code.
   - J'ai installé Visual Studio Code en exécutant la commande suivante :
     ```bash
     sudo apt install nom_du_fichier_d’installation.deb
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
  Les listes en Python sont des collections ordonnées d'éléments qui peuvent être modifiés après leur création. Cela signifie que vous pouvez ajouter, supprimer ou modifier des éléments dans une liste.

  ```python
  plateformes_sociales_liste = ["Facebook", "Instagram", "Snapchat", "Twitter"]
  ```

  - **Ajouter des valeurs** : Vous pouvez ajouter des éléments à une liste en utilisant la méthode `append()` pour ajouter un élément à la fin, ou `insert()` pour insérer un élément à une position spécifique.
    ```python
    plateformes_sociales_liste.append("LinkedIn")  # Ajoute "LinkedIn" à la fin de la liste
    plateformes_sociales_liste.insert(1, "WhatsApp")  # Insère "WhatsApp" à la position 1
    ```

  - **Accéder aux valeurs** : Vous pouvez accéder aux éléments d'une liste en utilisant des indices, où l'indice commence à 0 pour le premier élément.
    ```python
    premier_element = plateformes_sociales_liste[0]  # Accède au premier élément, "Facebook"
    dernier_element = plateformes_sociales_liste[-1]  # Accède au dernier élément, "LinkedIn"
    ```

  - **Méthodes de liste courantes** :
     - `extend(iterable)`: Ajoute tous les éléments d'un itérable (comme une liste) à la fin de la liste actuelle.
     - `insert(index, element)`: Insère un élément à la position spécifiée dans la liste.
     - `pop([index])`: Supprime et renvoie l'élément à la position donnée dans la liste. Si aucun index n'est spécifié, supprime et renvoie le dernier élément.
     - `index(element)`: Renvoie l'indice de la première occurrence de l'élément spécifié dans la liste.
     - `count(element)`: Renvoie le nombre de fois que l'élément spécifié apparaît dans la liste.
     - `reverse()`: Inverse l'ordre des éléments dans la liste.

- **Tuples** (immuables) :
  Les tuples sont similaires aux listes, mais ils sont immuables, ce qui signifie que vous ne pouvez pas modifier leurs éléments après leur création. Les tuples sont souvent utilisés pour regrouper des données qui ne doivent pas changer.

  ```python
  plateformes_sociales_tuple = ("Facebook", "Instagram", "TikTok", "Twitter")
  ```

  - **Accéder aux valeurs** : Comme les listes, vous pouvez accéder aux éléments d'un tuple en utilisant des indices.
    ```python
    premier_element_tuple = plateformes_sociales_tuple[0]  # Accède au premier élément, "Facebook"
    dernier_element_tuple = plateformes_sociales_tuple[-1]  # Accède au dernier élément, "Twitter"
    ```

### Dictionnaires

Un dictionnaire en Python est une structure de données qui permet d'enregistrer des paires clés-valeurs, où chaque clé unique est associée à une valeur.

- **Déclaration d'un dictionnaire** :
  ```python
  infos_utilisateur = {
      "prenom": "iliass",
      "age": 32,
  }
  ```

- **Ajouter une clé et une valeur** :
  Pour ajouter une nouvelle paire clé-valeur, vous pouvez simplement assigner une valeur à une nouvelle clé :
  ```python
  infos_utilisateur["ville"] = "Paris"
  ```

- **Accéder à une valeur via sa clé** :
  Pour accéder à la valeur associée à une clé spécifique, utilisez la clé entre crochets :
  ```python
  prenom = infos_utilisateur["prenom"]
  print(prenom)  # Affiche : iliass
  ```

- **Méthodes de dictionnaire courantes** :
  - `keys()`: Retourne une vue sur toutes les clés du dictionnaire.
  - `values()`: Retourne une vue sur toutes les valeurs du dictionnaire.
  - `items()`: Retourne une vue sur tous les couples (clé, valeur) du dictionnaire.
  - `get(clé)`: Retourne la valeur associée à la clé spécifiée. Si la clé n'existe pas, retourne `None`.
  - `pop(clé)`: Supprime la clé spécifiée et retourne la valeur associée. Si la clé n'existe pas, lève une exception `KeyError`.
  - `clear()`: Supprime tous les éléments du dictionnaire, le rendant vide.

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
print('Boucle While:')
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

En Python, un **module** est simplement un fichier contenant du code Python. Les modules vous permettent de structurer votre programme en petits morceaux réutilisables. Vous pouvez inclure un module dans votre code en utilisant le mot-clé `import`. Par exemple, le module `math` contient des fonctions mathématiques utiles :

```python
import math

print(math.sqrt(16))  # Utilisation d'une fonction du module math
```

**Résultat** : `4.0`

Un **package** est un dossier contenant un ensemble de modules Python. Les packages permettent d'organiser votre code en sous-dossiers et de créer des hiérarchies de modules. De nombreux packages populaires sont disponibles sur des dépôts en ligne tels que PyPI et peuvent être facilement installés à l'aide d'un gestionnaire de packages comme `pip`. Vous pouvez inclure des modules et des packages externes dans votre code avec `import`, et utiliser `from` pour importer directement un élément spécifique depuis un module :

```python
from math import sqrt

print(sqrt(16))  # Importation directe de la fonction sqrt
```

### Extraction et transformation de données

L'extraction de données web est un processus automatisé de récupération des données d'internet. Le terme ETL signifie extraction, transformation et chargement, et il est utilisé pour désigner le processus de récupération de données d'un endroit, de modification légère de ces données, et de leur sauvegarde dans un autre endroit. Les bibliothèques Python `requests` et `Beautiful Soup` peuvent vous aider à récupérer et analyser les données d'internet :

```python
import requests
from bs4 import BeautifulSoup

response = requests.get('https://example.com')
soup = BeautifulSoup(response.text, 'html.parser')

print(soup.title.string)  # Extraction du titre de la page
```

### Lecture et écriture de fichiers

Pour lire et écrire des fichiers en Python, vous pouvez utiliser la fonction intégrée `open()`, qui requiert deux paramètres : le nom du fichier et le mode. Les modes courants sont `"r"` pour la lecture, `"w"` pour l’écriture (écrasement) et `"a"` pour l’ajout. Voici comment vous pouvez lire et écrire dans un fichier :

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

## Configuration de mon environnement de développement pour JavaScript sur Ubuntu 🛠️

1. **Installation de Node.js** 📥
   - J'ai installé Node.js, un programme qui permet d'exécuter du JavaScript sur mon ordinateur sans navigateur. Il est essentiel pour utiliser des outils comme npm.
   - J'ai consulté la procédure d’installation pour Ubuntu sur le [site officiel](https://nodejs.org/fr/download/package-manager).

2. **Installation de `curl`** 🌐
   - `curl` est un outil en ligne de commande qui permet de télécharger ou d'envoyer des données à un serveur sur Internet.
   - J'ai installé `curl` en exécutant la commande suivante dans le terminal :
     ```bash
     sudo apt install curl
     ```

3. **Installation de NVM (Node Version Manager)** 🔄
   - NVM est un outil qui me permet de gérer plusieurs versions de Node.js sur mon système.
   - J'ai installé NVM en exécutant la commande suivante :
     ```bash
     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
     ```

4. **Téléchargement et installation de Node.js** 📦
   - J'ai utilisé NVM pour installer Node.js en exécutant :
     ```bash
     nvm install 20
     ```

5. **Vérification de l'installation** ✅
   - Je me suis assuré que Node.js était correctement installé avec :
     ```bash
     node -v
     ```
   - J'ai également vérifié la version de npm avec :
     ```bash
     npm -v
     ```

6. **Configuration de Visual Studio Code** ⚙️
   - J'ai lancé Visual Studio Code et installé les extensions suivantes pour améliorer mon expérience de développement JavaScript :
     - **ESLint** : Aide à détecter et corriger les erreurs dans votre code JavaScript en vérifiant qu'il respecte certaines règles de qualité.
     - **Prettier** : Formate automatiquement votre code pour qu'il soit propre et uniforme, ce qui facilite sa lecture et sa maintenance.
     - **Live Server** : Lance un serveur local qui recharge automatiquement votre page web dans le navigateur chaque fois que vous modifiez votre code.
     - **JavaScript (ES6) Code Snippets** : Fournit des raccourcis pour écrire plus rapidement du code JavaScript moderne, en insérant automatiquement des structures de code courantes.
