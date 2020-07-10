RECAP SEMAINE 8
###########################################################################
Le composant Form de Symfony:
(installé par défaut/automatique lors de la création du projet avec un symfony/website-skeleton)
Commande Manuelle :   composer require symfony/form
###########################################################################
Créer des Forms via la console:

php bin/console make:form
|The name of the form class (e.g. TinyChefType):
> CategoryType
|The name of Entity or fully qualified model class name that the
|new form will be bound to (empty for none):
> Category
|

###########################################################################
La classe CategoryType est alors automatiquement créée dans le dossier
src/Form, avec des champs correspondants à l’entité reliée

#1 -Créer un formulaire:

---> La méthode buildForm()
C’est ici que tu vas ajouter tous les champs nécessaires à ton formulaire

---> La méthode configureOptions()
Cette méthode permet d’envoyer des informations (options) au formulaire

---> 'data_class' => Wilder::class
Le plus souvent, un formulaire va travailler avec une entité (Doctrine).Il devra hydrater l’objet lors de
sa soumission

#2 -Le Contrôleur
- La méthode createForm()
Va instancier un form du type demandé (WilderType). Le second paramètre est optionnel. Si il est omis, le
formulaire va travailler avec un array et non un object.
- La méthode handleRequest()
Va reconnaître si le formulaire a été soumis et hydrater l'objet associé dans ce cas
- La méthode isSubmitted()
Nous informe si le form a été soumis.
- La méthode isValid()
Va lancer les validations paramétrées sur le form.
- La méthode createView()
Va retourner un objet FormView. Jusqu’ici le form n’avait aucune notion d’affichage (HTML), uniquement des
éléments, validations etc... Le createView() va permettre d’ajouter les informations nécessaire à
l’affichage (name, id...)

#3 - La vue
Il existe des extensions Twig (préinstallées via le
website/skeleton) pour gérer l’affichage des forms
dans Twig

#4 - Thème de la vue

Il est possible de gérer de la mise en forme automatique pour les formulaires (par formulaire ou de
manière globale)
De manière globale (pour tous les forms de l’application), dans le fichier config/packages/twig.yaml

#5 - L’entité - Validation côté serveur
C’est une entité Doctrine classique dans
laquelle on peut ajouter si nécessaire
des validations pour chaque champ.

###########################################################################

Sécurité:
Symfony embarque également un composant de sécurité.
Cela évite les failles de type CSRF (Cross-Site Request Forgery).
###########################################################################
Les éléments FieldTypes:
Un formulaire est composé de champs (éléments) : Form Types
De base, le type des champs (Field Type) est automatiquement choisi par le composant Form en fonction 
du type de la propriété dans l’entité
###########################################################################
EntityType:
Lorsque le type de la propriété dans l’entité n’est pas une propriété scalaire
mais une relation, il faut paramétrer explicitement le champ dans le formulaire avec un EntityType.
L’EntityType prend en paramètre l’entité avec laquelle il est en relation et le champ de cette dernière 
sur lequel il doit récupérer l’information pour affichage.
Cléfs obligatoires :
. class : l’entité liée
. choice_label : la propriété
de l’entité liée à afficher
Tout le reste est optionnel.
###########################################################################
Imbrication de formulaires:
Il est également possible d’imbriquer un form dans un form. Les éléments de formulaire étendent 
Symfony\Component\Form\AbstractType.
Les formulaires étendent Symfony\Component\Form\AbstractType. La méthode add()du FormBuilder 
attend un AbstractType en second paramètre, on peut donc sans soucis intégrer un form dans un form !
###########################################################################

