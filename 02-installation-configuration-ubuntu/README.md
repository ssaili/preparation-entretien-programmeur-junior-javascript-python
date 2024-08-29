# Installation et configuration d'Ubuntu 🚀

L'objectif de cette étape est d’installer Ubuntu. J'ai listé dans ce fichier les étapes qui m’ont permis d’y parvenir.

**Note :** Je travaille sous macOS et j’ai décidé d’installer Ubuntu avec **UTM** (un logiciel de virtualisation gratuit et open source pour macOS).

## Étapes d'installation 🛠️

1. **Téléchargement de UTM** 📥
   * Je me suis rendu sur le site officiel de UTM et j'ai téléchargé la dernière version de l'application.
   * J'ai installé UTM comme n'importe quelle autre application sur macOS.

2. **Téléchargement de l'image ISO d'Ubuntu** 📥
   * Je suis allé sur le site d'Ubuntu et j'ai téléchargé l'image ISO de la dernière version compatible ARM (Ubuntu 22.04.4 LTS).

3. **Création d'une nouvelle machine virtuelle dans UTM** 💻
   * J'ai ouvert UTM et j'ai cliqué sur le bouton “+” pour créer une nouvelle machine virtuelle.
   * J'ai sélectionné “Virtualize” pour une meilleure performance et j'ai choisi linux.

4. **Configuration de la machine virtuelle** ⚙️
   * **Chargement de l'image ISO** : Dans les paramètres de la VM, je suis allé dans l'onglet “Boot ISO Image” et j'ai sélectionné l'image ISO d'Ubuntu que j'avais téléchargée.
   * **Allocation des ressources** : Il faut assigné au moins 4 Go de RAM et configuré le stockage à un minimum de 25 Go.
   * **Sauvegarder la configuration** : J'ai ensuite sauvegarder la configuration en cliquant sur “enregistrer“.

5. **Installation d'Ubuntu** 🐧
   * J'ai démarré la VM en cliquant sur le bouton “Play”.
   * J'ai suivi les instructions à l'écran pour installer Ubuntu.

6. **Configuration post-installation** 🔧
   * Une fois l'installation terminée, j'ai mis à jour le système en exécutant les commandes suivantes dans le terminal Ubuntu :
     ```bash
     sudo apt update (télécharge les informations les plus récentes sur les paquets)
     sudo apt upgrade (effectue la mise à jour des paquets installés vers leurs nouvelles versions)
     ```
   * J'ai installé les outils nécessaires pour le partage du presse-papiers et des répertoires entre ma machine virtuelle et l’environnement hôte :
     ```bash
     sudo apt install spice-vdagent spice-webdavd
     ```
