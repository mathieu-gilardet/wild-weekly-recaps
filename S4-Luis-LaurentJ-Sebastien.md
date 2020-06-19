-> PHP POO :

La Programmation orientée objet (POO) tourne autour de la notion d'objet, PHP inclut le POO.

Objectifs de la POO :
- Meilleure réutilisabilité du code,
- Meilleure testabilité,
- Encourage le travail collectif.

Un objet va permettre de décrire un concept un peu plus large que les variables de PHP. En effet,
avec les entiers, les chaines de caractère et les tableaux on se retrouve trop souvent limité.

Un objet

-Héritage :

Le polymorphisme est lié à l'héritage, on peut redéfinir une méthode dans une classe fille pour
adapter son comportement. Le mot clé final permet d’empêcher l’héritage.

-Namespaces:

C’est un concept abstrait qui permet d’organiser ses classes;

La plupart du temps, les namespaces correspondent à l’arborescence des dossiers de l’application
mais ça n’est pas obligatoirement le cas.

Permettent d'encapsuler des éléments, Évite les collisions de noms, Permet de faire des alias.

PDO (PHP Database Object) est une couche d’abstraction fonctionnant avec plusieurs bases de données,
disponible depuis PHP 5.1. Mêmes classes et méthodes utilisées, quelle que soit le SGBD (MySQL, PostgreSQL, Oracle...)

Sans rendre le SQL 100% compatible avec tous les SGBD, il simplifie grandement la migration lorsque
celle-ci est nécessaire. Bonne pratique : Les données sensibles de connexion sont à mettre dans un fichier séparé, non versionné,
qui sera inclus là où les identifiants sont nécessaires.
