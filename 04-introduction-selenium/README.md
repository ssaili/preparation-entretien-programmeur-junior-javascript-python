# Introduction à Selenium 🕸️🔧

L'objectif de cette étape a été de configurer mon environnement de développement pour utiliser Selenium sur Ubuntu, en installant les bibliothèques nécessaires et en me familiarisant avec l'automatisation des tests. J'ai appris à exécuter des scripts Selenium simples en Python et JavaScript.

## Configuration de l'environnement de développement pour Selenium sur Ubuntu 🛠️

1. **Installation de Selenium et des dépendances** 📥
   - J'ai ouvert un terminal et installé pip :
     pip est un gestionnaire de paquets pour Python. Il est essentiel pour installer des packages Python tels que Selenium.
     ```bash
     sudo apt install python3-pip
     ```
   ### Installation de Selenium pour Python

    Une fois pip installé, j'ai pu installer Selenium pour Python en exécutant la commande suivante dans le terminal :
    ```bash
    pip install selenium
    ```
  
    ### Installation de Selenium pour JavaScript
    
    Pour installer Selenium pour JavaScript, j'ai d'abord dû avoir Node.js et npm installés sur mon système. Ensuite, j'ai exécuté la commande suivante dans le terminal :
    ```bash
    npm install selenium-webdriver
    ```

2. **Vérification de l'installation** ✅
    ### Vérification pour Python

    Pour vérifier si Selenium était bien installé pour Python via pip, j'ai exécuté la commande suivante dans le terminal :
    
    ```bash
    pip show selenium
    ```
    ### Vérification pour JavaScript

    Pour vérifier si Selenium WebDriver était installé pour JavaScript, j'ai exécuté la commande suivante dans le terminal :
    ```bash
    npm list selenium-webdriver
    ```

## Comprendre Selenium et son utilisation

Selenium est un outil puissant pour l'automatisation des tests web, permettant de simuler des interactions utilisateur avec un navigateur web et facilitant ainsi les tests fonctionnels des applications web. Cela permet de garantir qu'une application fonctionne correctement, est sécurisée, performante, et offre une expérience utilisateur optimale. Voici un aperçu des différents types de tests automatisés, notamment les tests unitaires, d'intégration, et end-to-end, ainsi que leur utilité, avec des exemples simples pour chacun :

### Tests Unitaires
Les tests unitaires se concentrent sur les plus petites unités de code, comme les fonctions ou les méthodes individuelles, pour s'assurer qu'elles fonctionnent correctement.  
**Exemple :** Tester une fonction `somme(a, b)` qui retourne la somme de deux nombres pour vérifier qu'elle donne le résultat attendu, par exemple `somme(2, 3)` devrait retourner `5`.

### Tests d'Intégration
Les tests d'intégration vérifient que les différents modules ou services d'une application fonctionnent bien ensemble. Ils sont essentiels pour détecter les problèmes d'interaction entre les composants, qui ne seraient pas visibles lors des tests unitaires.  
**Exemple :** S'assurer qu'après la soumission d'un formulaire de contact, une notification de confirmation est envoyée à l'utilisateur.

### Tests End-to-End (E2E)
Les tests end-to-end valident le fonctionnement complet d'une application du début à la fin, en simulant des scénarios réels d'utilisation. Ils se concentrent sur l'expérience utilisateur finale, vérifiant que tous les composants fonctionnent ensemble dans des conditions réalistes.  
**Exemple :** Simuler un utilisateur qui remplit un formulaire de contact sur un site web, en saisissant son nom, son adresse e-mail et son message, puis en soumettant le formulaire pour s'assurer qu'il reçoit une confirmation de soumission réussie.

## Scripts Selenium en JavaScript et Python

Ces scripts naviguent vers la page de [mon profil GitHub](https://github.com/ssaili) et vérifient la présence du message "Bienvenue sur mon profil GitHub! 👋".

### Écrire un script Selenium en Python 🐍

- **Script simple en Python** :
  ```python
  # Importation des modules nécessaires depuis Selenium
  from selenium import webdriver
  from selenium.webdriver.chrome.service import Service
  from selenium.webdriver.common.by import By

  # Configuration du service ChromeDriver avec le chemin vers l'exécutable
  service = Service(executable_path='/usr/bin/chromedriver')

  # Initialisation du navigateur Chrome avec le service configuré
  driver = webdriver.Chrome(service=service)

  # Ouvre la page web spécifiée
  driver.get("https://github.com/ssaili")

  try:
     # Recherche un élément sur la page contenant le texte spécifié
     element = driver.find_element(By.XPATH, "//*[contains(text(), 'Bienvenue sur mon profil GitHub! 👋')]")
    
     # Vérifie si l'élément a été trouvé
     assert element is not None
    
     # Si l'élément est trouvé, affiche un message dans la console
     print("Message trouvé : 'Bienvenue sur mon profil GitHub! 👋'")
  except:
     # En cas d'erreur (par exemple, si l'élément n'est pas trouvé), affiche un message d'erreur
     print("Message non trouvé.")
  finally:
     # Ferme le navigateur, que l'opération ait réussi ou échoué
     driver.quit()

  # Exécutez ce script avec la commande suivante :
  # python3 nom_du_fichier.py
  ```

### Écrire un script Selenium en JavaScript 🖥️

- **Script équivalent en JavaScript** :

  ```javascript
  // Importation des modules nécessaires depuis Selenium
  const { Builder, By } = require('selenium-webdriver');
  // Importation du module Chrome de Selenium
  const chrome = require('selenium-webdriver/chrome');

  // Configuration du service ChromeDriver avec le chemin vers l'exécutable
  const service = new chrome.ServiceBuilder('/usr/bin/chromedriver');

  // Fonction asynchrone auto-exécutante pour gérer les actions du navigateur
  (async function example() {
    // Initialisation du pilote pour le navigateur Chrome
    let driver = await new Builder()
      .forBrowser('chrome') // Spécifie l'utilisation de Chrome
      .setChromeService(service) // Associe le service ChromeDriver configuré
      .build(); // Construit l'instance du navigateur

    try {
      // Ouvre la page web spécifiée
      await driver.get('https://github.com/ssaili');

      // Recherche un élément sur la page contenant le texte spécifié
      let element = await driver.findElement(By.xpath("//*[contains(text(), 'Bienvenue sur mon profil GitHub! 👋')]"));

      // Si l'élément est trouvé, affiche un message dans la console
      if (element) {
        console.log("Message trouvé : 'Bienvenue sur mon profil GitHub! 👋'");
      }
    } catch (error) {
      // En cas d'erreur (par exemple, si l'élément n'est pas trouvé), affiche un message d'erreur
      console.log("Message non trouvé.");
    } finally {
      // Ferme le navigateur, que l'opération ait réussi ou échoué
      await driver.quit();
    }
  })();

  // Exécutez ce script avec la commande suivante :
  // node nom_du_fichier.js
  ```
