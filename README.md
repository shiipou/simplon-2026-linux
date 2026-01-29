# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

# Sommaire

## Commandes Linux

- [pwd](#pwd)
- [ping](#ping)
- [chown] (#chown)

### chown

Cela sert à le propriétaire et le groupe d'un fichier

#### Commandes utiles

chown (nouveau proprietaire) fichier/dossier
chown (nouveau proprietaire):(nouveau groupe proprietaire) fichier/dossier
chown :(nouveau groupe proprietaire) fichier/dossier

exemple :

chown newowner:newownergroupe readme.md

### pwd

Cette commande linux affiche le chemin absolu de votre emplacement actuel dans le systeme de fichier.
elle confirme votre position et d'éviter les erreures de chemin et d'éxecuter des scripts de manière fiable.
pwd signifie "imprimer le répertoire de travail.

### ping

Cette commande linux est un test entre votre ordinateur et l'hote cible qui permettra de le determiner:

-statut de l'hote cible : s'il est joignable
-Mesure du temps entre le trajet aller-retour (Hote-Ordinateur-Hote)
-Pourcentage de paquets perdus

