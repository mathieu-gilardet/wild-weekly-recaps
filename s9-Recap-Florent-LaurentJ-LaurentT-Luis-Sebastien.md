RECAP SEMAINE 10
###################################################################################################
#LES SERVICES :
DRY
Les Controllers gèrent exclusivement les Requests et les Responses.
Le traitement intermédiaire pouvant être réutilisé doit être délégué
à des classes tierces : les services.
=> on factorise son code.
Testable
Les services sont regroupés par thématique métier en respectant
le principe SOLID.
De fait ces classes sont testables unitairement (indépendamment
du contexte dans lequel elles sont utilisées puisqu’isolées du
Controller).
En savoir plus sur le principe S.O.L.I.DQu’est-ce que c’est ?
Un service n’est rien de plus qu’une classe.
Pour qu’une classe soit considérée comme service, il faut qu’elle soit
injectée dans le conteneur de service (Service Container).
Cette injection est faite de manière automatique (si vous n’avez pas
modifié la configuration de base). Vous n’avez rien à faire de particulier.
Il suffit que la classe se trouve dans le dossier src (selon la configuration
de config/services.yaml)
Exemple d’utilisation :
Je peux définir un service Mailer qui me permettra d’envoyer des mails
depuis n’importe quel Controller de mon application sans duplication de
code.Le Service Container
À quoi ça sert ?
Le conteneur de services :
● Centralise l’ensemble des services,
● Les références par leurs noms,
● Gère les dépendances de chacun,
● Lazy Loading : le service n’est instancié qu’au moment de son
utilisation, Puis, c’est la même instance qui sera renvoyée à chaque
demande.

#Créer ses propres services :

De quoi a t’on besoin pour créer un service ?
● Une classe
(logiquement dans le dossier src/Service même si toute classe dans le
dossier src/ est considérée comme un service...)
● Éventuellement des paramètres au __construct() pour toute injection (par ex,
pour l’utilisation du service Mailer).
● Des méthodes de classe qui seront les fonctionnalités du service.


Le but est de bien organiser et factoriser son code métier et identifier quel code peut être considéré et utilisé comme service.
Grâce au typage (type-hint) du paramètre, Symfony reconnaît que nous requérons un objet de type
MyAwesomeService, il recherche dans le service container un tel service (référencé par son FQCN) et
l’injecte automatiquement.

Toute classe est un service référencé dans le service container par son nom pleinement qualifié (FQCN).

Grâce au typage (type-hint) du paramètre, Symfony reconnaît que nous requérons un objet de type MyAwesomeService, il recherche dans 
le service container un tel service (référencé par son FQCN) et l’injecte automatiquement.

#Quelques détails ...
Afin d’assurer la compatibilité avec les anciennes versions et de donner une souplesse de
paramétrage, la configuration des services s’articule autour de 3 principes :

1. autowire (true)
Injection automatique des dépendances, vous pouvez utiliser vos services dans vos
classes uniquement grâce au type (type-hint)

2. autoconfigure (true)
Les services n’ont plus besoin d’être configurés car ils sont enregistrés par leur nom
pleinement qualifié. Le typage prend alors encore plus d’importance.

3. public (false)
Vous ne pouvez pas accéder directement aux services depuis le conteneur de service
(mais via le typage de vos paramètres).

Plus de détails :
Fichier de configuration :
config/services.yamlLes services

Configuration parameters:
locale: 'en'
config/services.yaml

services:
_defaults:
autowire: true #injection de dépendances automatiques
autoconfigure: true #enregistre automatiquement les services comme commande
public: false #optimise le container de services en rendant les services privés
# indique au container où trouver les services
App\:
resource: '../src/*'
exclude: '../src/{Entity,Migrations,Tests,Kernel.php}'
App\Controller\:
resource: '../src/Controller'
tags: ['controller.service_arguments']


#Déclaration automatique vs manuelle

● Comme nous l’avons déjà vu, Symfony déclare automatiquement les
services.

● Que se passe-t-il si vous souhaitez passer des paramètres spécifiques à un service ?
➙ Il suffit de déclarer manuellement le service dans services.yaml
(overriding).

●Vous n’êtes pas obligé de re-déclarer tous les arguments du service. Vous pouvez vous limiter à l’argument spécifique. Les autres resteront gérés grâce
à l’autowire. 

Déclaration manuelle
class MyService
src/Service/MyService.php
{
private $service;
private $parameter;
private $value;
public function __construct(MyService2 $service, string $parameter, string $value)
{
$this->service = $service;
$this->parameter = $parameter;
$this->value = $value;
// ...
}
}Les services
config/services.yaml
Déclaration manuelle
Configuration
parameters:
admin_email: manager@example.com
Il est possible de passer en paramètres :
● Des valeurs (booléens, strings,
nombres, etc.),
● Des paramètres d’application,
encadrés de signes « % »,
● Des services, précédés d'une
arobase.
services:
App\Service\MyService:
arguments:
$service: '@App\Service\MyService2'
$parameter: '%admin_email%'
$value: 'superadmin@example.com'


#~Symfony emporte de nombreux services, pour les retrouver :
$ php bin/console debug:container
Pour filtrer les services disponibles pour l’autowiring et le type-hint :
$ php bin/console debug:container --types
$ php bin/console debug:autowiring
Symfony Container Services
==========================
------------------------------------------------- -----------------------------------------------------
Service ID
Class name
------------------------------------------------- -----------------------------------------------------
App\Controller\DefaultController					App\Controller\DefaultController
App\Service\Service1								App\Service\Service1
App\Service\MyService2								App\Service\Service2
Doctrine\Common\Annotations\cached_reader			alias for "annotations.cached_reader"
Doctrine\Common\Persistence\ManagerRegistry			alias for "doctrine"
Doctrine\DBAL\default_connection					alias for "doctrine.dbal.default_connection"
Doctrine\DBAL\Driver\default_connection				alias for "doctrine.dbal.default_connection"
Doctrine\ORM\EntityManagerInterface					alias for "doctrine.orm.default_entity_manager"
Psr\Container\ContainerInterface					alias for "service_container"

