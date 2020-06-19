## MVC:

Organisation claire du code en 3 modules:

Modèle (Le coeur de l’application : Les entités représentées, 
Couche de persistance des données)

Vue (Présente le modèle à l'utilisateur)

Contrôleur (Gère les interactions avec l’utilisateur , 
Utilisé par de nombreux frameworks)

Modèle (base de données):
Contient les méthodes de manipulations des données :
- Create
- Read
- Update
- Delete

VUE:

- Met en forme les données
- Permet l'interaction avec l’utilisateur
- Le terme “vue” n’est pas à prendre au sens strict
- Aucun traitement

CONTROLEUR:

- Réagit aux actions de l’utilisateur et distribue les réponses
- Met à jour le modèle et/ou la vue
- Ne modifie pas directement les données

L'architecture MVC est une solution puissante et reconnue, adaptée à de
grands projets, permettant de faciliter le développement et l'évolutivité
du code.

## COMPOSER:

C'est un gestionnaire de dépendances
● Comme un gestionnaire de paquet (APT, YUM, ...)
○ Mais c’est orienté projet
○ Ca ne fonctionne pas globalement
● Permet d’automatiser :
○ l’installation, la mise à jour, la suppression de
bibliothèques
○ la configuration de bibliothèques
○ dans le cadre d’une application, un projet
● Résout les dépendances automatiquement et
récursivement

## TWIG:

Twig est un moteur de templates pour le langage de programmation PHP, 
utilisé par défaut par le framework Symfony.

sYNTHAXE :
{{ ... }} : appel à une variable ou une fonction PHP, ou un template Twig parent ({{ parent() }}).
{# ... #} : commentaires.
{% ... %} : commande, comme une affectation, une condition, une boucle ou un bloc HTML.

