
## SPRING

Spring est un framework open source pour construire et définir l'infrastructure d'une application Java5, dont il facilite le développement et les tests.

## Maven

Maven : installation et configuration en ligne de commande

Principe :

Il permet notamment :
-d'automatiser certaines tâches : compilation, tests unitaires et
-déploiement des applications qui composent le projet
-de gérer des dépendances vis-à-vis des bibliothèques nécessaires au
projet
-de générer des documentations concernant le projet

## Spring boot

Un projet est configuré via un fichier pom.xml contenant toutes les spécificités du projet. Il regroupe toutes les dépendances, version (du jdk), plugins, et propriété attenant au projet.

Ce fichier pom.xml peut être généré automatiquement via Spring Initializr. En allant sur https://start.spring.io/ , on peut configurer son projet automatiquement, en spécifiant le nom du projet, sa description, sa version du jdk… et ses dépendances (web, sql, etc…). Spring Initializr va alors générer un fichier (contenant également un pom.xml) qui créera le squelette (l’arborescence) du projet.
Il suffira de l’importer et de s’assurer que Maven le repère afin que le projet s’initialise correctement dans l’IDE.
    A partir de là, on peut commencer à travailler sans se soucier d’importer des dépendances supplémentaires.

La commande mvn spring-boot:run permet de compiler, exécuter et héberger un projet en local (on peut d’ailleurs facilement y accéder avec l’url http://localhost:8080/)

Cela à l’avantage de repérer en début de projet, si la configuration est “propre”, et dans le cas contraire d'ajouter les dossiers manquants (par exemple le dossier target).
Si tout s'exécute sans erreur, on peut dès lors commencer à travailler sur son projet.

##L’architecture d’un projet et la notion de couplage:

    Un projet avec un couplage fort, signifie qu’il y a un fort “lien” entre plusieurs classes et interfaces. C’est plus facile à construire, mais plus difficile à maintenir à jour car toutes les classes dépendent des unes et des autres.

    Un projet avec un couplage faible va gérer ces liens entre classes de manière “externe”. L’arborescence dans le package aura:
    -un controller: qui se charge d’appeler les classes dont il a besoin
    -un dao: qui contiendra les liens entres ces classes
    -un repository: qui contiendra des objets


## JDBC

    Le JDBC est une interface de programmation qui permet aux application Java de communiquer avec une base de donnée et d’y effectuer des traitements (CRUD : create, read, update, delete).



#Lors du Dojo jeudi, révision sur les collections en Java, nous avons revu la manipulation des Map.
