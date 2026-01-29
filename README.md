# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

<<<<<<< HEAD
# Sommaire
- [chmod](#chmod)


## Commandes Linux

### chmod
chmod est la commande Linux pour attribuer, changer, modifier ou supprimer les permissions de fichiers et répertoires.

Syntaxe:
- chmod [OPTIONS] MODE fichier
    - OPTIONS: paramètres de la commande
    - MODE: permissions à expliquer soit en octal (texte), soit en décimale (chiffre).
    - fichier: nom du fichier

- Exemples:
    -   U   |   G   |   W   |   COMMAND

        rwx |  rwx  |  rwx  | chmod 777 filename
        rwx |  rwx  |  r-x  | chmod 775 filename
        rwx |  r-x  |  r-x  | chmod 755 filename
        rw- |  rw-  |  r--  | chmod 664 filename
        rw- |  r--  |  r--  | chmod 644 filename

       User | Group | World |

     r = Readable
     w = Writable
     x = Executable
     - = None

        - Owner | Group | Any | All
   Read | 400   | 040   | 004 | 444
   Write| 200   | 020   | 002 | 222
   Exec | 100   | 010   | 001 | 111
   All  | 700   | 070   | 007 | 777
=======
<<<<<<< HEAD
# Sommaire 
-[kill](#kill)

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




=======
# Sommaire
- [pwd](#pwd)
- [ping](#ping)

## Commandes Linux

### pwd

Cette commande linux affiche le chemin absolu de votre emplacement actuel dans le systeme de fichier.
elle confirme votre position et d'éviter les erreures de chemin et d'éxecuter des scripts de manière fiable.
pwd signifie "imprimer le répertoire de travail.

### ping

Cette commande linux est un test entre votre ordinateur et l'hote cible qui permettra de le determiner:

-statut de l'hote cible : s'il est joignable
-Mesure du temps entre le trajet aller-retour (Hote-Ordinateur-Hote)
-Pourcentage de paquets perdus
>>>>>>> b50186960c4a66b9d0b9565a68debdc4670e85d6

>>>>>>> 5bd860f5a85130f94425d9413983d694cf50d98c
