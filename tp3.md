# TP 3 : Admin Linux

**Exercice 1:**  
1. Afin de créer les groupes on va éxecuter la commande ```groupadd nom_groupe``` avec en argument les noms de groupe choisi.
2. Pour créer des utilisateurs avec un dossier personnel on va effectuer la commande ```sudo useradd -m nom_user```. Le ```-m``` permet d'ajouter le répertoire personnel lors de la création.
3. Une commande permettant d'ajouter des utilisateurs à des groupes est ```sudo usermod -a -G nom_groupe nom_user``` en fournissant comme argument groupe et username.
4. Afin de visualiser les membres du groupes on peut effectuer la commande ```cat /etc/group``` qui listera les membres pour tous les groupes. On peut donc affiner la précision avec un 'grep' ou même uniquement utiliser grep avec ```grep -w infra /etc/group```.


