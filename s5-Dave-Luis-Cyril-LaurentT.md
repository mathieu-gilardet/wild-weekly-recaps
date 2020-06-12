# RECAP 5


# SIMPLE MVC


- Défini en 1978 par Trygve Reenskaug
- Organisation claire du code en 3 modules
- Modèle
   - Le coeur de l’application : Les entités représentées
   - Couche de persistance des données
- Vue :
     - Présente le modèle à l'utilisateur
- Contrôleur
     - Gère les interactions avec l’utilisateur
- Utilisé par de nombreux frameworks
- PHP (Symfony, Cake, Zend), Python (Django,
Turbogears), Ruby (Rails)

**Exemple Controller:**
				namespace Controller;
				
use Model\CategoryManager;

class CategoryController extends AbstractController
{
public function index()
 {
$categoryManager = new CategoryManager();
$categories =
$categoryManager ->selectAll();
return
$this->twig->render('index.html.twig', [
'categories'=>$categories,
]);
}
}


# GITFLOW

Le workflow **Gitflow** global est le suivant : Une branche de développement ( develop ) est créée à partir de master . Une branche de version ( release ) est créée à partir de develop . Les branches de fonctionnalité ( feature ) sont créées à partir de develop .


# Composer

Composer est un logiciel gestionnaire de dépendances libre écrit en PHP. Il permet à ses utilisateurs de déclarer et d'installer les bibliothèques dont le projet principal a besoin. Le développement a débuté en avril 2011 et a donné lieu à une première version sortie le 1er mars 2012. Développé au début par Nils Adermann et Jordi Boggiano  (qui continuent encore aujourd'hui à le maintenir), le projet est maintenant disponible sur la plateforme GitHub5. Il est ainsi développé par toute une communauté.
Le logiciel Composer est à l’initiative d'un portage en PHP du logiciel Libzypp satsolver d'Open Suse.
Le logiciel Composer est fortement inspiré du logiciel npm pour Node.js et de bundler pour Ruby.
Le dépôt principal de Composer est le site web Packagist10, qui permet notamment la recherche de bibliothèques et leur entreposage centralisé.
Le fichier binaire Composer est distribué sous la forme d'un lanceur, installable après un simple téléchargement.

**Exemple d'ajout de dépendance squizlabs/php_codesniffer :**

En ligne de commande : 
composer require squizlabs/php_codesniffer ^1.0

Ajout dans composer.json :
"require": {
"squizlabs/php_codesniffer": "^1.0"
}

# TWIG

Twig est un moteur de templates pour le langage de programmation PHP, utilisé par défaut par le framework Symfony.

**Quelles sont ses fonctions?**

- Contrôle de flux complexe
- Echappement automatique
- Héritage des templates
- Filtres variables
- Internationalisation (via gettext)
- Macros
- Langage extensible

# Lancement des projets

Mise en place des environnements de travail, outils (IDE / GITHUB), répartition des taches (Trello).......


Dave, Luis, Cyril, Laurent T.
