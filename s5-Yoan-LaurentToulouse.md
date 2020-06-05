## RECAP POO		

POO CEST QUOI ? 
POO Programmation Orientée Objet 
Cela permet une meilleure réutilisabilité du code, une meilleur testabilité et ça encourage le travail collectif 

L'objet est une instance de classe.
Plus précisément, une instance d’une classe est un représentant de celle-ci, qui possède :
- Les propriétés, définies dans la classe, avec des valeurs
propre à chaque objet.
- les méthodes, définies dans la classe, permettant de
récupérer et manipuler les propriétés de l'objet, afin de lui définir un comportement propre.
On instancie un objet grâce au mot clé new.

L’objet (exemple)
Classe : Car
● Couleur
● Nom
● Poids


$this
This est très important !
Le mot-clé $this désigne, dans une classe, l'instance courante de la classe elle-même.
Pour reprendre l’exemple des chats. La classe est unique et les instances
● L’héritage est TRÈS utilisé dans la POO.
● TOUTES les classes peuvent être héritée sauf si une classe définie explicitement le contraire (final)
● En PHP, une classe ne peut étendre qu’une seule autre classe.
$grumpy->rest();
$garfield->rest();
index.php
class Cat {
private $tiredness;
/** * Indicate if the cat is tired
* @return bool */ public function isTired() {
$result = false; if ($this->tiredness > 0) {
$result = true; } return $result; } /** * Reset the tiredness of the cat
*/ public function rest() {
$this->tiredness = 0; } }

Qualified Class Name
On peut même imaginer regrouper plusieurs chats dans la même boîte, la seule règle à respecter est de ne pas mettre de chats portant le même nom dans une même boîte.
Une constante est une valeur qui ne change pas et ne changera JAMAIS.
Elle peut être déclarée dans une classe si nécessaire ou dans un programme si elle est globale à tout le programme.
class Cat {
// Une constante de classe const FAMILY = 'Félin';
public function __toString() {
return $this->name." est un ". self::FAMILY; } }echo Cat::FAMILY; // Affiche Félin
$cat = new Cat(); echo $cat->getFamily(); // Affiche Félin
● Par convention, elles sont en MAJUSCULES.
● Elles sont obligatoirement publiques (si déclarées dans une classe)
● On peut y accéder sans instancier l'objet car elle appartient à la classe (et non à une instance).
● Pour accéder à une constante de classe, on préfixe son nom par le nom de la classe

Méthodes invoquées automatiquement par PHP lorsque certains évènements arrivent pendant l'exécution du code.
Elles ne s'appellent donc pas directement.
Elles démarrent toutes par "__" (double underscore). Voici celles que tu as déjà ou risques d'utiliser :
● __construct() : instanciation d'un objet.
● __toString() : lorsqu'un objet est utilisé comme une chaîne (echo, substr()...)
D’autres méthodes magiques existent : __clone(), __get, __set(),


INTRODUCTION JS : RECUPERATION API UTILISATION FICHIER JSON UTILISATION REACT ...

