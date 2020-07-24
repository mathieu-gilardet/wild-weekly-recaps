# **ApplicationPOZA Version 1.1 au 23/07/2020**

## **Navigateurs recommandés**
## **Logiciels utilisés**
## **Auteurs**
## **Installation**
## **Superviseurs**
## **Contacts**
## **Licence**


# **Introduction**

Le site [smoocyclette](https://smoocyapp.netlify.app/) est une application web réalisé pour L'entreprise Poza-event Cette application est une refonte de l'application précédente, avec des évolutions et améliorations pour permettre de former, suivre et répertorier les animateurs pour l’ensemble de des animations POZA.

# **Navigateurs recommandés**
Utilisez si possible, les derniers navigateurs web pour un affichage optimale des pages web comme: Google Chrome, Safari, Mozilla Firefox, Microsoft Internet Explorer >=11, Microsoft Edge

# **Logiciels utilisés**
**PHP7.4.3**
**SYMFONY 5.4**
**BOOTSTRAP v4.5.0**
**Twig**
**CKeditor 4**
**Facebook Plugin Page**
**Composer 1.10.0**
**Travis**
**Trello**
**Github**


# **Auteurs**
Cette application a été réalisé par Florent BELLENGER, Laurent TOULOUSE, Luis RODRIGUES et Sébastien Le Gal, étudiants à la Wild Code School de Biarritz.

# **Installation**
Cette application a été créé sous PHP7.4.3 en suivant l'architecture MVC (Modèle , Vue, Contrôleur) Les fichiers essentiels de l'application sont dans le dossier src.

Pour une mise en production via ftp/sftp: -> Se connecter au serveur Pour cela, il vous faudra au préalable, le nom d'hôte (Serveur) l'identifiant (Utilisateur) le mot de passe (password)

Pour une mise en production du site via le terminal du serveur :
 -> installer symfony en global sur votre machine

 -> Se mettre dans le dossier choisit -> git clone https://github.com/WildCodeSchool/biarritz-php-2006-project-smoothcyclette

 -> Créer le fichier .env.local a partir du fichier .env (copier coller le fichier renomer) et modifier la ligne 27 :

	DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name
 
	en y remplacant le champ db_user, db_password et db_name par votre user mysql, votre password mysql et le nom de la base de donnée : poza-event


Installer les dépendences avec la commande :
$ composer install
Installer et Initialiser yarn :
$ yarn install
$ yarn encore dev

Créer une **base de données**, avec la commande :

$ symfony console doctrine:database:create poza-event

Mettre à jour la base de données, avec la commande :
$ symfony console make:migration
$ symfony console doctrine:schema:update --force

Charger les fixtures :
$ symfony console doctrine:fixture:load --append

Lancer le serveur, avec la commande :
$ symfony server:start

Rendez-vous sur le site local :
localhost:8000 
Vous etes sur la page de conexion.

# **Informations de la Wild Code School**

**Project 2 - La Smoocyclette - Symfony 4.16.4**



# **Superviseurs**
Pierre ALEXALINE

# **Contacts**
Pour toutes demandes d'informations,N'hésitez pas à contacter directement l'école: Wild Code School 27 Route de Pitoys, 64600 Anglet 

Mail: pierre@wildcodeschool.fr

# **Licence**
Ce projet est la propriété de la Wild Code School et de Pierre ALEXALINE, Campus Manager: 06 ** ** ** **
