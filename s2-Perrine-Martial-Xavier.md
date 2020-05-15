### Synthèse semaine 02:

<h2>Participants: Perrine, Martial, Xavier

<h1>Thème principal: Java:

### Les variables en Java:

Il existe deux grandes familles de type de données :

* Primitives  : byte ,short, int, long, float, double, char, boolean 
	A déclarer dans le bloc dans lequel on en a besoin. 

- Objet:

### Les Tableaux :

Un tableau "simple" est déclaré, par exemple, de cette façon:
	
	String[] weapons = new String[] {"whip", "gun", "saber"};
	ou 
	String[] weapons = {"whip", "gun", "saber"};
	Pour un tableau comprenant des caractères. A mettre entre guillemets pour String.

	int[] chiffres = {1,2,3,4}

Un tableau multidimensionnels:

` weapons = new String[][] {
    weaponsIndiana,
    weaponsHelen,
    weaponsRavenwood
	}; `

### Les boucles:

La boucle for:

`for (int i = 0; i < 10; i++) {
    // Do something
	 }`
	
La boucle "while":

`int i = 0;
while (i < 10) {
    i++
    // Do something
}`

La boucle "for each":

`String[] weapons = {"whip", "gun", "saber"};
for (String weapon : weapons) {
    System.out.println(weapon); // affiche l'arme
}`
	
### Les méthodes:

Une méthode peut être intégrée directement depuis le jdk, ou créé dans une classe. Une méthode est une "fonction" qui appartient à une classe. 

	Arrays.toString() par exemple fais partie du Jdk.

Une méthode créée pourrait ressembler a ceci:

`public String SayHello(){
		System.out.println("Hello");
		}`

### La POO (Programmation Orientée Objet)

Java est un langage typé orienté objet. Un objet peut avoir: une classe, des attributs, un constructeur, des méthodes.  Il peut implémenter une interface ou hériter d'un autre objet c'est à dire récuperer des propriétés ou des "fonctions" définies dans une classe parente dans le cas de l'héritage.

Dans le cas ou les attributs sont définis en "private" les autres classes ont besoin de "getter" et de "setter" pour y accéder (les rappeler). Ce sont les accesseurs et mutateurs.

Pour utiliser un objet qui hérite d'une autre classe, il faut "l'instancier" dans une classe fille.
Cela consiste à "appeler" l'objet voulu, pour pouvoir lui assigner de nouveau paramètres (définis dans la classe parente) pour s'en servir dans une nouvelle classe.
Par exemple:

	`Duck loulou = new Duck("Loulou", 8);
    loulou.nameAndAge();`