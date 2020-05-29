## SQL
Langage permettant de communiquer avec une base de données

Une base de données est composée de tables qui sont composées de champs (ou colonnes) qui sont composés de tuples (ou lignes).

`Clé primaire` => C'est un identifiant unique qui permet d'identifier un enregistrement
`Clé étrangeres` => Permet de lier deux contenus de tables différentes

Requetes :

`CREATE` => Création de base de données et de tables
`SELECT` => Affichage de données
`DELETE` => Suppression de tuple
`UPDATE SET` => Modifier le contenu de tuple
`TRUNCATE` => Vider une table sans la supprimer
`DROP` => supprimer une table et son contenu (Attention au contraintes d'intégrité, utiliser CASCADE ou supprimer les dépendances avant de drop la table)
`ALTER` => Permet de modifier la structure d'un table (ADD pour ajouter / DROP pour supprimer)
`SHOW / DESCRIBE` => Afficher le contenu d'une table, DESCRIBE permet d'afficher les détails des les champs
`INSERT INTO` => Ajouter un tupple dans une table
`USE` => Selectionner une base de données
`GRANT` => Attribuer des droits a un utilisateur

`WHERE / AND / OR` => Condition
`JOIN (INNER, LEFT, RIGHT, OUTER), IMBRIQUÉES` => Jointure entre deux tables
`ORDER BY` => Définis dans quel ordre les données seront affichées
`DISTINCT` => Exclus une donnée de la séléction
`GROUP BY` => A utilise avec les fonction d'aggregation
`HAVING` => Condition a utiliser sur un groupement
`AS` => Alias


Fonctions de chaines de characteres :
`CONCATE()` => Concatene plusieurs données
`LENGHT()` => Donne la longueur d'une chaine de characteres

Fonctions de dates:
`DAYOFWEEK()` => Donne le jour de la semaine
`NOW()` => Donne la date du jour

Fonctions Mathematiques :
`RAND()` => Donne un chiffre aléatoire
`ROUND()` => Donne un arrondi

Fonctions d'agregation:
`COUNT()` => Compte le nombre de données
`AVG()` => Donne une moyenne des données concernées
`MAX() / MIN()` => Donne la donnée maximale ou minimale
`SUM()` => Additionne les données concernées

`TRANSACTION` => Suite de requêtes dont l'exécution se fait par bloc. Si tout le bloc d’instruction n’est pas exécuté (erreur), il est possible de revenir en arrière (ROLLBACK).

Utilisation de MySQL en CLI

MERISE:
Methode de conception et modelisation de Base de données

`ENTITÉS` => 
`CARDINALITÉS` =>
`ASSOCIATIONS` =>

`MCD` => 
`MLD` =>
`MPD` =>




## PHP

PHP CLI

Récuperation et sécurisation des données d'un formulaires en php

Coté front : Via les champs required, certains types d'input (tel, email...) et les patterns, implémentation de données de facon dynamique avec php
Coté Back : Lecture des données via GET et POST (ce sont des variables superglobales) 

# PDO 
Couche d'abstraction a la base de données

Injections SQL
