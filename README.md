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
> Le pattern MVC est une architecture logicielle qui découpe une application en 3 blocs. Le modèle qui contient les données à afficher. La view qui contient l'interface graphique. Et le controller qui contient les traitement des requetes faîtes par l'utilisateur.


| Avantages |
|---|
| - Facilement scalable<br>- Processus de développement plus rapide car il est plus simple de répartir la charge de travail au sein d'une équipe de dev.<br>- Le modèle est découplé de la vue<br>- Facilement maintenable |


Qu’est-ce que le Web dynamique ? pourquoi est-il intéressant ? 
> Le web dynamique consiste à faire créer une page par le serveur grace à un moteur de template et à la renvoyer à l'utilisateur.

Comment sont récupérés les fichiers par le Web Browser en Web
statique ? 

> En Web statique le web browser fait une requête au serveur qui lui renvoie les fichier tel quel.

Quels sont les avantages d’utiliser du Web Statique avec des services REST ?

> On peut récupérer les données des ressources exposées et mettre à jour la page en conséquences.


Qu’est que les architectures N-Tiers ? Quelles avantages apportent-elles ?

> Les architecures N-tier découpent la couche des services métier en plusieurs blocs. Cela offre plusieurs avantages :
> - Offre une meilleure scalabilité. On peut allouer plus de ressource à un service en particulier. 
> - La distibution est plus simple.
> - Les évolutions sont plus facile car on peut cibler un seul service à faire évoluer qui est découplé des autres services.


Comment fonctionne l’AJAX ?
> L'AJAX est une requête HTTP programmée pour être lancée après une action. Cette requête s'envoie sans rechargement de la page.

Qu’est-ce que JEE ? Comment fonctionne un serveur JEE ? Qu’est-ce qu’un Web Container en JEE ?
> JEE est un ensemble de norme pour la plateforme Java.

Qu’est ce que Springboot ? quelles différences avec JEE ?

Qu’apport Thymeleaf à Springboot ?

Que signifie l’annotation @Controller, pourquoi est-elle importante lors de la génération de pas coté
serveur ?

Que représente le répertoire ‘src/main/resources’ dans un projet SpringBoot ? Quelles sont les
informations stockées à cet endroit ?