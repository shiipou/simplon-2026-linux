# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

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




# Sommaire
- [pwd](#pwd)
- [cd](#cd)
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


