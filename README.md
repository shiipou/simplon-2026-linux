# simplon-2026-linux
<<<<<<< HEAD
# Sommaire
- [man] (#man)

## Commande man
man est une commande UNIX permettant d'accéder aux pages de manuel installées sur le système. La plupart des programmes fournissent une page de manuel les documentant,
lisible donc avec la commande man.


### Utilisation
man s'utilise dans un terminal de la façon suivante : "man nom-de-la-page"

Par exemple, pour obtenir le manuel de la commande man, l'on fera : "man man"

#### Les sections

Les pages de manuel sont réparties dans des sections distinctes:

1.Programmes exécutables ou commandes de l'interpréteur de commandes (shell) ;
2.Appels système (Fonctions fournies par le noyau) ;
3.Appels de bibliothèque (fonctions fournies par des bibliothèques) ;
4.Fichiers spéciaux (situés généralement dans /dev) ;
5.Formats des fichiers et conventions (Par exemple /etc/passwd) ;
6.Jeux ;
7.Divers (y compris les macropaquets et les conventions). Par exemple, man(7), groff(7) ;
8.Commandes de gestion du système (généralement réservées au superutilisateur) ;
9.Interface du noyau Linux.

Les numéros de sections dont souvent spécifiés entre parenthèses après le nom de la page, comme ci-dessus.

Il arrive (rarement) que deux pages de manuel aient le même nom mais soient dans des sections différentes ; c'est le cas de man(1) et man(7) ou de printf(1) et printf(3) par exemple. Il est donc possible de spécifier dans quelle section chercher la page de manuel, en indiquant son numéro juste avant le nom de la page ou en spécifiant le paramètre -s.
Par exemple, pour obtenir la page de manuel de man(7) (qui parle de la syntaxe des pages de manuel), l'on fera :

"man 7 man"

#### Source

https://doc.ubuntu-fr.org/man


Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026
=======
"Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

# Sommaire
- [mv](#mv)
- [kill](#kill)
- [ls](#ls)
- [pwd](#pwd)
- [cd](#cd)
- [ping](#ping)
- [top | htop](#top | htop)
- [chown] (#chown)
- [cat] (#cat)


## Commande Linux
La commande Linux mv nous permet d'effectuer de nombreuses opérations sur les fichiers comme déplacer des fichiers, les renommer, créer des sauvegardes, etc. 
Bien qu'il n'autorise qu'un nombre limité d'options, nous pouvons combiner mv avec de nombreuses commandes de terminal Linux comme la commande find et créer des combinaisons de commandes plus complexes.  
### mv
1 Déplacer des fichiers directement :
Cette commande linux permet de déplacer et/ou renommer des fichiers dans les distributions linux et BSD.
Mv copie le fichier source dans le répertoire et supprime la source de son emplacement précédent.
Exemple
 mkdir Test && cd Test/ && mkdir dir1 && touch test
$ tree
$ mv test dir1/
 Renommer les fichiers :
Lorsque vous utilisez mv sur deux fichiers résidant sur le même système de fichiers Linux, cela entraînera une opération de renommage de fichier.
Exemple
$ cd dir1
$ mv test TEST
Vérifier avec Tree si aucun fichier s'appelle Test.

3 Empêcherl'écrasement des fichiers :
Par défaut, mv écrasera tous les fichiers portant le même nom dans le répertoire de destination. Vous pouvez le vérifier en utilisant les commandes ci-dessous.
Exemple
$ cp TEST dir1
$ mv TEST dir1/TEST
$ tree
Cependant, nous pouvons facilement empêcher un tel écrasement en utilisant l'option -n, comme démontré dans l'exemple ci-dessous.
Exemple
$ cp dir1/TEST .
$ mv -n TEST dir1/TEST
$ tree

4 Activer le mode intéractif lors de l'écrasement de fichiers :
Vous pouvez également définir le mode interactif dans mv, ce qui entraîne une invite vous demandant si vous souhaitez ou non écraser le fichier de destination. Bien qu’utile pour les utilisateurs débutants, il va de soi que cela arrêtera vos scripts d’automatisation.
Exemple
$ mv -i TEST dir1/TEST
mv: overwrite 'dir1/TEST'?
Tapez simplement y ou n dans l'invite ci-dessus pour activer/désactiver l'écrasement des fichiers.

5 Créer des sauvegardes avant d'écraser des fichers
mv nous permet de sauvegarder nos fichiers de destination
Exemple
$ mv --backup TEST dir1/TEST
$ tree
Le résultat de la commande tree montre que le fichier source a été déplacé avec succès et qu'il existe un fichier supplémentaire appelé TEST~ dans le répertoire de destination. Il s'agit de la sauvegarde du fichier précédent. Utilisez toujours cette option lorsque vous n'êtes pas sûr du répertoire de destination exact ou des fichiers associés.

6 Définir un suffixe personnalisé pour les fichiers de sauvegarde 
Comme nous l'avons déjà vu, mv utilise le symbole ~ comme suffixe de sauvegarde par défaut. Cependant, nous pouvons changer cela en n'importe quoi d'autre en utilisant l'option -S. L'exemple ci-dessous illustre cela en utilisant un nouveau suffixe de sauvegarde .BKP.
Exemple
$ mv -S .BKP TEST dir1
$ mv --suffix=.BKP TEST dir1

7 Mettre à jour le fichier de destination :
La commande Linux mv nous permet de mettre à jour les fichiers de destination en fonction de leur disponibilité et de leur horodatage. Dans ce cas, l'opération de déplacement ne réussira que si le fichier source est plus récent que le fichier de destination ou si le fichier de destination est complètement absent.

$ rm -ri *
$ mkdir dir1 && touch test dir1/test
$ mv -u test dir1/
Tout d’abord, nous avons supprimé tout le contenu de Test/, puis nous l’avons recréé. Je l'ai fait, donc les deux fichiers de test sont créés en même temps et sont donc identiques. Maintenant, lorsque j'essaie de déplacer test vers dir1, le déplacement a échoué et s'est terminé silencieusement. Cela s'est produit puisque mv les a trouvés identiques et en a déduit qu'aucune mise à jour n'était requise.

#### Conclusion :
 Il existe plus de 25 exemples sur linux terminal (cf :https://fr.linux-terminal.com/?p=398)
### kill 

kill envoie un signal TERM ou kill à un processus pour le terminer
Lorsqu'un programme ne répond pas ou qu'il ne peut pas être fermé par quelque moyen que ce soit, la commande kill va permettre de résdoudre ce genre de problème

Pour stopper le processus on peut saisir soit le PID (identifiant du processus); soit le nom binaire du programme : 

ex : 

kill 5339436
    ou 
kill firefox

!!! Attention : avec cette commande, il y à risque d'éffacer accidentellement le travail que vous avez effectué !!! 

 
## la commande ls
la commande ls permet de lister le contenu du répertoire que l'on souhaite (le répertoire courant par defaut), y compris les fichiers et autre répertoires imbriqués

### commande utile
Elle possède de nombreuses options, il peut donc être utile d’obtenir de l’aide en utilisant l’option --help. Cette option renvoie toutes les options que vous pouvez utiliser avec ls.
Par exemple, pour coloriser la sortie de la commande ls, on peut utiliser ls --color=auto, la sortie de la commande ls est colorisée,
 et on peut apprécier la différence entre un répertoire et un fichier.


#### commande associer 
Mais saisir ls avec le flag color serait inefficace ; c’est pourquoi nous utilisons la commande alias.
Elle permet de définir des alias temporaires dans votre session shell.
En créant un alias, vous demandez à votre shell de remplacer un mot par une série de commandes.
Par exemple, pour que ls ait une couleur sans avoir à taper le flag --color à chaque fois, on peut utiliser : alias ls="ls --color=auto"


### chown

Cela sert à le propriétaire et le groupe d'un fichier

#### Commandes utiles

chown (nouveau proprietaire) fichier/dossier
chown (nouveau proprietaire):(nouveau groupe proprietaire) fichier/dossier
chown :(nouveau groupe proprietaire) fichier/dossier

exemple :

chown newowner:newownergroupe readme.md
>>>>>>> a87b0fa70a44d3c015093eeec9e53f531f1319a4

Elle déplace le fichier test vers le répertoire dir1. Ainsi, le premier argument de mv est la source et le second est la destination.


### cat
The cat command stands for "concatenante" and is primarily used to read, display, and concatenate text fles. 

#### Basic syntax
The basic syntax of the cat command is straightforward :
cat [OPTION] [FILE]
	- [OPTION]... refers to the various options you con use with cat to modifiy its behavior.
	- [FILE]... represents one or more files you want to display or concatenate. 
### Example
To display the content of a single file, you can use:
cat filename.txt

To concatenate multiple files into a single output, you can use:
cat file1.txt file2.txt > combined.txt

In this example, the content of file1.txt and file2.txt is combined and redirected into combined.txt.
### Advanced Cat Command Options

Option	Description
-A	Show all characters, including non-printing characters and line endings.
-b	Number non-blank output lines.
-e	Equivalent to -vE, shows non-printing characters and ends lines with $.
-E	Display $ at the end of each line.
-n	Number all output lines.
-s	Squeeze multiple adjacent blank lines into a single blank line.
-T	Display tab characters as ^I.
-v	Show non-printing characters, except for tabs and end-of-line characters.

Cette commande linux affiche le chemin absolu de votre emplacement actuel dans le systeme de fichier.
elle confirme votre position et d'éviter les erreures de chemin et d'éxecuter des scripts de manière fiable.
pwd signifie "imprimer le répertoire de travail.

### ping

Cette commande linux est un test entre votre ordinateur et l'hote cible qui permettra de le determiner:

-statut de l'hote cible : s'il est joignable
-Mesure du temps entre le trajet aller-retour (Hote-Ordinateur-Hote)
-Pourcentage de paquets perdus


### cd
La commande `cd`sous Linux signifie "changer de répertoire" et sert à naviguer entre les répertoires du système de fichiers. C'est l'une des commandes les plus fondamentales et les plus fréquemment utilisées dans le terminal.
Exemples d'utilisation clés :

- `cd ~` or `cd` : Retourne au répertoire personnel de l'utilisateur
- `cd /` : Passe au répertoire racine
- `cd ..` : Passe au répertoire parent
- `cd -` : Revient au répertoire précédent
- `cd directory name` : Navigue vers un sous-répertoire à l'aide d'un chemin relatif
- `cd /full/path/to/directory` : Utilise un chemin absolu pour accéder à un emplacement spécifique

Special Symbols :
- `.` : Fait référence au répertoire actuel (exemple `cd.` ne fait rien
- `..`: Fait référence au répertoire parent
- `~` : Représente le répertoire d'accueil
- `-` : Passe au répertoire de travail précédent

> [!TIP]
> Utilisez les guillemets ("Dir Name") ou des bachslahes (Dir\ Name) pour gérer les répertoires contenant des espaces
> Appuyez sur la touche `Tab` pour compléter automatiquement les noms de répertoires
> Utilisez [`pwd`](#pwd) pour confirmer votre répertoire actuel


##top | htop

la commande **top** permet d'afficher les processus Linux en cours d'execution.
On appelle processus l'execution d'un programme. **top** va donc vous fournir une vue dynamique en temps réel du système en cours d'execution. 

``` 
top - 10:28:53 up 40 min,  1 user,  load average: 0.00, 0.00, 0.00
Tasks:  23 total,   1 running,  22 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.1 sy,  0.0 ni, 99.9 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :  15993.2 total,  15549.3 free,    500.9 used,    135.9 buff/cache
MiB Swap:   4096.0 total,   4096.0 free,      0.0 used.  15492.3 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
      1 root      20   0   21656  12628   9428 S   0.0   0.1   0:01.57 systemd
      2 root      20   0    3120   1920   1920 S   0.0   0.0   0:00.01 init-systemd(Ub
      6 root      20   0    3120   1792   1792 S   0.0   0.0   0:00.00 init
     44 root      19  -1   50352  15744  14848 S   0.0   0.1   0:00.45 systemd-journal
     98 root      20   0   25532   6784   4992 S   0.0   0.0   0:00.14 systemd-udevd
    107 systemd+  20   0   21456  12672  10624 S   0.0   0.1   0:00.13 systemd-resolve
    108 systemd+  20   0   91024   7808   6912 S   0.0   0.0   0:00.11 systemd-timesyn
    155 root      20   0    4236   2560   2432 S   0.0   0.0   0:00.01 cron
    156 message+  20   0    9648   4992   4480 S   0.0   0.0   0:00.13 dbus-daemon
    178 root      20   0   17960   8192   7424 S   0.0   0.1   0:00.09 systemd-logind
    181 root      20   0 1755840  12672  10624 S   0.0   0.1   0:00.34 wsl-pro-service
    187 root      20   0    3160   2048   1920 S   0.0   0.0   0:00.01 agetty
    202 syslog    20   0  222508   5632   4480 S   0.0   0.0   0:00.11 rsyslogd
    211 root      20   0    3116   1920   1792 S   0.0   0.0   0:00.00 agetty
```


Là où top affiche une liste statique rafraîchie périodiquement, **htop** propose une expérience interactive morderne.
vous pouvez naviguer avec les flèches ou la souris, filtrer en temps réel, trier par n’importe quelle colonne et agir directement sur les processus sans quitter l’interface

####htop vs top : pourquoi htop est mieux?


**Navigation visuelle** : au lieu de taper des commandes cryptiques, vous naviguez avec les flèches et agissez avec les touches de fonction
**Couleurs significatives** : chaque couleur a un sens (vert = processus utilisateur, rouge = kernel, bleu = basse priorité)
**Filtrage instantané** : tapez F4 puis un nom, seuls les processus correspondants s’affichent
**Actions groupées** : marquez plusieurs processus avec Space puis tuez-les tous en une fois avec F9

Attention : top est installé par defaut mais pas htop.
Il faudra utiliser deux commandes pour l'installer:
```
sudo apt update

sudo apt install htop
```


>>>>>>> 704032d5ee8544dd062d08f9c77431e4571df836
