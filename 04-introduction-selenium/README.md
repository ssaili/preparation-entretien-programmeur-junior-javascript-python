# Introduction à Selenium 🕸️🔧

L'objectif de cette étape est de configurer votre environnement de développement pour utiliser Selenium sur Ubuntu, en installant les bibliothèques nécessaires et en vous familiarisant avec l'automatisation des tests. Vous apprendrez à exécuter des scripts Selenium simples en Python et JavaScript pour automatiser des tâches web, et comprendrez comment Selenium peut être utilisé pour manipuler le DOM via JavaScript.

## Configuration de l'environnement de développement pour Selenium sur Ubuntu 🛠️

1. **Installation de Selenium et des dépendances** 📥
   - Ouvrez un terminal et installez pip :
     pip est un gestionnaire de paquets pour Python. Il est essentiel pour installer des packages Python tels que Selenium.
     ```bash
     sudo apt install python3-pip
     ```
   ### Installation de Selenium pour Python

    Une fois pip installé, vous pouvez installer Selenium pour Python en exécutant la commande suivante dans le terminal :
    ```bash
    pip install selenium
    ```
  
    ### Installation de Selenium pour JavaScript
    
    Pour installer Selenium pour JavaScript, vous devez d'abord avoir Node.js et npm installés sur votre système. Ensuite, exécutez la commande suivante dans le terminal :
    ```bash
    npm install selenium-webdriver
    ```

2. **Vérification de l'installation** ✅
    ### Vérification pour Python

    Pour vérifier si Selenium est bien installé pour Python via pip, vous pouvez exécuter la commande suivante dans le terminal :
    
    ```bash
    pip show selenium
    ```
    ### Vérification pour JavaScript

    Pour vérifier si Selenium WebDriver est installé pour JavaScript, exécutez la commande suivante dans le terminal :
    ```bash
    npm list selenium-webdriver
    ```

## Comprendre Selenium et son utilisation

Selenium est un outil puissant pour l'automatisation des tests web, permettant de simuler des interactions utilisateur avec un navigateur web et facilitant ainsi les tests fonctionnels des applications web. Voici un aperçu des différents types de tests automatisés, notamment les tests unitaires, d'intégration, et end-to-end, ainsi que leur utilité, avec des exemples simples pour chacun :

### Tests Unitaires
Les tests unitaires se concentrent sur les plus petites unités de code, comme les fonctions ou les méthodes individuelles, pour s'assurer qu'elles fonctionnent correctement.  
**Exemple :** Tester une fonction `somme(a, b)` qui retourne la somme de deux nombres pour vérifier qu'elle donne le résultat attendu, par exemple `somme(2, 3)` devrait retourner `5`.

### Tests d'Intégration
Les tests d'intégration vérifient que les différents modules ou services d'une application fonctionnent bien ensemble. Ils sont essentiels pour détecter les problèmes d'interaction entre les composants, qui ne seraient pas visibles lors des tests unitaires.  
** Exemple : S'assurer qu'après la soumission d'un formulaire de contact, une notification de confirmation est envoyée à l'utilisateur.

### Tests End-to-End (E2E)
Les tests end-to-end valident le fonctionnement complet d'une application du début à la fin, en simulant des scénarios réels d'utilisation. Ils se concentrent sur l'expérience utilisateur finale, vérifiant que tous les composants fonctionnent ensemble dans des conditions réalistes.  
**Exemple :** Simuler un utilisateur qui remplit un formulaire de contact sur un site web, en saisissant son nom, son adresse e-mail et son message, puis en soumettant le formulaire pour s'assurer qu'il reçoit une confirmation de soumission réussie.

## Scripts Selenium en JavaScript et Python

Ces scripts naviguent vers la page de [mon profil GitHub](https://github.com/ssaili) et vérifient la présence du message "Bienvenue sur mon profil GitHub! 👋".

### Écrire un script Selenium en Python 🐍

- **Script simple en Python** :
  ```python
  from selenium import webdriver
  from selenium.webdriver.common.by import By

  driver = webdriver.Chrome()
  driver.get("https://github.com/ssaili")
  try:
      element = driver.find_element(By.XPATH, "//*[contains(text(), 'Bienvenue sur mon profil GitHub! 👋')]")
      assert element is not None
      print("Message trouvé : 'Bienvenue sur mon profil GitHub! 👋'")
  except:
      print("Message non trouvé.")
  finally:
      driver.quit()
  ```

### Écrire un script Selenium en JavaScript 🖥️

- **Script équivalent en JavaScript** :
  ```javascript
  const { Builder, By } = require('selenium-webdriver');

  (async function example() {
    let driver = await new Builder().forBrowser('chrome').build();
    try {
      await driver.get('https://github.com/ssaili');
      let element = await driver.findElement(By.xpath("//*[contains(text(), 'Bienvenue sur mon profil GitHub! 👋')]"));
      if (element) {
        console.log("Message trouvé : 'Bienvenue sur mon profil GitHub! 👋'");
      }
    } catch (error) {
      console.log("Message non trouvé.");
    } finally {
      await driver.quit();
    }
  })();
  ```
