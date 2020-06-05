Récap semaine 4

## Bases SQL

Introduction aux bases de données:
installation de mysql ,phpmyadmin.

**CREATE DATABASE southwind;**
Création d'une base de donnée "southwind".

   
 **DROP DATABASE southwind;**
Suppression de la base "southwind".
   
**CREATE DATABASE IF NOT EXISTS southwind;**
Créer une base "southwind" si elle n'existe pas dèjà.
   
**DROP DATABASE IF EXISTS southwind;**
Suppression de la base "southwind" si elle existe.



## Commande UPDATE

La syntaxe basique d’une requête utilisant UPDATE est la suivante :

UPDATE table
SET nom_colonne_1 = 'nouvelle valeur'
WHERE _**condition**_

# Commande SELECT

L’utilisation la plus courante de SQL consiste à lire des données issues de la base de données. Cela s’effectue grâce à la commande SELECT, qui retourne des enregistrements dans un tableau de résultat. Cette commande peut sélectionner une ou plusieurs colonnes d’une table.

## Commande basique

L’utilisation basique de cette commande s’effectue de la manière suivante:

SELECT nom_du_champ FROM nom_du_tableau

Cette requête SQL va  **sélectionner**  (SELECT) le champ “nom_du_champ”  **provenant**  (FROM) du tableau appelé “nom_du_tableau”.

## Cours avancé : ordre des commandes du SELECT

Cette commande SQL est relativement commune car il est très fréquent de devoir lire les données issues d’une base de données. Il existe plusieurs commandes qui permettent de mieux gérer les données que l’ont souhaite lire. Voici un petit aperçu des fonctionnalités possibles qui sont abordées sur le reste du site:

-   Joindre un autre tableau aux résultats
-   Filtrer pour ne sélectionner que certains enregistrements
-   Classer les résultats
-   Grouper les résultats pour faire uniquement des statistiques (note moyenne, prix le plus élevé …)

Un requête SELECT peut devenir assez longue. Juste à titre informatif, voici une requête SELECT qui possède presque toutes les commandes possibles:

SELECT *
FROM table
WHERE condition
GROUP BY expression
HAVING condition
{ UNION | INTERSECT | EXCEPT }
ORDER BY expression
LIMIT count
OFFSET start

**A noter :**  cette requête imaginaire sert principale d’aide-mémoire pour savoir dans quel ordre sont utilisé chacun des commandes au sein d’une requête SELECT.

## La Methode MERISE !!!!!!

MCD : Un Modèle Conceptuel de Données est la formalisation de la structure et de la signification des informations décrivant des objets et des associations perçus d'intérêt dans le domaine étudié, en faisant abstraction des solutions et contraintes techniques informatiques d'implantation en base de données.

MLD : Le modèle logique des données consiste à décrire la structure de données utilisée sans faire référence à un langage de programmation. Il s'agit donc de préciser le type de données utilisées lors des traitements.Ainsi, le modèle logique est dépendant du type de base de données utilisé.

MPD : Dans la méthodologie [Merise](https://www.base-de-donnees.com/merise/), le **MPD** (**Modèle Physique des Données**) fait suite au [MCD](https://www.base-de-donnees.com/mcd/). Ensuite viendra le [MLD](https://www.base-de-donnees.com/mld/).   
L’étape de création du MPD est presque une formalité comparée à la création du MCD. En s’appuyant sur des règles simples (et qui fonctionnent à tous les coups), l’analyste fait évoluer sa modélisation de haut niveau pour la transformer en un schéma plus proche des contraintes des logiciels de bases de données. Il s’agit de préparer l’implémentation dans un [SGBDR](https://www.base-de-donnees.com/sgbd/).  
Concrètement, cette étape permet de **construire la structure finale de la base de données** avec les différents liens entre les éléments qui la composent.


## Les Jointures SQL  
Les jointures en SQL permettent d’associer plusieurs tables dans une même requête. Cela permet d’exploiter la puissance des bases de données relationnelles pour obtenir des résultats qui combinent les données de plusieurs tables de manière efficace.
Voici quelques liens vers des 'bibliothèques' de commandes SQL
[commandes](https://sql.sh/cours)
[site sympa avec des exemples](https://www.ntu.edu.sg/home/ehchua/programming/sql/mysql_beginner.html)

## AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
##

## PHP formulaires - Sécurisation - PDO

Création d'un formulaire de récupération , sécurisation de ce formulaire puis envoie en BDD.
exemple de fonction de sécurisation pour vérifier un email:

    function test_input($data) : string  
    
        {  
          $data = trim($data);  
          $data = stripslashes($data);  
          $data = htmlspecialchars($data);  
         return $data;  
        }
        
        if (empty($_POST["email"])) {  
          $emailErr = "Email is required";  
        } else {  
          $email = test_input($_POST["email"]);  
        }  
        // check if e-mail address is well-formed  
        if (!filter_var ($email, FILTER_VALIDATE_EMAIL)) {  
          $emailErr = "Invalid email format";  
        }



## Commande POST et GET

methode POST:
exemple d'envoie avec de donnée avec la méthode POST avec HTML :
   
    <!DOCTYPE html>  
    <html>  
    <head>  
     <meta charset="UTF-8">  
     <title>Formulaire D'inscription</title>  
    </head>  
    <body>  
    <form method="post" action="index.php">  
     <label for="name">name</label>  
     <input type="text" name="name" id="name" required placeholder="Name" pattern="^[a-zA-Z][a-zA-Z]{1,80}$">  
     <label for="pseudo">pseudo</label>  
     <input type="text" name="pseudo" id="pseudo" required placeholder="Pseudo">  
     <label for="email">email</label>  
     <input type="email" name="email" id="email" required placeholder="Email">  
     <label for="passord">password</label>  
     <input type="password" name="password" id="password" required placeholder="Password">  
     <button type="submit" name="inscription">Submit</button>  
    </form>

L'extension _PHP Data Objects_ (PDO) définit une excellente interface pour accéder à une base de données depuis PHP. Chaque pilote de base de données implémenté dans l'interface PDO peut utiliser des fonctionnalités spécifiques de chacune des bases de données en utilisant des extensions de fonctions. Notez que vous ne pouvez exécuter aucune fonction de base de données en utilisant l'extension PDO par elle-même ; vous devez utiliser un [driver PDO spécifique à la base de données](https://www.php.net/manual/fr/pdo.drivers.php) pour accéder au serveur de base de données.

Exemple de réception de donnée avec la méthode POST  avec ajout des données en base avec PDO:

    if(isset($_POST['add'])) { try{  
	    $title = $_POST['title'];  
	    $content = $_POST['content'];  
	    $author = $_POST['author'];  
	    $date_rec = time(); //date('d.m.Y h')  
	    $queryInsert = "INSERT INTO story (title, content, author, date_rec) VALUES (:title, :content, :author, :date_rec)"; $stm = $pdo->prepare($queryInsert); $stm->bindValue(':title', $title, PDO::PARAM_STR);  
    $stm->bindValue(':content', $content, PDO::PARAM_STR);  
    $stm->bindValue(':author', $author, PDO::PARAM_STR);  
    $stm->bindValue(':date_rec', $date_rec, PDO::PARAM_INT); $stm->execute();  
    } catch ( Exception $e ) {  
    echo "Cannot insert data ! | " . $e->getMessage( ) . "<br>" . PHP_EOL;  
    }

Laurent TOULOUSE
Florent BELLENGER
