### COLLECTIONS JAVA

Savoir quelle type de collection utiliser en fonction de ses besoins. 

#### 1. List : 
**ArrayList** résout le problème du tableau statique dans Java: la taille du tableau ne peut augmenter une fois qu’il est créée. Lorsqu’un tableau est créé à l’aide de **ArrayList**, un tableau dynamique est créé et on peut augmenter et réduire sa taille si nécessaire. La classe **ArrayList** hérite de l’interface **List**.

 - **ArrayList** : Se classe par ordre d'insertion avec des index. Il est possible d'utiliser les interfaces Comparable & Comparator.  
`ArrayList<Food> lunch = new ArrayList<>();`
`ArrayList<Integer> integers = new ArrayList<>();`

#### 2. Set 
- **HashSet** : Sans ordre défini  
`HashSet<Food> lunch = new HashSet<>();`
- **LinkedHashSet** : Tri par ordre d'insertion  
`LinkedHashSet<Food> lunch = new LinkedHashSet<>();`
- **TreeSet** : Tri par ordre de valeur (Comparable / Comparator)  
`TreeSet<Food> lunch = new TreeSet<>();`
	
#### 3. Map
- HashMap : Sans ordre défini  
`Map<User, Computer> classroom = new HashMap<>();`
- LinkedHashMap : Tri par ordre d'insertion  
`Map<User, Computer> linkedClassroom = new LinkedHashMap<>();`
- TreeMap :  Tri par ordre de valeur des clés (Comparable / Comparator)
`Map<User, Computer> treeClassroom = new TreeMap<>(optionnel : comparator);`

### MAVEN / SPRING 
**Spring** : Facilite / automatise la configuration d'un projet afin de pouvoir se focaliser sur la logique métier.

**Maven** : 
-   d'automatiser certaines tâches : compilation, tests unitaires et déploiement...
-   de gérer des dépendances vis-à-vis des bibliothèques nécessaires au projet  
-   de générer des documentations concernant le projet

### BDD / MERISE / SQL 
**BDD** : Permet de stocker et de retrouver l'intégralité des données, de manière structurée et organisée, et de les modifier et réutiliser facilement.
**NoSQL** : va contenir toutes les informations qui la concerne.
**SQL** (Structured Query Language) : ne va avoir que les informations qui la concerne directement. Elle sera ensuite mise en relation avec des informations périphériques.
	- create database : 
	`mysql> CREATE DATABASE wild;`
	- create table :
	`mysql> CREATE TABLE student
    (
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,  
    firstname VARCHAR(100),  
    lastname VARCHAR(150),
    birthday DATE,
    address TEXT
    );`
	- insert into : `mysql> INSERT INTO school (city, capacity)
VALUES ('Orléans', 30);`
	- select : `mysql> SELECT * FROM student;`
	- update & delete : `mysql> UPDATE school SET capacity=24 WHERE city='Orléans';`
	- on a aussi utilisé : count, sum, having, like, join ...
	- Doc SQL:  [sql.sh](https://sql.sh/cours)
	
**MERISE**

- Méthode de conception, de développement et de réalisation de projets  
informatiques  
- Application à la modélisation de BDD  


![Les différents modèles](https://lh3.googleusercontent.com/proxy/HfzvgfR9GZ9EQ8o-QVkZuuk5C89P9dZr23F0HWqajG129yTvdmQeC7Pr8QCwG0FVi3f7p8lP-m54oADr3QW6pGiFNvpOiW5LS4rTsAQ4f0qgyGeJ3yOqGFDCylyOgICqOQ)


