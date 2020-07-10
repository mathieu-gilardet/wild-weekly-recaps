#### Recap de la semaine

#### Qu'est-ce qu'un service ?

Un service est simplement un objet PHP qui remplit une fonction, associé à une configuration.

Cette fonction peut être simple : envoyer des e-mails, vérifier qu'un texte n'est pas un spam, etc. Mais elle peut aussi être bien plus complexe : gérer une base de données (le service Doctrine !), etc.

Un service est donc un objet PHP qui a pour vocation d'être accessible depuis n'importe où dans votre code. Pour chaque fonctionnalité dont vous aurez besoin dans toute votre application, vous pourrez créer un ou plusieurs services (et donc une ou plusieurs classes et leur configuration). Il faut vraiment bien comprendre cela : un service est avant tout une  _simple classe_.

#### Qu'est-ce qu'un formulaire ?

Quoi de plus important sur un site web que les formulaires ? En effet, les formulaires sont l'interface entre vos visiteurs et votre contenu. Chaque annonce, chaque candidature de notre plateforme, etc., tous passent par l'intermédiaire d'un visiteur et d'un formulaire pour exister dans votre base de données.
La vision Symfony sur les formulaires est la suivante : un formulaire se construit sur un objet existant, et son objectif est d'hydrater cet objet.
Hydrater ? Un terme précis pour dire que le formulaire va remplir les attributs de l'objet avec les valeurs entrées par le visiteur. Exemple : Faire`$advert->setAuthor('Alexandre')`,`$advert->setDate(new \Datetime())`, etc., c'est _hydrater_ l'objet`Advert`.
Le formulaire en lui-même n'a donc comme seul objectif que d'hydrater un objet. Ce n'est qu'une fois l'objet hydraté que vous pourrez en faire ce que vous voudrez : enregistrer en base de données dans le cas de notre objet`Advert`, envoyer un e-mail dans le cas d'un objet`Contact`, etc.

Points forts formulaires symfony:

- Un composant objet (réutilisable et maintenable). - Créations et soumissions simplifiées des formulaires. - Form helpers pour gérer la vue (extension Twig). - Validation et gestion des contraintes accrues, notamment par rapport aux entités au préalablement créées.


**Création d'un formulaire symfony :**
symfony console make:form

**Création d'un CRUD symfony :**
symfony console make:crud

**Commande pour trouver les services:**
 symfony console debug:container


**La forme canonique d'une User Story**

Une User Story présente une vision utilisateur autour de 3 axes : rôle, besoin et valeur métier

-   En tant que /Je Veux /Afin de.
    -   **En tant que / rôle, utilisateur**
    -   **Je Veux / besoin, action**
    -   **Afin de / bénéfice, valeur métier**



