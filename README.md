# simplon-2026-linux
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
