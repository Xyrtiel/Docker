# Application Multi-Services avec Docker Compose

Ce projet utilise Docker Compose pour orchestrer plusieurs services conteneurisés, chacun utilisant une technologie différente. L'application inclut un service web basé sur Flask, un service Node.js, un service de traitement en arrière-plan avec Java, une base de données PostgreSQL, et Redis pour la mise en cache.

## Vue d'Ensemble des Services

### 1. **Service de Sondage (Flask)**
- **Technologie**: Python 3.9 avec Flask
- **Ports**: Expose le port 80 dans le conteneur (mappé sur le port 5000 de l'hôte)
- **Description**: Service web utilisant Flask pour gérer la logique des sondages.

### 2. **Service de Travailleur (Java)**
- **Technologie**: Java avec Maven
- **Ports**: Aucun port exposé (service interne)
- **Description**: Service en arrière-plan qui traite les tâches asynchrones.

### 3. **Service de Résultats (Node.js)**
- **Technologie**: Node.js
- **Ports**: Expose le port 80 dans le conteneur (mappé sur le port 5001 de l'hôte)
- **Description**: Service Node.js qui gère l'affichage des résultats.

### 4. **Redis**
- **Technologie**: Redis (version Alpine)
- **Ports**: Expose le port 6379 dans le conteneur (mappé sur le port 6379 de l'hôte)
- **Description**: Serveur de cache pour améliorer la performance de l'application.

### 5. **Base de Données PostgreSQL**
- **Technologie**: PostgreSQL (version Alpine)
- **Ports**: Expose le port 5432 dans le conteneur (mappé sur le port 5432 de l'hôte)
- **Description**: Base de données relationnelle pour stocker les données des sondages et autres informations.
