# Weekly Recaps

 Synthèse Semaine 4 - Perrine, Sylène, Valentin


# Thème

## JDBC

### JAVA DATAS BASE CONNECTION

Process ;
Connection connection = null;
 PreparedStatement statement = null;
 ResultSet rs = null;
--> Connexion à la source
connection = DriverManager.getConnection(DB_URL, DB_USER, DB_PASSWORD)
 --> Création d’une requête (ou plusieurs) 
--> Exécution de la requête (ou plusieurs) 
--> Traitement des résultats --> Fermeture de la connexion 

Try {"requête(s)"} catch{"récupérer les exceptions"} finally {"closer"}


## Spring IO & DI

### Couplage fort

Rapide à mettre en place
Interdépendance forte
Plus long à maintenir
=> Peu couteux à la réalisation mais couteux à la modification, peu recommandé


### Couplage faible

Long à mettre en place
Interdépendance faible
Plus rapide à maintenir
=> Une classe réalise une action.

### DAO

Interface qui injecte le repository dans le contrôler, et qui permet de traduire des données en instance d'un object, par exemple : traduire un JSON d'une API en object Java.

### Injection de dépendances

Les injections créent dynamiquement les dépendances entre les différents objets, en se basant sur
un fichier de configuration ou une annotation (@Autowired, @Qualified, @Repository,..).

## JS

### FrameWork  

Framework exemple : React(léger), Angular(complet),.. permet la rédaction des lignes de commande du web.  
React se concentre sur la gestion de l'interface utilisateur, 
Les autres briques applicatives, comme le routage côté client, le stockage des données, etc. sont laissées aux innombrables solutions complémentaires de son écosystème.

### Permet de dynamisé le web

Le code **Javascript** sert donc à donner du dynamisme à la page. Sans lui, la page ressemblerai à une page de livre, un peu animée (grâce à un autre langage appelé le CSS), mais qui ne change pas beaucoup.

--> C'est cool!

