# Exercice 1
Cette exercice ne necessite pas de réponse.

# Excercice 2

## Manuel
### Questions :
1. A l’aide du manuel, identifiez le rôle de la commande which
2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher
le terme option dans la page de manuel de which ?
3. Comment quitte-t-on le manuel ?
4. Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?

### Réponses :
1. La commande which permet de renvoyer le chemin des ficiers qui seraient éxécutés dans l'environnement courant.
2. Il faut réalisé la commande `man nom_de_la_commande | grep mot_a_chercher`, dans l'exemple de la questions : `man which | grep option`. On peut aussi directement chercher le mot dans le manuel en tapant `/mot_a_chercher`
3. Pour quitter le mannuel il faut taper sur la touche `q`.
4.La sections 6 n'existe pas pour la commande whiche.

## Navigation dans l’arborescence des fichiers
### Questions :
1. allez dans le dossier `/var/log`
2. remontez dans le dossier parent (/var) en utilisant un chemin relatif
3. retournez dans le dossier personnel
4. revenez au dossier précédent (/var) sans utiliser de chemin
5. essayez d’accéder au dossier `/root` ; que se passe-t-il ?
6. essayez la commande `sudo cd /root` ; que se passe-t-il ? Expliquez
7. à partir de votre dossier personnel, créez l’arborescence suivante :
8. revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?
9. quelle commande permet de supprimer un dossier ?
10. que se passe-t-il quand on applique cette commande à Dossier2 ?
11. comment supprimer en une seule commande Dossier2 et son contenu ?

### Réponses :
1. Il faut taper `cd /var/log`
2. Il faut taper `cd ..`
3. Il faut taper `cd /home/val/` (ne pas oublier le premier / pour partir de la racines).
4. Il faut utiliser `cd -` (permet de retourner au précédent chemin utilisé).
5. On ne peut pas accéder à /root. Pour cela il faut se mettre un super utilisateur et donc réaliser la commande suivante : `sudo cd /root`
6. Cette commande nous demande de renseigner le mot de passe pour pouvoir accéder au dossier root. Le mot de passe est demandé pour éviter que n'importe qui atteigne ce répertoire.
7. Il faut réliser la série de commande suivante pour réalisé l'arborescence :
: val@serverofvalentin:~$ mkdir Dossier1 <br/>
: val@serverofvalentin:~$ mkdir Dossier2 <br/>
: val@serverofvalentin:~$ cd Dossier1 <br/>
: val@serverofvalentin:~/Dossier1$ touch Fichier1 <br/>
: val@serverofvalentin:~/Dossier1$ cd .. <br/>
: val@serverofvalentin:~$ cd Dossier2 <br/>
: val@serverofvalentin:~/Dossier2$ mkdir Dossier2.1 <br/>
: val@serverofvalentin:~/Dossier2$ mkdir Dossier2.2 <br/>
: val@serverofvalentin:~/Dossier2$ cd Dossier2.2 <br/>
: val@serverofvalentin:~/Dossier2/Dossier2.2$ touch Fichier2 <br/>
: val@serverofvalentin:~/Dossier2/Dossier2.2$ touch Fichier3 <br/>
8. Avec la commande `rm` on peut uniquement supprimer des fichiers.
9. C'est la commande `rm -rf nom_du_dossier` si le dossier est plein (pour tout vider) et `rmdir nom_du_dossier` si le dossier est vide.
10. La commande `rmdir` on ne peut pas supprimer un dossier rempli.
11. Il faut alors utiliser la commande `rm -rf` pour supprimer ce dossier Dossier2.

## Commandes importantes
###Questions : 
1. Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?
2. Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?
3. Où se situe le programme ls ?
4. Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.
5. Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?
6. Que fait la commande ls .. ?
7. Quelle commande donne le chemin complet du dossier courant ?
8. Que fait la commande echo 'yo' > plop exécutée 2 fois ?
9. Que fait la commande echo 'yo' >> plop exécutée 2 fois ?
10. A quoi sert la commande file ? Essayez la sur des fichiers de types différents.
11. Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?
12. Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?
13. Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?
14. Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20.
15. Que fait la commande dmesg | less ?
16. Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?
17. Affichez seulement la première colonne triée par ordre alphabétique inverse
18. Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?
19. Combien de pages de manuel comportent le mot-clé conversion dans leur description ?
20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine
21. Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment
23. Utilisez la commande locate pour trouver le fichier history.log.
24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?

### Réponses :
1. C'est la commande `date` qui permet d'afficher l'heure. La commande `time` permet de déterminer le temps d'exécution d'un processus.
2. La commande `ls` nous affiche uniquement les dossier `Dossier1` et `Dossier2`. La commande `la` nous affiche d'autre fichier. Les fichiers avec un point sont donc visible uniquement avec la commande `la` (ce sont des fichiers cachées).
3. Pour trouver ou se situe la commande `ls` il faut taper `sudo find / -name ls`. On trouve donc les chemins suivants : 
: /usr/lib/klibc/bin/ls <br/>
: /usr/bin/ls <br/>
: /snap/core/7917/bin/ls <br/>                                                                                      
: /snap/core/7917/usr/lib/klibc/bin/ls <br/>
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14. 
15. La commande `dmesg|less` permet d'afficher le buffer du kernel (mémoire tampon). Le `less` permet de parcourir ligne à ligne ce buffer. En effet si on réalise la commange `dmesg` tout seul on a le buffer en entier qui apparaît.
16. Le fichier `/etc/passwd` contient les comptes ainsi que les répertoires associés présent sur la machine. Pour afficher le mannuel il faut réaliser la commande `man passwd`.
17. Il faut réaliser la commande `sort -r /etc/passwd` pour un affichage des colonnes dans l'ordre alphabétique inverse (l'attribut `sort` permet d'affiché les colonnes trié et `-r` permet d'afficher l'inverse de sort).
18. La commande qui nous permet d'avoir le nombre d'utilisateurs ayant un compte sur la machine est la commande `cut -d: -f1 /etc/passwd | wc -l`
19. La commande `man -k conversion | wc -l` nous permet de compter le nombre de pages de manuel comportent le mot conversion dans leur description.
20. Il faut utiliser la commande `sudo find / -name passwd` nous permet d'avoir tout les fichiers (et leur chemin) se nommmant `passwd`.
21. La commande `find / -name passwd 2> /dev/null > ~/list_passwd_files.txt` nous permet d'enregistrer la liste de fichiers trouvés précédement, dans un fichier texte (et les erreur dans le fichier null).
22.
23. Il faut utiliser la commande `locate history.log` pour trouver le fichier history.log (il faut au préalable installer mlocate). On obtient le résultat suivant : `/var/log/apt/history.log`
24. On créer un fichier avec la commande `touch`. Cependant on n'arrive pas à retrouver ce fichier avec la commande `locate`. Un rafraîchissement est nécessaire, pour cela il faut utiliser la commande `updatedb`.
# Exercice 3 :
Cette exercice ne nécessite pas réponses.

# Exercice 4 :
### Questions :
Commencez par créer une copie de ce fichier, que vous appellerez .bashrc_bak
2. Editez le fichier .bashrc avec nano et décommentez la ligne force_color_prompt=yes pour activer
la couleur. Enregistrez le fichier et quittez nano.
3. Le fichier .bashrc est lu au démarrage du shell ; pour le recharger, il faudrait donc se déconnecter
puis se reconnecter ; mais il existe un autre moyen : la commande source .bashrc. Testez-la, l’invite
de commande devrait immédiatement passer en couleurs.
4. Les couleurs par défauts (surtout celle du dossier courant) ne sont pas très visibles. Dans .bashrc,
cherchez les lignes commençant par PS1= ; elles indiquent la mise en forme de l’invite de commande
(selon que l’on est en couleurs ou non).
Sur cette ligne, on peut distinguer un certain nombre de raccourcis :

### Réponses :
3. Une fois `force_color_prompt=yes` décommenté dans le fichier `~/.bashrc` et la commande `source .bashrc`, l'invité de commande passe en couleur verte.
4. Il faut ajouter cette ligne `\e[35m[\A] - ${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;36m\]\w\[\033[00m\]\$PWD`après le "PS1=...".
# Exercice 5 :
Cette exercice ne nécessite pas de réponses.

