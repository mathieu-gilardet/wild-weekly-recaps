## RECAP PHP

Le PHP :
Langage le plus utilisé actuellement pour le développement web
Permet de créer des pages web dynamiques couplées à un
serveur HTTP
Un script PHP peut s'exécuter de différentes manières
Directement dans un terminal en mode CLI (Command Line Interface)

 1. la commande php interprète directement le script
 2. la sortie (affichage) se fait dans le terminal

À l’aide d’un serveur web :
Interne : serveur web interne de PHP, utilisé pendant la phase de développement
(se lance aussi via la CLI).

Externe (Apache, Nginx). Utilisé principalement pour la production
Le serveur HTTP Interne de PHP se lance dans le terminal via
$ cd myProject
$ php -S localhost:8000 -t public
Cela va exécuter les scripts dans le dossier public du projet myProject
Le nom public est donné par convention au dossier contenant les script PHP que l’utilisateur
pourra appeler publiquement depuis son navigateur
Puis ouvrir son navigateur avec l’adresse http://localhost:8000/myScript.php.

Une **variable** permet de stocker des valeurs,des données de plusieurs type différents *(int,float,boolean,string,array,object)*  
Il faut bien les nommer de préférence en **anglais** et de type **camelCase** (rajouter chaque majuscule si la variable contient plusieurs mots, car il faut éviter les caractères spéciaux et les espace dans les variables).

Une fonction exécute ce qu'il y a dans la fonction, énormément de fonctions existent déjà (comme count();, sort();) mais on peut aussi les créer.
Créer ses propres fonctions
<? php <br>
function myFunction($param1, $param2)   <br>
{   <br>
  //Some code here using $param1 and $param2   <br>
} <br>
myFunction($varA, $varB);              <br> <br> 
1: appeler la fonction.  <br>
2: lui donner un nom.      <br>
3: définir les types et les paramétrés.   <br>
3: définir le type en sorti.    <br>
4: effectuer le retour dans la fonction.   <br>
5: afficher le résultat de la fonction avec les variables. <br><br>

Conditions  
if else, permet de tester si une condtion est respectée ou non.<br>Nous pouvons combiner un certains nombre de conditions avec if elseif else ....  <br>
Si la condition1 est respectée, elle renvoit "instruction1", sinon on teste la condition2  <br>
Si la condition2 est respectée, elle renvoit "instruction2"  <br>
Sinon elle renvoit enfin le dernier test "instruction3"<?php  <br>
// 3 cas de figure  <br>
if(condition1) {  <br>
// instruction1;  <br>
}  <br>
elseif (Condition2){  <br>
// instruction2;  <br>
}  <br>
else {  <br>
// instruction3;  <br>
}  <br>
?><br>signe  | exemple |  retourne TRUE si :  

    == (égal) $a == $b $a est égal à $b  
    === (identique)  $a === $b  $a est égal et du même type que $b  
    != (différent)  $a != $b  $a est différent de $b  
    <> (différent) $a <> $b $a est différent de $b  
    < (inférieur)  $a < $b  $a est inférieur à $b  
    > (supérieur)  $a > $b  $a est supérieur à $b  
    <= (inférieur ou égal)  $a <= $b <br>$a est inférieur ou égal à $b  
    >= (supérieur ou égal)  $a >= $b<br> $a est supérieur ou égal à $b

