# RECAP 2


# PHP basics

Installation de l'environement de travail PHP.

## Les variables et chaines de caractères 

**Une variable** est un conteneur servant à stocker des informations de manière temporaire, comme une chaine de caractères ou un nombre.
En PHP, les variables sont représentées par un signe dollar "$" suivi du nom de la variable.
Les variables sont toujours assignées par valeur.

**Exemple :**
				$var = 42 ;

**Une chaîne de caractères** est une série de caractères, où un caractère est la même chose qu'un octet.
En PHP, La façon la plus simple de spécifier une chaîne de caractères est de l'entourer de guillemets simples ou doubles.


## Les tableaux et les boucles 

**Un tableau** en PHP est en fait une carte ordonnée. Une carte est un type qui associe des _valeurs_ à des _clés_.
Un tableau peut être créé en utilisant la structure de langage [array()] Il prend un nombre illimité de paramètres, chacun séparé par une virgule, sous la forme d'une paire _key => value_.

**Exemple :**
					array(  
					    key  => value,  
					    key2 => value2,  
					    key3 => value3,  
					    ...  
					)
					
**Les boucles** vont nous permettre d’exécuter plusieurs fois un bloc de code, c’est-à-dire d’exécuter un code « en boucle » tant qu’une condition donnée est vérifiée.

Nous disposons de quatre boucles différentes en PHP :

-   La boucle  `while`  (« tant que ») ;
-   La boucle  `do… while`  (« faire… tant que ») ;
-   La boucle  `for`  (« pour ») ;
-   La boucle  `foreach`  (« pour chaque ») ;

## Les conditions et fonctions 

Tous les scripts PHP sont une suite d'instructions. Les expressions évaluées peuvent être plus ou moins complexes, c'est-à-dire qu'elles peuvent être constituées d'une combinaison d'opérateurs de comparaison, d'opérateurs logiques et même de fonctions. Le langage PHP introduit 4 constructions conditionnelles: if, elseif, else et switch.

**Exemple :**
			<?php  
					if ($a > $b)  
					echo "a est plus grand que b";  
			?>

**Une fonction** est un bloc de code PHP destiné généralement à être réutilisé plusieurs fois. Plutôt que d'écrire plusieurs fois le même morceau de code, on met celui-ci dans une fonction, et c'est cette fonction que l'on appellera dès que l'on en aura besoin.  
En PHP, il y a déjà des fonctions prédéfinies que l'on peut utiliser immédiatement. Pour autant, rien ne nous empêche d'en créer d'autres selon nos besoins. Et plus encore, on peut se servir des fonctions PHP pour créer nos propres fonctions.

**Exemple :**
		<?php  
		$animal = "Le pangolin";  
		$item = "la Planète";  
		function writeSecretSentence(string $animal ,string $item) : string  
		{  
		return "$animal s'incline face à $item.";  
		}$writeSecretSentence = writeSecretSentence($animal ,$item);  
		echo $writeSecretSentence;


## Outils de debug

Intallation et utilisation de Xdebug (joli var_dump)

# PHP avancé

## Les formulaires 

En cours de réalisation.



Florent Bellenger, Laurent Toulouse.
