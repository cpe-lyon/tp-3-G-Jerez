# TP 3 : Admin Linux

**Exercice 1:**  
1. Afin de créer les groupes on va éxecuter la commande ```groupadd nom_groupe``` avec en argument les noms de groupe choisi.
2. Pour créer des utilisateurs avec un dossier personnel on va effectuer la commande ```sudo useradd -m nom_user```. Le ```-m``` permet d'ajouter le répertoire personnel lors de la création.
3. Une commande permettant d'ajouter des utilisateurs à des groupes est ```sudo usermod -a -G nom_groupe nom_user``` en fournissant comme argument groupe et username.
4. Afin de visualiser les membres du groupes on peut effectuer la commande ```cat /etc/group``` qui listera les membres pour tous les groupes. On peut donc affiner la précision avec un 'grep' ou même uniquement utiliser grep avec ```grep -w infra /etc/group```.
5. Afin de faire passer un groupe en prorpiétaire d'un fichier on peut utiliser la commande ```chgrp nom_groupe nom_dossier```.
6. La commande pour changer le groupe primaire d'un utilisateur est ```usermod --gid nom_groupe nom_user```.
7. On va créer les répertoires à l'aide de la commande ```mkdir nom_repertoire``` et pour les droits une fois que l'on a associé le groupe propriétaire du dossier on peut utiliser ```chmod 755 /home/nom_repertoire``` afin d'affilier les droits correspondants à ce groupe.


