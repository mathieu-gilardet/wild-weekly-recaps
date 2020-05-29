# Récapitulatif semaine 3 :

## Base de données : Stockage des données, relations logiques.
### Vocabulaire :
  - Tables = 'entité'
  - champs = 'attributs'
  - tuple = 'ligne'...
  - clé primaire = 'id ...'
  
### Exemple de SGBD (Relationnels / NoSQL) ###
    - Relationnels : MySQL...
    - NoSQL : MongoDB...
  
### NoSQL != SQL###
  - NoSQL = Permets de récuperer les données en un seul appel, possibilités de duplications,
  - SQL = Pas de duplicaiton de données, mais besoin de structurer les données en amont,
  
## SQL ;##
  - Installation = différentes lignes de commandes suivant le système d'exploitation.
  - Configuration = Password, utilisation possible en ROOT ou à distance.
  
  STRUCTURED QUERY LANGUAGE 
 
### Utilité :###
- Créer des tables et des champs
- Récupérer des données
- Ajouter/modifier/supprimer des données
- Relier des données entre elles...
- Interroger la base donnée

Utilisable dans tous les SGBDR.

### Commande de bases :###
  - CREATE DATABASES = Création base de donnée,
  - CREATE .... = Création ..
  - TRUCANTE ... = Vider ..
  - DROP ... = Supprimer ..
  - INSERT INTO ... = Insertion ..
  - GRANT ... = Gère les droits d'accès.,
  - UPDATE, DELETE....
  
 - SELECT ... = Sélection ...
  --> SELECT * FROM ... ;
  
### Connexion :###

Connexion->  - mysql -u 'user' -p 
Connexion à une base--> mysql -u 'user' -D 'database' -p
Importation d'une base--> ...-p < abc.sql

Utilisation d'interface graphique pour modélisation : MySQL Workbench, ...

## Merise :##
### - Modèle Conceptuel de données (MCD)###

Permet d'établir une représentation claire des données et définit
les dépendances fonctionnelles de ces données entre elles.

Passage à MLD -> On ne garde que les entités, ajout des tables de jointures

### - Modèle Logique de données (MLD)###

Traduction du modèle conceptuel de données en y ajoutant
notamment les clés primaires et clés étrangères

Passage à MPD -> Insertion des types, des contraintes et des indexes

### - Modèle Physique de données (MPD)###

Représentation finale d’une base de données, prenant en
compte les spécificités du SGBD utilisé

### Points à souligner :###
  - Cardinalités : 
     - One To One (1, 1)
     - Many To One (1, n)
     - Many To Many (n, m)
     
  - Clé étrangère = Toujours du côté du One pour One To Many,
  - Table de jonction = Obligatoire pour Many To Many,
  - Contraintes d'intégrité = Cascade, "élimine automatiquement les champs en rapport avec l'occurence supprimée"
  
  ## SQL Advanced ##
  
  ### Recherche d'informations :##
    - Utilisation du language SQL,
    - Commandes étudiées : SELECT, FROM, --> WHERE : 
        - LIKE, AND, BETWEEN, IN,...
    - SELECT -->
        - DISTINCT, CONCAT, LENGTH, ...
    - Opérateur d'agrégation :
        - COUNT(*) AS , SUM(), AVG(),..
    - GROUP BY, HAVING, 
    - JOIN = 'Association des deux tables par une fonciton de champs commun', possibilité d'imbrication,
        - Différents types : LEFT, RIGHT, INNER, OUTER,
    - UNION = Cumul des résultats des requêtes
 
 ## Collection##
 ### LiveCoding###
  - Interface Map / Set / List
    - Map : HashMap, TreeMap, ...
    - Set : TreeSet, HashSet, ...
    -List : ArrayList, LinkedList, ...
 
 
 
 ## SPRING##
 ### C'est quoi ?###
 - Spring est un framework open source pour construire et définir l'infrastructure d'une applicaiton Java, dont il faicilité le développement et les tests (#merciwiki)
### A quoi ça sert ?###
- Développement d’applications web
- Destiné aux entreprises
- Basé sur Java : robuste et portable
- Déployé et exécuté sur un serveur d'applications

" Spring se focalise sur la "plomberie" des applications ..., afin dque les équipes puissent se focaliser sur ..., la logique métier ...

--> A éclaircir la semaine prochaine.

  

  
