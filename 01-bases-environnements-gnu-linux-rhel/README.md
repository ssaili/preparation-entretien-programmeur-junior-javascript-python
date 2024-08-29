**Note :** Je travaille sous macOS, mais cela ne pose pas de problème pour cette partie, car macOS et Linux partagent les mêmes commandes via le terminal.

# Bases des environnements GNU/Linux-RHEL

## Introduction à Linux

### Familiarisation avec les concepts de base des systèmes d'exploitation GNU/Linux, en particulier RHEL

**Résumé des concepts :**

Le projet GNU a été lancé en 1983 avec l'objectif de créer un système d'exploitation open source. Bien que le projet GNU ait développé de nombreux composants essentiels d'un système d'exploitation (outils et logiciels comme GNU Bash ou GNU Parted), il lui manquait un noyau fonctionnel. C'est là qu'intervient Linux, un noyau développé par Linus Torvalds en 1991.

**Le Noyau Linux**

Le noyau Linux est le composant principal d'un système d'exploitation Linux. Il agit comme une interface entre le matériel de l'ordinateur et les processus (programme en cours d'exécution sur un ordinateur), gérant les ressources du système de manière efficace. Voici quelques-unes de ses fonctions clés :

- **Gestion de la mémoire :** Le noyau suit les contenus stockés, leur emplacement et l'espace mémoire utilisé.
- **Gestion des processus :** Il identifie quels processus peuvent solliciter le processeur, à quel moment et pour quelle durée.
- **Pilote des périphériques :** Le noyau sert de médiateur entre le matériel et les processus.

Sans un noyau fonctionnel, le système d'exploitation ne peut pas opérer.

**Red Hat Enterprise Linux (RHEL)**

RHEL est une distribution commerciale de Linux développée par Red Hat. Elle est largement utilisée dans les environnements professionnels et les serveurs en raison de sa stabilité, de son support technique et de ses fonctionnalités avancées pour la sécurité et la gestion des systèmes. Voici quelques caractéristiques spécifiques à RHEL :

- **Support commercial :** RHEL est connu pour son support technique professionnel, ce qui en fait un choix privilégié pour les entreprises.
- **Sécurité renforcée :** RHEL intègre des outils comme SELinux pour améliorer la sécurité du système.
- **Gestion des paquets :** RHEL utilise yum (et son successeur DNF) pour la gestion des paquets, facilitant l'installation et la mise à jour des logiciels.

RHEL est conçu pour être utilisé dans des environnements de production, offrant des fonctionnalités robustes pour le déploiement et la gestion des systèmes à grande échelle.

### Exercices pratiques

- **Identifier les composants d'un système Linux :** Sur mon terminal macOS, j'utilise la commande `uname -a` pour afficher des informations sur mon système, voici ce qu'il affiche:

  ```
  Darwin Kernel Version 23.6.0: Mon Jul 29 21:14:30 PDT 2024; root:xnu-10063.141.2~1/RELEASE_ARM64_T6000 arm64
  ```

  Cette ligne indique la version du noyau Darwin utilisée par macOS, précisant la date de compilation, le numéro de version spécifique du noyau et le type de processeur utilisé (ARM64) .

- **Comparer les distributions :** Recherchez les différences entre RHEL et d'autres distributions comme Ubuntu, en termes de gestion des paquets, d'utilisation, et de public cible.

  RHEL utilise le gestionnaire de paquets YUM (et son successeur DNF) adapté aux entreprises recherchant stabilité et support professionnel, tandis qu'Ubuntu utilise APT, est gratuit, et s'adresse à un public plus large incluant les débutants et les développeurs individuels.

## Pratique des commandes de base du terminal

### Exercices pratiques

- **Navigation dans le système de fichiers :** J’utilise `pwd` pour afficher le répertoire courant, `ls` pour lister le contenu du répertoire courant, et `cd nomRepertoire` pour changer de répertoire. Je crée un répertoire avec `mkdir nomRepertoire` puis un fichier avec `touch nomFichier.extension`.

- **Gestion des processus :** J’utilise la commande `ps aux` via le terminal pour lister les processus en cours (ou `top` pour une liste dynamique des processus). Ensuite, pour terminer un processus j’utilise la commande `kill` suivie du PID du processus.

- **Permissions :** Je crée un fichier texte avec `touch fichier.txt`, modifie ses permissions avec `chmod numeroDePermission fichier.txt`, et change son propriétaire avec `chown nomProprietaire fichier.txt`.

## Outils et configurations RHEL

### Exploration des outils spécifiques à RHEL pour le développement

**Résumé des outils RHEL :**

Red Hat Enterprise Linux propose des outils spécifiques pour le développement, notamment le Red Hat Developer Toolset, qui inclut des versions stables et récentes de GCC (GNU Compiler Collection : Un ensemble de compilateurs pour divers langages de programmation.), GDB (GNU Debugger : Un débogueur avancé pour analyser et corriger les erreurs dans les programmes).

### Utilisation de gestionnaires de paquets comme yum

**Résumé de yum :**

YUM (Yellowdog Updater, Modified) est un gestionnaire de paquets pour RHEL qui permet d'installer, mettre à jour, et supprimer des logiciels tout en gérant automatiquement les dépendances nécessaires.

### Exercices pratiques

- **Simulation de commandes yum :** Je suis sur macOS, j’utilise brew comme gestionnaire de paquets. Après avoir consulté la documentation de yum, j’ai remarqué que YUM et Homebrew partagent des similitudes telles que l'utilisation de commandes pour installer (`yum install` / `brew install`), mettre à jour (`yum update` / `brew upgrade`), et supprimer (`yum remove` / `brew uninstall`) des paquets.
