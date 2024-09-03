# Connaissances des protocoles TCP/IP et du protocole HTTP 🌐📡

L'objectif de cette étape a été de comprendre les principes fondamentaux des protocoles TCP/IP et du protocole HTTP, essentiels pour la communication sur Internet.

## Protocoles TCP/IP 🖧

Un protocole en informatique est un ensemble de règles qui régissent la manière dont les données sont transmises et reçues sur un réseau. TCP/IP est un ensemble de protocoles qui permet la communication entre appareils sur un réseau, comme Internet. TCP (Transmission Control Protocol) et IP (Internet Protocol) ont des rôles distincts mais complémentaires dans ce processus.

1. **IP (Internet Protocol)**
   - IP est responsable de l'adressage et de l'acheminement des paquets de données depuis la source jusqu'à la destination. Chaque appareil sur le réseau possède une adresse IP unique, similaire à une adresse postale, qui permet aux paquets d'atteindre leur destination. IP ne garantit pas la livraison ordonnée ou fiable des paquets.

2. **TCP (Transmission Control Protocol)**
   - TCP s'assure que les données arrivent de manière fiable et ordonnée. Il établit une connexion entre l'expéditeur et le destinataire avant le transfert des données, segmente les données en paquets, et utilise des accusés de réception pour vérifier la réception correcte. En cas de perte, TCP retransmet les paquets manquants.

Ensemble, TCP et IP permettent une communication efficace et fiable entre appareils. IP s'occupe de l'acheminement des paquets, tandis que TCP assure la fiabilité et l'ordre des données transmises.

## Protocole HTTP 📑

### Étudier le fonctionnement du protocole HTTP

1. **Les bases du protocole HTTP**
   - HTTP (Hypertext Transfer Protocol) est le protocole qui permet aux navigateurs web et aux serveurs de communiquer entre eux pour échanger des informations sur le Web.
   - Il fonctionne comme un protocole de requête-réponse entre un client (navigateur) et un serveur web.

2. **Méthodes de requête HTTP**
   - Les méthodes de requête HTTP définissent les actions à effectuer sur les ressources identifiées par une URL. Les méthodes les plus courantes incluent GET, POST, PUT, DELETE, et PATCH.
   - Chaque méthode a un rôle spécifique, par exemple, GET est utilisé pour récupérer des données, tandis que POST est utilisé pour envoyer des données au serveur.

3. **Codes de statut HTTP**
   - Les codes de statut HTTP sont des réponses standard émises par les serveurs pour indiquer le résultat d'une requête HTTP.
   - Ils sont classés en cinq catégories : 1xx (informations), 2xx (succès), 3xx (redirection), 4xx (erreur du client), et 5xx (erreur du serveur).
   - Par exemple, un code 200 indique un succès, tandis qu'un code 404 signifie que la ressource demandée n'a pas été trouvée.
