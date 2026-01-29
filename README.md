# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026


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
- [cat](#cat)
- [cd](#cd)
- [ping](#ping)


## Commandes Linux

### pwd


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


