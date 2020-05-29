##RECAP SEMAINE 3

MySQL
Prendre en main MySQL
MySQL est un SGBD sous double licence. La licence varie en fonction de l'utilisation qui en est faite : dans un produit libre, la licence est la GPL et dans un produit propriétaire, c'est une licence propriétaire et payante qui s'applique.
Lancement:
Les commandes sont à lancer en root ou bien en les précédant de sudo 
Démarrez MySQL avec la commande suivante (le service peut aussi s'appeler mysqld avec un « d » final sous certaines distributions):
sudo /etc/init.d/mysql start
Vous pouvez vérifier s'il est bien lancé (status: started) en consultant son statut :
sudo /etc/init.d/mysql status
Arrêtez MySQL avec la commande :
sudo /etc/init.d/mysql stop
Lister les bases présentes :
SHOW DATABASES;
Se connecter à une base :
USE nom_base;
Créer une base :
CREATE DATABASE nom_base;
Supprimer une base :
DROP DATABASE nom_de_la_base;
Manipuler les tables
Lister les tables de la base active :
SHOW TABLES;
Afficher la structure d'une table :
DESCRIBE nom_table;
Créer une table :
CREATE TABLE nom_table ( listes des composants avec leur type ) ;
exemple :
CREATE TABLE personnes (
 id tinyint(4) unsigned NOT NULL auto_increment,
 nom varchar(80) NOT NULL,
 prenom varchar(80) NOT NULL,
 email varchar(32),
 PRIMARY KEY (id)
);
Supprimer une table :
DROP table nom_table;
Renommer une table :
ALTER TABLE nom_table RENAME AS nouveau_nom_table;
Export et import d'une base
Pour exporter une base dans un fichier, tapez la commande dans un shell :
mysqldump -u root -p nom_base > nom_base_sauvegarde.sql
Pour importer une base à partir d'un fichier :
mysql -u root -p nom_base < nom_base_sauvegarde.sql
Changer le mot de passe root quand on l'a oublié
Redémarrer MySQL : /etc/init.d/mysql restart 
Les BDD :
Les BDD Elles servent à Stocker, Organiser, Créer des Requêtes...
Outils : SQLite, Mariadb, MySQL, Mongodb, Hbase....
Créer des tables , des champs
Récupérere des données
Ajouter/Modifier/Supprimer des données
Relier des données entre elles
INSERT ---> Rajouter des données
SELECT ---> Chercher/Selectionner 1 donnée précise
