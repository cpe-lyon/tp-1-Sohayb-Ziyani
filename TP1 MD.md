# TP1 - Installation d'Ubuntu Server et prise en main du shell

## Exercice 2 : Manuel

### 1. A l’aide du manuel, identifiez le rôle de la commande which 

Le rôle de la commande `which` est de prendre un ou plusieurs arguments et par la suite, donner le chemin complet de la commande exécutée.

### 2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher le terme option dans la page de manuel de which ? 

Pour rechercher un terme quand on consulte une page du manuel il suffit d'aller dans la page du manuel qu'on veut puis utiliser « /\[mot_recherché\] »

Exemple : man which

/Option

### 3. Comment quitte-t-on le manuel ?

Pour quitter le manuel il suffit simplement d'entrer `q`

### 4. Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la première page de la section 6 ; de quoi parle cette section ?

Après avoir entré `man 6 intro`, cette section parle des jeux et des petits programmes amusants disponibles sur le système

## Navigation dans l'arborescence des fichiers

### 1. Allez dans le dossier /var/log

Pour aller dans le dossier /var/log on utilise la commande `cd /var/log`

### 2. Remontez dans le dossier parent (/var) en utilisant un chemin relatif

Pour remonter dans le dossier parent (/var) en utilisant un chemin relatif on utilise `cd /var` ou `cd ..`

### 3. Retournez dans le dossier personnel

Pour retourner dans le dossier personnel on peut simplement utiliser `cd`

### 4. Revenez au dossier précédent (/var) sans utiliser de chemin 

Pour retourner dans le dossier précèdent sans utiliser de chemin on utilise `cd -`

### 5. Essayez d’accéder au dossier /root; que se passe-t-il ?

Il n'est pas possible d'accéder au dossier /root car nous n'avons pas les permissions

### 6. Essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez

Il est marqué que la commande cd est inconnu car il n'est pas possible de l'exécuter directement
avec la commande sudo, il faut d'abord se connecter en administrateur

### 8. Revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1 ; que se passe-t-il ?

A l'aide de la commande rm il est possible de supprimer Fichier1 mais pas Dossier1 car c'est un fichier

### 9. Quelle commande permet de supprimer un dossier ?

La commande permettant de supprimer un Dossier est rmdir seulement s'il est vide

### 10. Que se passe-t-il quand on applique cette commande à Dossier2 ?

Quand on applique cette commande sur le Dossier2, il n'est pas possible de le supprimer car il n'est pas vide.

### 11. Comment supprimer en une seule commande Dossier2 et son contenu ? 

Il est possible de supprimer le Dossier2 et son contenue avec la
commande `rm --r`

## Commandes importantes :

### 1. Comment supprimer en une seule commande Dossier2 et son contenu ?

La commande pour afficher l'heure est `date`. La commande `time` sert à déterminer le temps d'exécution d'une commande. Exemple : `time date`

### 2. Comment supprimer en une seule commande Dossier2 et son contenu ? 

Les fichiers commençant par un point sont des fichiers masqués

### 3. Où se situe le programme ls ?

La commande ls se situe dans `/usr/bin/ls`

### 4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.

Il n'existe pas d'entrée de manuel pour cette commande

### 5. Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?

La commande qui permet d'afficher les fichiers contenus dans le dossier /bin est `ls`

### 6. Que fait la commande ls .. ? 

Elle permet de lister les fichiers du répertoire dans lequel on se trouve

### 7. Quelle commande donne le chemin complet du dossier courant ?
 
La commande qui donne le chemin complet du dossier courant est `pwd`

### 8. Que fait la commande echo 'bip' > plop exécutée 2 fois ?

Cette commande a permis de créer le fichier plop et d'y inscrire le mot bip

### 9. Que fait la commande echo 'bip' >> plop exécutée 2 fois ?

Cette commande a permis d'ajouter le mot bip dans le fichier plop

### 10. Interprétez le comportement de la commande sleep 10 | echo 'toto' ?

le shell affiche toto et la commande est exécutée pendant 10s

### 11. A quoi sert la commande file ? Essayez la sur des fichiers de types différents

La commande file permet d'avoir des informations sur le type d'un fichier

### 12. Créez un fichier original qui contient la chaîne Hello Toto ! ; créer ensuite un lien lien_phy vers ce fichier avec la commande ln original lien_phy. Modifiez à présent le contenu de original et affichez le contenu de lien_phy : qu’observe-t-on ? Supprimez le fichier original ; quelle conséquence cela a-t-il sur lien_phy ?

On observe que le changement fait sur le fichier original a aussiété effectué sur lien_phy après avoir supprimé le fichier original lien_phy ne bouge pas

### 13. Créez à présent un lien symbolique lien_sym sur lien_phy avec la commande ln -s lien_phy lien_sym. Modifiez le contenu de lien_phy ; quelle conséquence pour lien_sym ? Et inversement ? Supprimez le fichier lien_phy ; quelle conséquence cela a-t-il sur lien_sym ?

En créant un lien symbolique avec lien_phy et apres l'avoir supprimé, lien_sym ne peut plus s'ouvrir et apparait en rouge

### 14. Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?

Les raccourcis qui permettent d'interrompre et reprendre le défilement sont ctrl + s et ctrl + q

### 15. Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.

Pour afficher les 5 premières lignes du fichier il faut mettre `head -5 [nom_fichier]`

Pour afficher les 15 dernières lignes il faut mettre `tail --n 15 [nom_fichier]`

Afficher seulement les lignes de 10 à 20  `tail --n 20 /var/log/syslog | head 10`

### 16. Que fait la commande dmesg | less ?

La commande affiche un caractère en continue

### 17. Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?

Il contient les différents utilisateurs sur le système ainsi que leurs informations

18\)

### 19. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?

La commande qui nous donne tous les utilisateurs ayant un compte sur cette machine est          `wc -l/etc/passwd`

### 20. Combien de pages de manuel comportent le mot-clé conversion dans leur description ?

Avec la commande man -k conversion \| wc -l on peut voir qu'il y a 141 pages comportant le mot-clé

### 21. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine

Pour rechercher tous les fichiers se nommant passwd avec la commande find on peut utiliser find / -iname «passwd»

### 22. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null

find / -iname «passwd» \>\> list_passwd_files.txt pour enregistrer
et pour les erreurs la commande est find / -iname « passwd » 2\>\>
/dev/null

### 24. Utilisez la commande locate pour trouver le fichier history.log.

Le fichier history.log se situe dans /var/log/apt/history.log

### 25. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?

Non, le dossier n'apparait pas car la base de données n'est pas encore à jour

## Exercice 3 ; Découverte de l’éditeur de texte nano

### 1. Copiez le fichier /var/log/syslog dans votre dossier personnel sous le nom log.txt, puis ouvrez-le avec nano

Dans le dossier personnel il faut faire cp /var/log/syslog log.txt
et ensuite nano log.txt

### 2. Remplacez toutes les occurrences du mot kernel par le mot noyau

il faut faire ctrl + \\ et ensuite suivre les instructions sur la console
