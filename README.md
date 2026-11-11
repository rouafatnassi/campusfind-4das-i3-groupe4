<div align="center">

# CampusFind

### Trouver un espace, réserver une salle et étudier ensemble.

Plateforme universitaire de recherche d’espaces de travail, de réservation et de collaboration étudiante, construite autour d’une architecture microservices.

</div>

---

## Présentation

CampusFind aide les étudiants à mieux organiser leur vie sur le campus. La plateforme rassemble dans une même application la recherche d’espaces d’étude, la réservation de salles, les échanges entre étudiants et le signalement de problèmes dans les espaces universitaires.

Le projet est organisé en services indépendants afin de séparer les principaux domaines fonctionnels et de faciliter leur développement et leur évolution.

## Fonctionnalités

- **Recherche d’espaces d’étude** selon le calme, la capacité et les équipements, avec consultation des horaires, caractéristiques et localisation sur le campus.
- **Gestion des comptes étudiants** : inscription, authentification, profils, rôles et préférences.
- **Espace d’expression étudiant** : publications anonymes, expériences, questions, commentaires et réactions.
- **Réservation de salles** : consultation des disponibilités, réservation par date et heure, consultation et annulation des réservations.
- **Communauté étudiante** : création et découverte de groupes de travail, organisation de séances de révision et échanges autour des activités.
- **Signalement des problèmes du campus** : description d’un problème, ajout de photos et suivi du traitement.
- **Notifications et messagerie** pour accompagner les échanges et les activités de la plateforme.

## Architecture

CampusFind repose sur une architecture composée de microservices Spring Boot et de services d’infrastructure :

| Composant | Rôle |
| --- | --- |
| API Gateway | Point d’entrée et routage des requêtes vers les services |
| Eureka Discovery | Découverte et enregistrement des services |
| Config Server | Centralisation de la configuration |
| Keycloak | Gestion de l’authentification et des accès |
| Docker Compose | Orchestration de l’environnement conteneurisé |
| Application Web | Interface utilisateur de la plateforme |

### Microservices métier

1. Study Space Service
2. User Management Service
3. Student Expression Service
4. Room Reservation Service
5. Study Community Service
6. Campus Issues Service

### Service commun

- Notification & Messaging Service

## Équipe et responsabilités

| Membre | Responsabilité | Périmètre fonctionnel |
| --- | --- | --- |
| **Ranya Addouli** | Study Space Service | Recherche et filtres d’espaces, caractéristiques, horaires, équipements et localisation sur le campus. |
| **Ahmed Khadraoui** | User Management Service | Inscription, authentification, profils étudiants, rôles et préférences du compte. |
| **Tansim Daham** | Student Expression Service | Publications anonymes, partage d’expériences, commentaires, réactions, questions et discussions. |
| **Oumayma Miladi** | Room Reservation Service | Disponibilités des salles, réservations par date et heure, consultation et annulation. |
| **Roua Fatnassi** | Study Community Service | Groupes de travail, matières, séances de révision et échanges autour des activités de groupe. |
| **Wajdi Touj** | Campus Issues Service | Signalements avec photos, suivi des problèmes de matériel, de prises ou de propreté. |

## Technologies

- **Backend :** Java, Spring Boot, microservices
- **Routage :** API Gateway
- **Découverte de services :** Eureka
- **Configuration :** Spring Cloud Config Server
- **Authentification et gestion des accès :** Keycloak
- **Conteneurisation et orchestration locale :** Docker, Docker Compose
- **Frontend :** application Web

> Les versions et technologies spécifiques du frontend, des bases de données et des outils de test seront précisées lors de leur intégration au dépôt.

## Organisation du dépôt

Le dépôt regroupe les éléments du projet, qui sont organisés autour des axes suivants :

- **Backend :** services métier et composants d’infrastructure.
- **Frontend :** application Web CampusFind.
- **Documentation :** diagrammes d’architecture et présentation du projet.

La structure exacte des dossiers dépend de l’intégration des composants dans le dépôt.

## Démarrage

Les instructions de démarrage détaillées seront ajoutées après l’intégration des services, de l’application Web et de leur configuration Docker Compose.

À terme, l’environnement local nécessitera notamment :

- Java et Maven ou Gradle, selon la configuration des services ;
- Docker et Docker Compose ;
- les variables d’environnement et la configuration Keycloak requises par le projet.

Une fois le fichier Compose et la configuration intégrés, le démarrage pourra se faire depuis le dossier qui contient ce fichier, avec la commande adaptée au dépôt, par exemple :

```bash
docker compose up --build
```

Cette commande est indicative : les services, ports, variables d’environnement et éventuelles étapes d’initialisation devront être documentés ici après intégration.

## Configuration

Ne placez pas de mots de passe, de secrets Keycloak, de clés ou d’autres informations sensibles dans le dépôt. Utilisez les mécanismes de configuration prévus par le projet et fournissez un fichier d’exemple sans valeurs sensibles lorsque la configuration sera intégrée.

## Documentation

Les diagrammes d’architecture et la présentation du projet seront disponibles dans la partie documentation du dépôt après leur intégration.

## État du projet

La plateforme est en cours de développement et d’intégration. Les consignes d’installation, la configuration complète et les modalités de lancement seront mises à jour à mesure que les composants seront disponibles.

## Contributions

Les contributions de l’équipe doivent rester cohérentes avec la séparation des responsabilités par service. Avant de proposer une modification, vérifiez les conventions et les instructions de développement qui seront ajoutées au dépôt.

## Licence

Aucune licence n’est spécifiée pour le moment. Les conditions de réutilisation et de distribution seront précisées ultérieurement.
