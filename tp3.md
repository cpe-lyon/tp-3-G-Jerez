# TP 3 : Admin Linux

**Exercice 1:**  
1. Afin de créer les groupes on va éxecuter la commande ```groupadd nom_groupe``` avec en argument les noms de groupe choisi.
2. Pour créer des utilisateurs avec un dossier personnel on va effectuer la commande ```sudo useradd -m nom_user```. Le ```-m``` permet d'ajouter le répertoire personnel lors de la création.
3. Une commande permettant d'ajouter des utilisateurs à des groupes est ```sudo usermod -a -G nom_groupe nom_user``` en fournissant comme argument groupe et username.
4. Afin de visualiser les membres du groupes on peut effectuer la commande ```cat /etc/group``` qui listera les membres pour tous les groupes. On peut donc affiner la précision avec un 'grep' ou même uniquement utiliser grep avec ```grep -w infra /etc/group```.
5. Afin de faire passer un groupe en prorpiétaire d'un fichier on peut utiliser la commande ```chgrp nom_groupe nom_dossier```.
6. La commande pour changer le groupe primaire d'un utilisateur est ```usermod --gid nom_groupe nom_user```.
7. On va créer les répertoires à l'aide de la commande ```mkdir nom_repertoire``` et pour les droits une fois que l'on a associé le groupe propriétaire du dossier on peut utiliser ```chmod 755 /home/nom_repertoire``` afin d'affilier les droits correspondants à ce groupe.
8. Afin que dans ces dossiers, seuls ceux créant un fichier puisse le renommer et le supprimer, il faudra ajouter un sticky bit.
9. On ne peut pas ouvrir de session en tant qu'Alice car n'ayant pas de mot de passe, la session n'est pas utilisable.
10. Afin d'activer le compte d'alice il suffit de rentrer la commande ```passwd alice``` qui demandera d'inscrire un mot de passe pour le compte d'alice.
11. L'uid d'alice est le 1002 tout comme son gid.
12. La commande permettant de trouver l'utilisateur correspondant à un uid est ```id -nu XXXX``` avec XXXX = à l'uid recherché.
13/14. L'id du groupe dev est le 1002.
15. Lorsque l'on effectue la commande pour retirer charlie du groupe infra, on a retour en console disant ```Removing user charlie from group infra```. Cependant lorsque l'on fait un id, il reste dans le groupe infra car un utilisateur ne peut pas ne pas avoir de groupe de même qu'un utilisateur ne peut être supprimer de son groupe principal.
16. Afin d'ajouter une date d'expiration au compte de dave on peut utiliser la commande ```usermod -e 2023-06-01```

