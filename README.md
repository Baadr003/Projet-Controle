# Système de Gestion des Commandes de Fournitures et des Fournisseurs

## Description
Ce projet est une application web développée en Java avec le framework Spring Boot. Elle permet à une entreprise de gérer les commandes de fournitures auprès de différents fournisseurs. L'application offre des fonctionnalités de gestion des fournisseurs et des fournitures associées, ainsi qu'une interface utilisateur conviviale pour visualiser et manipuler ces données.

## Fonctionnalités
- **Gestion des Fournisseurs** :
  - Ajouter un nouveau fournisseur avec son nom et son adresse.
  - Consulter la liste des fournisseurs.
  - Visualiser les détails d'un fournisseur, y compris les fournitures qu'il propose.
  - Supprimer un fournisseur.

- **Gestion des Fournitures** :
  - Ajouter une nouvelle fourniture avec son nom, sa quantité et son prix.
  - Associer une fourniture à un fournisseur.
  - Modifier les informations d'une fourniture.
  - Consulter la liste de toutes les fournitures disponibles.

## Structure du Projet

### Packages
- **controller** : Contient les contrôleurs de l'application qui gèrent les requêtes HTTP et contrôlent le flux entre la vue et les services.
  - `FournisseurController` : Contrôleur pour gérer les opérations CRUD des fournisseurs.
  - `FournitureController` : Contrôleur pour gérer les opérations CRUD des fournitures.

- **entities** : Contient les entités de l'application qui représentent les objets de données.
  - `Fournisseur` : Représente un fournisseur avec les attributs `nom`, `adresse` et une liste de fournitures fournies.
  - `Fourniture` : Représente une fourniture avec les attributs `nom`, `quantite`, `prix` et un lien vers le fournisseur.

- **repositories** : Contient les interfaces de dépôt pour interagir avec la base de données.
  - `FournisseurRepository` : Interface de gestion des fournisseurs, étendant `CrudRepository`.
  - `FournitureRepository` : Interface de gestion des fournitures, étendant `CrudRepository`.

- **resources/templates** : Contient les templates Thymeleaf pour l'interface utilisateur.

### Templates Thymeleaf
- `addFournisseur.html` : Formulaire pour ajouter un nouveau fournisseur.
- `addFourniture.html` : Formulaire pour ajouter une nouvelle fourniture.
- `detailsFournisseur.html` : Page pour afficher les détails d'un fournisseur, y compris les fournitures qu'il propose.
- `editFourniture.html` : Formulaire pour modifier les informations d'une fourniture.
- `index.html` : Page d'accueil de l'application.
- `listFournisseurs.html` : Page pour afficher la liste des fournisseurs.
- `listFournitures.html` : Page pour afficher la liste des fournitures disponibles.

### Fichier de configuration
- **`application.properties`** : Contient la configuration de l'application, incluant la connexion à la base de données.

## Prérequis
- **Java 11+** : Assurez-vous d'avoir Java 11 ou une version ultérieure installée.
- **Maven** : Pour gérer les dépendances et construire le projet.
- **Base de données** : Configurez une base de données compatible avec Spring Data JPA (par exemple, MySQL ou H2) et assurez-vous de mettre à jour les informations de connexion dans `application.properties`.

