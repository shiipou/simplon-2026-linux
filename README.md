# simplon-2026-linux
Cheatsheet sur les commandes Linux écrite par la promo CDA Niort de 2026

# Sommaire
- [mv](#mv)


## Commandes Linux
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

Elle déplace le fichier test vers le répertoire dir1. Ainsi, le premier argument de mv est la source et le second est la destination.

2 Renommer les fichiers :
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
