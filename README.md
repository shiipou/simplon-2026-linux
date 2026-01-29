#
simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

##SOMMAIRE

[top | htop](#top | htop)

##COMMANDES LINUX

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
