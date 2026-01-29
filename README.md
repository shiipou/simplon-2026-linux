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
