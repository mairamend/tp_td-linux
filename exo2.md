1. Chemin absolu de linux.txt
/home/groupeA/alice/cours/linux.txt

2. Depuis /home/groupeA/bob
../alice/cours/linux.txt
(.. remonte à groupeA, puis on descend dans alice/cours.)

3. Depuis /home/groupeB/carla/projets/tp1, vers notes de bob
../../../../groupeA/bob/notes
Les quatre .. remontent successivement à projets, carla, groupeB, puis home. On redescend ensuite vers groupeA/bob/notes.

4. Séquence de pwd

(a) cd ../../bob depuis /home/groupeA/alice/cours : on remonte à groupeA, puis on descend dans bob. Résultat : /home/groupeA/bob
(b) cd ../../groupeB/./carla/projets/.. depuis bob : on remonte à home, on descend dans groupeB/carla/projets (le . ne change rien), puis .. remonte d’un cran. Résultat : /home/groupeB/carla
(c) cd / puis cd .. : la racine est son propre parent, donc on reste à la racine. Résultat : /
(d) cd sans argument ramène au répertoire de connexion. Résultat : /home/groupeA/alice

5. Classement

Chemins absolus (commencent par /) : /etc/passwd, /
Chemins relatifs : ../alice, ./script.sh, cours/linux.txt, ..

6. Pourquoi ./script.sh ?
Pour une commande sans /, le shell ne cherche que dans les répertoires listés dans la variable PATH. Le répertoire courant n’en fait pas partie, notamment pour des raisons de sécurité (éviter d’exécuter par erreur un programme piégé déposé dans un dossier). Écrire ./script.sh donne un chemin explicite, donc le shell n’utilise plus PATH.

7. Vérification sur machine

Création de l’arborescence :
    mkdir -p ~/arbo/home/groupeA/alice/cours ~/arbo/home/groupeA/bob/notes ~/arbo/home/groupeB/carla/projets/tp1
    touch ~/arbo/home/groupeA/alice/cours/linux.txt ~/arbo/home/groupeA/alice/monfichier

Vérification de la Q2 :
        cd ~/arbo/home/groupeA/bob
        ls ../alice/cours/linux.txt