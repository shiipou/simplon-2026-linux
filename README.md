# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

# Sommaire
- [pwd](#pwd)
- [grep](#grep)


## Commandes Linux

### pwd

Cette commande linux fait ........

#### hfjkdghk
kjhfdklgf:

### grep

Cette commande linux permet de rechercher des occurences dans des fichiers et renvoie chaques lignes des fichiers contenant ces occurences.

#### Options d'utilisation

Voici une liste des options essentielles utilisables avec la commade grep :

> [!important]
> -i : permet d'ignorer la casse.
> -v : permet de rechercher les lignes SANS l'occurence.
> -n : permet d'afficher les numéros de lignes.
> -c : permet de compter les lignes.
> -r : permet d'effectuer une recherche récursive.
> -l : permet d'afficher uniquement le nom des fichiers dans lesquels l'occurence est présente.

Voici une liste de quelques options avancées utilisables avec grep :

> [!Pour aller plus loin]-
> -w : permet d'utiliser le mot entier uniquement.
> -o : permet d'afficher uniquement la correspondance.
> -A x : permet d'afficher x lignes après chaque occurence.
> -B x : permet d'afficher x lignes avant chaque occurence.
> -C x : permet d'afficher x lignes avant et après chaque occurence.


#### Exemples d'utilisation

> [!example]
> grep toto texte1 texte2

Dans cet exemple, on recherche le texte "toto" dans les fichiers texte1 et texte2.


> [example]
> grep toto -C 3 toto texte1

Ici, on recherche les 3 lignes avant et après le texte "toto" dans le fichier texte1.

#### Sources

Pour plus d'informations, voici une source détaillant la commande grep : https://blog.stephane-robert.info/docs/admin-serveurs/linux/grep/

