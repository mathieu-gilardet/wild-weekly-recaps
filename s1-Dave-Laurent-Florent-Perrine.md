# RECAP 1
​
## Unix
​
Interface principale entre un développeur et sa machine. Elle permet d'effectuer toutes les taches dans le terminal.
​
**Exemples :** 
`-i` => Demande de confirmation des actions  
`- sudo !!` => Rappel la commande précédente en admin  
`- sudo apt update` => mise à jour (de tout)  
`- sudo apt upgrade -y` => upgrade système avec auto confirmation grace au -y 
`- cd~` => retour home  
`- pwd` => vérif de localisation 
`- touch` => création de fichier 
`- cat` => afficher contenu du fichier  
`- wc` => détail d'un fichier ( nbr de lignes , mot etc )  
`ls *.txt` => liste uniquement les éléments avec pour extension .txt  
`rm` => remove  
`-r` => inclut le contenu du dossier (supr)  
`mkdir` => création de dossier éditeur intégré au terminal => nano , vi , `newget` => recuperation de fichier distant type html via une adresse  
`curl` => affiche le fichier distantunzip => décompresse fichier zip  
`head` => afficher les 10 premières ligne d un fichier  
`tail` => afficher les 10 dernières ligne d'un fichier  
`-f` => suivis de log ou fichier  
`grep` => recherche chaine de caractère quelque part  
`-v` => exclus une chaine de caractères  
`&&` => enchaine les commandes uniquement si la précédente à fonctionné
`chmod` => donner des permissions + ou - ajout ou suppression sur les 3 groupes  
`chown`  =>  change le propriétaire du fichier ou dossier
​
​
## Git & Github  
​
Git est un logiciel de gestion de version décentralisé.
Github est un service web d'hébergement et de gestion de développement de logiciel. Facilite le travail collaboratif.
​
**git init :** initialiser un repertoire git  
**git status :** affiche le status des fichiers présents  
**git add :** ajouter le fichier a la stack  
**git commit -m "description du commit :"** créé une sauvegarde de la branche dans git (point d'ancrage)  
**git remote add origin "branche" <branch_url> :** ajoute une remote a la branche  
**git remote set-url "branch" <branch_url> :** donne l'adresse url a la branche  
**git push :** push la sauvegarde git sur github (par exemple)  
**git branch "branch" :** créé une nouvelle branche "branch"  
**git checkout "branch" :** entrer dans la branche "branch"
​
​
## CSS / Responsive
​
 - Choisir les unités CSS adaptées en fonction du besoin
 - Utiliser les _media queries_ pour créer des break-points, pour réaliser des designs _responsive_
 - Utiliser l'approche _mobile-first_
​