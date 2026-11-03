1. Système d’exploitation
Un système d’exploitation est un ensemble de programmes qui sert d’intermédiaire entre le matériel et les applications/utilisateurs. Il gère les ressources de la machine : le processeur (CPU), la mémoire (RAM), les périphériques d’entrée/sortie (disques, clavier, réseau…), les fichiers.

2. Noyau, shell, applications

Le noyau (kernel) est le cœur du système : il gère le matériel, les processus, la mémoire et les pilotes.
Le shell est l’interpréteur de commandes : il fait le lien entre l’utilisateur et le noyau.
Les applications sont les programmes utilisés par l’utilisateur (navigateur, éditeur…).

Les applications doivent obligatoirement passer par le noyau (via les appels système) pour accéder au matériel.

3. Multitâche / multiutilisateur

Multitâche : plusieurs programmes s’exécutent « en même temps » (le noyau partage le temps processeur entre eux).
Multiutilisateur : plusieurs utilisateurs peuvent travailler simultanément sur la même machine, chacun avec son compte, ses fichiers et ses droits.

4. Le 1er janvier 1970
C’est l’« epoch » d’UNIX : une date d’origine choisie par les concepteurs d’UNIX (Bell Labs), proche de la naissance du système. Le temps est ensuite compté en secondes écoulées depuis cette date.

5. Distribution GNU/Linux
Une distribution est un ensemble cohérent : noyau Linux + outils GNU + applications + gestionnaire de paquets + installateur, assemblés et maintenus par une communauté ou une entreprise.

Communautaires : Debian, Fedora (ou Arch, Rocky Linux).
Commerciales : Red Hat Enterprise Linux (RHEL), SUSE Linux Enterprise.

6. « Libre ne veut pas dire gratuit »
« Libre » (free) renvoie à la liberté, pas au prix : un logiciel libre peut être vendu, mais l’acheteur dispose de libertés sur le logiciel. Les quatre libertés de la GPL :

Liberté 0 : exécuter le programme pour n’importe quel usage.
Liberté 1 : étudier son fonctionnement et l’adapter (accès au code source).
Liberté 2 : redistribuer des copies.
Liberté 3 : améliorer le programme et publier ses améliorations.

7. ls -lia /etc /home

Commande : ls
Options : -l, -i, -a
Arguments : /etc et /home
Sans regrouper : ls -l -i -a /etc /home

8. -l vs --list et --
-l est une option courte (un seul tiret, un caractère) ; --list est une option longue (deux tirets, un mot complet). Le double tiret -- seul indique la fin des options : tout ce qui suit est traité comme un argument (ex. rm -- -test).

9. Les invites
$ : session d’un utilisateur ordinaire. # : session de l’administrateur (root).

10. Commandes

a. man 5 passwd
b. man -k clear (ou apropos clear)
c. shutdown -h +15 "Maintenance" (ou shutdown -P +15 "Maintenance")
d. reboot (ou shutdown -r now)
e. !! (ou flèche haut)
f. !ls
g. history -c (à ne pas exécuter pendant le TP)