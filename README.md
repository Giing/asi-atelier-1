# asi-atelier-1

## Sujet 

Vous êtes en phase de création d’un projet de jeu de plateau sur une application web. En tant que
responsable projet de cette application vous souhaitez explorer deux méthodes pour représenter
l’IHM :
- Utilisation de Web Statique en interaction avec un Web Service existant via javascript et AJAX.
- Utilisation du Web Dynamique en utilisant la technologie Springboot et tout particulièrement
les Thymeleaf et les Services.

Dans un second temps, réaliser à nouveau le formulaire et l’affichage d’une carte en Web Dynamique
en simulant des données dans le programme.

Après avoir expliqué en quoi vos prototypes respectent le pattern MVC, expliquer les avantages et
inconvénients des approches Web Statique + Web Service et Dynamique.

## Tableau récapitulatif

|               | Web statique + microservices                                                                                                                                                                                                              | Web dynamique                                                                                                                                              |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Définition    | Une page web statique charge un fichier HTML statique chez le client. Le client va ensuite faire une ou plusieur requêtes aux webservices pour  récupérer les données et construire la page chez le client. Le rendu se fait côté client. | La page est construite côté serveur grâce un moteur de templating.  Elle est renvoyée au client en une seule fois au client avec les données déjà chargée. |
| Avantages     | Pas besoin de recharger les pages. Affichage dynamique.                                                                                                                                                                                   | Plus rapide. Moins de temps pour charger les pages. Moins coûteux en développement.                                                                        |
| Inconvénients | Plus lent au démarrage (car pas de mise en cache) car on doit charger l'intégralité du site chez le client.                                                                                                                               | On doit recharger la page pour modifier les données de la vue. Moins adapté aux besoins actuels.                                                           |
| Technos       | Vue.js, Javascript, Ajax                                                                                                                                                                                                                  | Blade, PHP, Twig, Thymleaf                                                                                                                                 |

## Questions

Qu’est-ce que le pattern MVC ? Quels avantages présente-t-il ? 
> Le pattern MVC est une architecture logicielle qui découpe une application en 3 blocs. Le modèle qui contient les données à afficher.

Qu’est-ce que le Web dynamique ?
pourquoi est-il intéressant ? 

Comment sont récupérés les fichiers par le Web Browser en Web
statique ? 

Quels sont les avantages d’utiliser du Web Statique avec des services REST ?


Qu’est que les architectures N-Tiers ? Quelles avantages apportent-elles ?


Comment fonction l’AJAX ?

Qu’est-ce que JEE ? Comment fonctionne un serveur JEE ? Qu’est-ce qu’un Web Container en JEE ?

Qu’est ce que Springboot ? quelles différences avec JEE ?
> Spring Boot est un framework de développement JAVA. C'est une déclinaison du framework classique de Spring qui permet essentiellement de réaliser des microservices (ce sont la majeure partie du temps des services web qui sont regroupés en API). Springboot s'affranchit de certaines règles de JEE afin d'avoir un temps d'avance notamment sur les fonctionnalités qu'il propose.

Qu’apport Thymeleaf à Springboot ?
> Thymeleaf est un template engine (moteur de rendu de document) écrit en Java. Principalement conçu pour produire des vues Web, il fournit un support pour la génération de documents HTML, XHTML, JavaScript et CSS (voire de n’importe quel format texte).

Que signifie l’annotation @Controller, pourquoi est-elle importante lors de la génération de pas coté serveur ?
> L'annotation @Controller de Spring est une spécialisation de l'annotation @Component. L'annotation @Controller indique qu'une classe particulière joue le rôle d'un contrôleur. Il est utilisé pour marquer une classe comme un gestionnaire de requête web. Elle est surtout utilisée avec les applications Spring MVC. Cette annotation agit comme un stéréotype pour la classe annotée, indiquant son rôle.

Que représente le répertoire ‘src/main/resources’ dans un projet SpringBoot ? Quelles sont les
informations stockées à cet endroit ?
> Le répertoire représente des ressources statiques. Des fichiers de config comme: ```application.properties```, ce fichier est utilisé pour paramétrer le comportement par défaut de l’application. En fonction des dépendances déclarées dans notre projet et en fonction de la valeur des propriétés présentes dans ce fichier, Spring Boot va adapter la création du contexte d’application.