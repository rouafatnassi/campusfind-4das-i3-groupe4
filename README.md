# CampusFind

### Réserver une salle, retrouver un objet et étudier ensemble.

CampusFind est une plateforme universitaire qui facilite l'accès aux salles d'étude, la collaboration entre étudiants, les échanges sur la vie du campus et le suivi des objets perdus ou trouvés.

## Présentation

CampusFind est une application Web basée sur une architecture microservices. Elle permet aux étudiants de réserver des salles, de rejoindre des groupes de révision, de partager des publications, de signaler des problèmes sur le campus et de rechercher des objets perdus ou trouvés.

Chaque microservice possède ses propres responsabilités et sa propre base de données.

## Fonctionnalités

- **Room Reservation Service :** consulter les salles et leurs disponibilités, effectuer et annuler des réservations.
- **User Management Service :** gérer les comptes, profils, rôles et préférences des étudiants.
- **Student Expression Service :** publier des expériences, poser des questions, commenter et réagir aux publications.
- **Lost & Found Service :** déclarer des objets perdus ou trouvés, rechercher des annonces et suivre les récupérations.
- **Study Community Service :** créer des groupes de travail, rejoindre des groupes, organiser des séances et échanger entre membres.
- **Campus Issues Service :** signaler des problèmes sur le campus, joindre des photos et suivre leur traitement.
- **Notification Service :** informer les utilisateurs des événements importants des différents microservices.

## Architecture

CampusFind se compose de six microservices métier Spring Boot et d'un microservice commun Notification développé avec Node.js.

| Composant | Rôle |
| --- | --- |
| API Gateway | Routage des requêtes vers les microservices |
| Eureka | Découverte des microservices Spring |
| Config Server | Configuration centralisée |
| Keycloak | Authentification et gestion des accès |
| RabbitMQ | Communication asynchrone pour les notifications |
| Docker Compose | Démarrage de l'environnement |
| Frontend | Interface Web de l'application |

### Microservices métier

1. Room Reservation Service
2. User Management Service
3. Student Expression Service
4. Lost & Found Service
5. Study Community Service
6. Campus Issues Service

### Microservice commun

7. Notification Service — Node.js, Express, MongoDB et RabbitMQ.

## Équipe et responsabilités

| Membre | Microservice |
| --- | --- |
| Ranya Addouli | Room Reservation Service |
| Ahmed Khadraoui | User Management Service |
| Tansim Daham | Student Expression Service |
| Oumayma Miladi | Lost & Found Service |
| Roua Fatnassi | Study Community Service |
| Wajdi Touj | Campus Issues Service |

Le Notification Service et l'infrastructure commune sont développés en équipe.

## Technologies

- **Backend métier :** Java, Spring Boot et Spring Cloud.
- **Notification Service :** Node.js et Express.
- **Base de données :** une base indépendante par service ; PostgreSQL pour Study Community et Room Reservation, MongoDB pour Notification Service.
- **Communication :** API REST, OpenFeign et RabbitMQ.
- **Sécurité :** Keycloak et JWT.
- **Infrastructure :** Eureka, API Gateway, Config Server et Docker Compose.
- **Frontend :** application Web.

## Organisation du dépôt

Le projet comprend les dossiers suivants :

- **Backend/** : les microservices métier, le Notification Service et l'infrastructure.
- **Frontend/** : l'application Web.
- **Documentation/Presentation/** : la présentation du projet.
- **Documentation/Diagrams/** : les diagrammes de conception et d'architecture.
- **Documentation/Technical/** : les documents techniques des microservices.

## Démarrage

Le projet est en cours de développement. Les instructions complètes de lancement seront ajoutées après l'intégration des microservices et de Docker Compose.

Prérequis prévus : Java, Maven, Node.js et Docker.

Une fois l'environnement configuré, les services pourront être démarrés avec `docker compose up --build`, depuis le dossier contenant le fichier Compose.

## Configuration et sécurité

Les mots de passe, secrets Keycloak et autres informations sensibles ne doivent pas être ajoutés dans le dépôt GitHub. La configuration sera gérée avec des variables d'environnement et des fichiers d'exemple.

## Documentation

Les diagrammes, rapports de conception et présentations sont disponibles dans le dossier `Documentation`.

## État du projet

CampusFind est en cours de développement et d'intégration. Chaque membre travaille sur son microservice et contribue aux composants communs.