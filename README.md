[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8410838&assignment_repo_type=AssignmentRepo)
[TP1 - Installation d'Ubuntu Server et prise en main du shell]{.ul}

[Exercice 2 : Manuel]{.ul}

1\) Le rôle de la commande which est de prendre un ou plusieurs
arguments et par la suite, donner le chemin complet de la commande
exécutée.

2\) Pour rechercher un terme quand on consulte une page du manuel il
suffit d'aller dans la page du manuel qu'on veut puis utiliser
« /\[mot_recherché\] »

Exemple : man which

/Option

3\) Pour quitter le manuel il suffit simplement d'entrer « q »

4\) Après avoir entré « man 6 intro », cette section parle des jeux et
des petits programmes amusants disponibles sur le système

[Navigation dans l'arborescence des fichiers :]{.ul}

1\) Pour aller dans le dossier /var/log on utilise la commande cd
/var/log

2\) Pour remonter dans le dossier parent (/var) en utilisant un chemin
relatif on utilise « cd /var » ou « cd .. »)

3\) Pour retourner dans le dossier personnel on peut simplement utiliser
« cd »

4\) Pour retourner dans le dossier précèdent sans utiliser de chemin on
utilise « cd - »

5\) Il n'est pas possible d'accéder au dossier /root car nous n'avons
pas les permissions

6\) Il est marqué que la commande cd est inconnu car il n'est pas
possible de l'exécuter directement avec la commande sudo, il faut
d'abord se connecter en administrateur

8\) A l'aide de la commande rm il est possible de supprimer Fichier1
mais pas Dossier1 car c'est un fichier

9\) La commande permettant de supprimer un Dossier est rmdir seulement
s'il est vide

10\) Quand on applique cette commande sur le Dossier2, il n'est pas
possible de le supprimer car il n'est pas vide.

11\) Il est possible de supprimer le Dossier2 et son contenue avec la
commande rm --r

[Commandes importantes :]{.ul}

1\) La commande pour afficher l'heure est date. La commande time sert à
déterminer le temps d'exécution d'une commande. Exemple : time date

2\) Les fichiers commençant par un point sont des fichiers masqués

3)La commande ls se situe dans /usr/bin/ls

4)Il n'existe pas d'entrée de manuel pour cette commande

5\) La commande qui permet d'afficher les fichiers contenus dans le
dossier /bin est ls

6\) Elle permet de lister les fichiers du répertoire dans lequel on se
trouve

7\) La commande qui donne le chemin complet du dossier courant est pwd

8\) Cette commande a permis de créer le fichier plop et d'y inscrire le
mot bip

9\) Cette commande a permis d'ajouter le mot bip dans le fichier plop

10\) le shell affiche toto et la commande est exécutée pendant 10s

11\) La commande file permet d'avoir des informations sur le type d'un
fichier

12\) On observe que le changement fait sur le fichier original a aussi
été effectué sur lien_phy après avoir supprimé le fichier original
lien_phy ne bouge pas

13\) En créant un lien symbolique avec lien_phy et apres l'avoir
supprimé, lien_sym ne peut plus s'ouvrir et apparait en rouge

14\) Les raccourcis qui permettent d'interrompre et reprendre le
défilement sont ctrl + s et ctrl + q

15\) Pour afficher les 5 premières lignes du fichier il faut mettre
« head -5 \[nom_fichier\] »

Pour afficher les 15 dernières lignes il faut mettre « tail --n 15
\[nom_fichier\] »

Afficher seulement les lignes de 10 à 20 : « tail --n 20 /var/log/syslog
\| head 10 »

16\) La commande affiche un caractère en continue

17\) Il contient les différents utilisateurs sur le système ainsi que
leurs informations

18\)

19\) La commande qui nous donne tous les utilisateurs ayant un compte
sur cette machine est wc -l/etc/passwd

20\) Avec la commande man -k conversion \| wc -l on peut voir qu'il y a
141 pages comportant le mot-clé

21\) Pour rechercher tous les fichiers se nommant passwd avec la
commande find on peut utiliser find / -iname «passwd»

22\) find / -iname «passwd» \>\> list_passwd_files.txt pour enregistrer
et pour les erreurs la commande est find / -iname « passwd » 2\>\>
/dev/null

24\) Le fichier history.log se situe dans /var/log/apt/history.log

25\) Non, le dossier n'apparait pas car la base de données n'est pas
encore à jour

[Exercice 3]{.ul}

1\) Dans le dossier personnel il faut faire cp /var/log/syslog log.txt
et ensuite nano log.txt

2\) il faut faire ctrl + \\ et ensuite suivre les instructions sur la
console
