# simplon-2026-linux
"Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026


# Sommaire 
-[kill](#kill)
- [ls] (#ls)
- [pwd](#pwd)
- [cd](#cd)
- [ping](#ping)
- [top | htop](#top | htop)

## Commande Linux

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



### pwd

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



###top | htop

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

