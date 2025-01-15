## Chapitre 01:

### 1. Historique et Structure d'Unix :

- Unix est un système d'exploitation multi-utilisateur et multitâche.
- Il est indépendant du matériel, fonctionnant sur différents ordinateurs.
- Unix gère les périphériques, la mémoire, les processeurs, les fichiers et la protection des erreurs.
- Son objectif : permettre le développement d'applications sans se soucier des détails matériels.
---
### 2. Concepts de Base :
- _**Utilisateur**_ :
    - Chaque utilisateur a un _nom d'utilisateur_ et un _mot de passe_.
    - L'accès est sécurisé et chaque utilisateur possède un répertoire personnel.
    - Les utilisateurs peuvent définir les permissions d'accès sur leurs fichiers pour les protéger ou les partager.
- **Processus** :
    - Un processus est un _programme en cours d'exécution_.
    - Chaque processus a un numéro unique (PID) et peut être dans différents états (exécution, attente).
    - Les processus sont organisés en une structure hiérarchique, chaque processus ayant un "parent".
- **Fichier** :
    - Unix utilise une _hiérarchie de fichiers_, où presque tout est représenté comme un fichier.
    - Types de fichiers :
        - _Ordinaires_ (contenant des données ou programmes),
        - _Répertoires_ (organisent les fichiers),
        - _Spéciaux_ (représentent des périphériques),
        - _Liens symboliques_ (références vers d'autres fichiers).
- **Structure générale** :
    Unix est organisé en une arborescence de fichiers avec un répertoire racine (`/`).

    <img src="UNIX Images/image.png" style="border-radius: 7px;" width="400">
    - **Matériel** :
        - Niveau le plus bas, comprenant le processeur, la mémoire, et les périphériques (clavier, écran, etc.).
        - Fonctionne en _langage machine_ propre au processeur.
    - **Noyau (Kernel)** :
        - Partie centrale qui gère les ressources matérielles (fichiers, mémoire, processus, périphériques).
        - Utilise des _appels système_ (comme `open`, `read`, `write`) pour interagir avec les applications.
        - Gère le multitâche, l'accès aux fichiers, la mémoire et les périphériques.
    - **Shell** :
        - Interface entre l'utilisateur et le noyau, permettant d'exécuter des commandes.
        - Fonctionne comme un _langage de script_, utilisé pour automatiser des tâches.
        - Exemples de shells : `sh`, `bash`, `zsh`.
    - **Scripts et Applications** :
        - Scripts : automatiques pour tâches répétitives, écrits en langage shell.
        - Applications : interagissent avec le noyau via des appels système sans passer par le shell.
---
### 3. Connexion et Interfaces :

- Les utilisateurs se connectent via une interface alphanumérique (Xterm) ou graphique (X11).
- L’interface graphique utilise le serveur X pour gérer l’affichage et la communication avec les clients (applications).
- La connexion permet de configurer l’environnement de travail (environnement de bureau, gestionnaire de fenêtres).
---
### 4. Outils de Base :

- **_Xterm_ :** Simulateur de terminal pour entrer des commandes Unix.
- **_Emacs_ :** Éditeur de texte extensible pour programmer et modifier des fichiers.
- **_Autres éditeurs_ :** `Vi`, `Vim`, `Nano`, utilisés pour des modifications simples ou avancées de fichiers texte.
---
### 5. Apprentissage de Unix :

- L'apprentissage est difficile, nécessitant la recherche d'informations dans la documentation (`man` pages) et l'utilisation de divers outils de recherche (`grep`, `find`).
- Unix évolue par accumulation, ce qui peut rendre l’apprentissage redondant et parfois confus pour les débutants.
- La prise en main rapide des commandes de base est nécessaire pour devenir opérationnel efficacement.
---
## Chapitre 02:
### 1. Distributions Linux :

- **Définition** : Systèmes basés sur Linux avec des caractéristiques et outils spécifiques.
- **Exemples** :
    - **Debian** (stable), **Ubuntu** (facile d’utilisation, variantes KDE/Xfce), **Fedora** (basée sur Red Hat).
    - **Linux Mint** (user-friendly), **openSUSE**, **Mandriva**, **Slackware**, **Gentoo**.
---
### 2. Partitionnement et Systèmes de Fichiers

- **Partitionnement** : Divise le disque pour installer plusieurs OS ou organiser les données.
    - **Partitions** : Primaires (systèmes d’exploitation) et étendues (partitions logiques).
    - **MBR** : Stocke la table des partitions et le chargeur d’amorçage.
    - **Swap** : Zone dédiée à l’échange entre mémoire vive et disque dur
- **Systèmes de Fichiers** : Organisent les fichiers sur le disque.
    - **Exemples** : FAT (Windows), NTFS (Windows), Ext2/Ext3/Ext4 (Linux).
    - **Inodes** : Structures pour les informations sur les fichiers (user, groupe, taille, droits d’accès nbr de liens, … ).
    - **Montage** :Les systèmes de fichiers sont accessibles en les **montant** sur des répertoires avec `mount` (`sudo mount <disque ou partition> <point de montage>`), ce qui rend leur contenu visible sans le déplacer ; ils sont ensuite **démontés** avec `umount` (`sudo umount <point de montage>`) pour retirer cet accès.
    
    <img src="UNIX Images/image (1).png" style="border-radius: 7px;" width="400">
---
### 3. Virtualisation
- **Définition** : Exécuter plusieurs OS sur une même machine.
- **Types** : Émulation, Virtualisation complète, Paravirtualisation, Niveau OS.
- **Outils** :
    - **VMware** : VMware Workstation, Player (postes de travail).
    - **VirtualBox** : Open-source, flexible.
---
## Chapitre 03:
### 1. Opérations sur les Répertoires
- **Organisation** : En UNIX/Linux, l’arborescence commence à la racine `/`.
- **Commandes principales** :
    - `mkdir` : Créer un répertoire; `-p`: créer une fois une hiérarchie de répertoires.
    - `rmdir` : Supprimer un répertoire (doit être vide); `-p`: supprimer une hiérarchie.
    - `cd` : Changer de répertoire.
    - `ls` : Liste le contenu d'un répertoire ; `-l`: affiche les détails (permissions, propriétaire, taille, etc.), `-a`: inclut les fichiers cachés.
    - `pwd` : Afficher le répertoire courant.
---
### 2. Opérations sur les Fichiers

- **Création de fichiers** :
    - **`touch fichier`** : Crée un fichier vide.
    - **`cat > fichier`** : Crée un fichier et y ajoute du contenu (finir avec **Ctrl+D**).
- **Affichage du contenu** :
    - **`cat fichier`** : Affiche le contenu du fichier.
    - **`more` fichier** / **`less` fichier** : Affichent le contenu page par page.
        - **`less` options** :
            - **`b`** : Revenir en arrière.
            - **`v`** : Ouvrir l'éditeur.
            - **Echap + a** : Mode ajout.
            - **`:wq`** : Enregistrer et quitter.
            - **`q`** : Quitter.
- **Édition de fichiers** :
    - **`vi fichier`** : Éditeur de texte.
        - **`i`** : Mode insertion.
        - **`:wq`** : Enregistrer et quitter.
        - **`:q!`** : Quitter sans enregistrer.
- **Suppression de fichiers** :
    - **`rm fichier`** : Supprime un fichier.
        - **Options** :
            - **`r`** : Supprime récursivement.
            - **`i`** : Confirmation avant suppression.
            - **`f`** : Force la suppression sans confirmation.
- **Liens** :
    - **`ln fichier lien`** : Crée un lien **physique**, un double du fichier pointant vers le même emplacement mémoire. Le fichier reste accessible même si l'original est supprimé.
    - **`ln -s fichier lien_symbolique`** : Crée un lien **symbolique**, ou raccourci, qui pointe vers le fichier original. Le lien devient cassé si le fichier d'origine est supprimé.
- **Recherche de fichiers** :
    - **`locate nom_fichier`** : Recherche un fichier par nom.
    - **`grep "texte" fichier`** : Recherche un texte dans un fichier.
        - **Options** :
            - **`i`** : Insensible à la casse.
            - **`r`** : Recherche récursive.
            - **`l`** : Affiche les noms de fichiers correspondants.
            - **`v`** : Affiche les lignes ne contenant pas le texte.
- **Copie et déplacement de fichiers** :
    - **`cp source destination`** : Copie un fichier.
        - **Options** :
            - **`i`** : Confirmation avant d’écraser.
            - **`r`** : Copie récursive.
            - **`p`** : Préserve les attributs (Les permissions,La date de modification, L’appartenance utilisateur et groupe)**.**
            - **`s`** : Crée un lien symbolique au lieu de copier.
	            ⚠️ **Remarque** : pourrait ne pas être disponible sur toutes les distributions.
    - **`mv source destination`** : Déplace ou renomme un fichier.
        - **Options** :
            - **`i`** : Confirmation avant d’écraser.
            - **`u`** : Déplace seulement si le fichier source est plus récent.

---

## Chapitre 05:

### 1. Droits d’accès

- **Principe des droits d'accès** : Dans un système multi-utilisateur comme Linux, les droits d'accès permettent de gérer qui peut lire, modifier, ou exécuter un fichier/répertoire. Chaque utilisateur a un identifiant unique (UID) et appartient à un ou plusieurs groupes.
- **Catégories de droits** :
    - **Propriétaire (u)** : L'utilisateur qui possède le fichier.
    - **Groupe (g)** : Les utilisateurs appartenant au même groupe que le fichier.
    - **Autres (o)** : Tous les autres utilisateurs.
- **Types de permissions** :
    - **Lecture (r)** : Permet d'afficher le contenu d’un fichier ou la liste des fichiers d'un répertoire.
    - **Écriture (w)** : Autorise la modification d'un fichier ou la gestion des fichiers dans un répertoire (ajout, suppression).
    - **Exécution (x)** : Nécessaire pour exécuter un programme ou pour accéder à un répertoire.

Les droits peuvent être consultés avec la commande `ls -l`, qui affiche les permissions pour le propriétaire, le groupe et les autres.

---

### 2. Modification des Droits d’Accès

- **Commande `chmod`** : Utilisée pour modifier les permissions d’un fichier/répertoire. Il existe deux méthodes pour changer les droits :
    - **Méthode symbolique** :
        - **Syntaxe** : `chmod [u/g/o/a] [+/-/=] [r/w/x] fichier`
            - `u`, `g`, `o`, `a` : Propriétaire, groupe, autres, tous.
            - `+` : Ajoute un droit.
            - `-` : Retire un droit.
            - `=` : Définit les droits spécifiés.
        - **Exemples** :
            - `chmod u+r fichier` : Ajoute le droit de lecture pour le propriétaire.
            - `chmod go-w fichier` : Retire le droit d'écriture pour le groupe et les autres.
            - `chmod a+x fichier` : Ajoute le droit d’exécution pour tous.
    - **Méthode octale** :
        - Les droits sont représentés par des chiffres de 0 à 7 :
            - **4** _(100)_ pour lecture, **2** _(010)_ pour écriture, **1** _(001)_ pour exécution.
            - Exemple : `chmod 754 fichier` applique les droits `rwx` _(111)_ au propriétaire (7 = 4+2+1), `r-x` _(101)_ au groupe (5 = 4+1), et `r--` _(100)_ aux autres (4).
        - **Exemples** :
            - `chmod 644 fichier` : Propriétaire (lecture/écriture), groupe/autres (lecture).
            - `chmod 755 fichier` : Propriétaire (lecture/écriture/exécution), groupe/autres (lecture/exécution).

---

### 3. Modification du Propriétaire et du Groupe

- **Changer le propriétaire** : Seul l’administrateur (root) peut modifier le propriétaire d’un fichier avec la commande `chown`.
    - **Syntaxe** : `chown nouvel_utilisateur fichier`
    - **Exemple** : `chown user1 fichier` assigne la propriété du fichier à `user1`.
- **Changer le groupe** : Le propriétaire ou root peut changer le groupe avec `chgrp`.
    - **Syntaxe** : `chgrp nouveau_groupe fichier`
    - **Exemple** : `chgrp groupe1 fichier` assigne le groupe `groupe1` au fichier.
- **Changer propriétaire et groupe en même temps** :
    - **Syntaxe** : `chown utilisateur:groupe fichier`
    - **Exemple** : `chown user1:groupe1 fichier` modifie le propriétaire et le groupe du fichier.

---

### 4. Permissions par Défaut (umask)

- **Umask** : Définit les permissions de base pour les nouveaux fichiers et répertoires. Il fonctionne en supprimant des permissions lors de la création.
    - **Syntaxe** : `umask valeur`
        - Les valeurs sont en octal, similaires à `chmod`, mais elles définissent les permissions à enlever.
    - **Exemple** : `umask 022` empêche l’écriture pour le groupe et les autres sur les nouveaux fichiers (les permissions de base sont donc 755 pour les répertoires et 644 pour les fichiers).
- **Vérifier/Modifier la valeur actuelle de umask** :
    - **Afficher la valeur** : `umask`
    - **Exemple** : `umask 077` enlève toutes les permissions pour le groupe et les autres (seul le propriétaire a tous les droits sur les nouveaux fichiers).
- **Affichage sous forme symbolique**: Pour afficher la valeur de `umask`sous forme symbolique, utilisez l’option `-S`:
    - **Commande** : `umask -S`
    - **Exemple** : Si le `umask` est défini sur `000`, l'affichage sera : `u=rwx,g=rwx,o=rwx`, indiquant que tous les utilisateurs (propriétaire, groupe et autres) ont tous les droits (lecture, écriture, exécution) sur les nouveaux fichiers.

---

## Chapitre 6:

### 1. Gestion des Utilisateurs et des Mots de Passe

- **Types de comptes** :
    - **Superutilisateur (root)** : UID 0, gère l'administration du système.
    - **Comptes systèmes** : Utilisés par les services et applications, avec UID entre 1 et 499.
    - **Comptes ordinaires** : UID de 500 et plus, pour les utilisateurs standard.
- **Création d'un utilisateur** : La commande `useradd` permet d'ajouter un utilisateur avec diverses options :
    - **UID** : Identifiant unique de l'utilisateur.
    - **Groupe** : Groupe principal ou secondaires.
    - **Expiration** : Date d’expiration du compte.
        Options de la commande `useradd` :
        - **`u`** : Définit l’UID unique de l’utilisateur.
        - **`g`** : Spécifie le groupe principal de l’utilisateur.
        - **`G`** : Définit les groupes secondaires de l’utilisateur.
        - **`d`** : Indique le répertoire personnel de l’utilisateur.
        - **`s`** : Définit le shell par défaut de l’utilisateur.
        - **`e`** : Date d’expiration du compte (ex. : `YYYY-MM-DD`).
        - **`p`** : Mot de passe crypté initial.
- **Modification des utilisateurs** : La commande `usermod` est utilisée pour modifier les informations d’un utilisateur existant.
	Options :
	- `-m` : Déplace le contenu du répertoire personnel vers le nouveau répertoire.
	- `-L` : Verrouille le compte.
	- `-U` : Déverrouille le compte.
    - `-p` : Modifie le mot de passe de l'utilisateur.
- **Affichage des informations utilisateur** : La commande `finger` affiche des informations sur un ou plusieurs utilisateurs.
    - **Options** :
        - **`l`** : Affiche les informations au format long (par défaut).
        - **`s`** : Affiche les informations au format court.
- **Modification des informations utilisateur** : La commande `chfn` permet de changer les informations utilisées par `finger`. Seul l’administrateur peut modifier les informations d'un autre utilisateur.
    - **Options** :
        - **`f nom`** : Modifie le nom et le prénom.
        - **`o bureau`** : Modifie le nom du bureau.
        - **`p btel`** : Modifie le numéro de téléphone du bureau.
        - **`h mtel`** : Modifie le numéro de téléphone personnel.
- **Modification des mots de passe** : La commande `passwd` permet de changer et gérer les mots de passe avec diverses options :
    - **Options** :
        - `-l` : Verrouille le compte en ajoutant un **!** devant le mot de passe crypté.
        - `-u` : Déverrouille le compte. Nécessite `-f` si le compte n'a pas de mot de passe.
        - `-d` : Supprime le mot de passe du compte (root).
        - `-n <j>` : Définit la durée de vie minimale en jours du mot de passe.
        - `-x <j>` : Définit la durée de vie maximale en jours du mot de passe.
        - `-w <j>` : Spécifie le nombre de jours avant un avertissement d’expiration du mot de passe.
        - `-i <j>` : Définir le délai de grâce avant désactivation du compte après expiration du mot de passe.
        - `-S` : Affiche le statut du compte.
- **Suppression d'un utilisateur** : La commande `userdel` permet de supprimer un utilisateur ainsi que son répertoire personnel.
    - **Options** :
        - `-r` : Supprime également le répertoire personnel de l'utilisateur et son contenu.
        - `-f` : Force la suppression de l'utilisateur même si celui-ci est connecté ou possède des processus actifs.
---

### 2. Gestion des Groupes d’Utilisateurs

- **Types de groupes** :
    - **Groupe root** : GID 0, associé à l’administrateur.
    - **Groupes systèmes** : GID entre 1 et 499, pour les droits d’accès partagés entre applications.
    - **Groupes ordinaires** : GID 500 et plus, pour des groupes d’utilisateurs réels.
- **Création et modification d'un groupe** :
    - **Création** : `groupadd` pour ajouter un groupe.
    - **Suppression** : `groupdel` supprime un groupe. Les fichiers appartenant à ce groupe nécessitent une modification manuelle pour changer de groupe.
    - **Modification** : `groupmod` permet de changer le nom ou le GID d’un groupe.
- **Changement de groupe pour une session** : Un utilisateur peut temporairement changer de groupe avec `newgrp` pour adopter les permissions de ce groupe.

---

## Chapitre 7:

### 1. Caractéristiques d’un Processus

- Un **processus** est un programme en cours d’exécution.
- Chaque processus est identifié par un **PID** (Process ID).
- Un processus peut avoir un **PPID** (Parent Process ID) s’il est créé par un autre processus (processus parent).
- Le processus **init** (PID = 1) est le premier lancé au démarrage du système.

---

### 2. États des Processus

- **Élu** : Le processus est en cours d’exécution.
- **Prêt** : En attente du CPU.
- **Bloqué** : Attente d’une ressource ou d’un événement.
- **Zombie** : Terminé, mais non nettoyé par son processus parent.
- États affichés dans le champ `STAT` :
    - **D** : Dormant non interruptible.
    - **R** : En cours d’exécution.
    - **S** : Endormi mais interruptible.
    - **T** : Stoppé.
    - **Z** : Zombie.

---

### 3. Visualiser les Processus

- **`ps`** : Affiche les processus.
    - Options :
        - **`-e`** : Tous les processus.
        - **`-f`** : Format détaillé.
        - **`aux`** : Affiche les processus avec leurs propriétaires.
    - Exemple : `ps -ef` pour une vue complète.
- **`top`** : Affiche en temps réel les processus actifs.
- **`pstree`** : Affiche les processus sous forme d’arbre.

---

### 4. Arrêter un Processus

- **`kill` PID** : Arrête un processus par son ID.
    - Options :
        - **`-l`** : Liste des signaux disponibles.
        - **`-9`** : Forcer l’arrêt (signal KILL).
- **`killall`** : Termine tous les processus portant un nom spécifique.

---

### 5. Changer la Priorité d’un Processus

- **`nice`** : Lance un processus avec une priorité spécifique (valeur entre **-20** et **20**, où -20 est la plus prioritaire).
    - Exemple : `nice -n 10 commande`.
- **`renice`** : Change la priorité d’un processus en cours.
    - Exemple : `renice -n 5 -p PID`.

---

### 6. Lancer un Processus en Tâche de Fond

- **`&`** : Lance une commande en arrière-plan.
    - Exemple : `commande &`.
- **`nohup`** : Continue d’exécuter le processus après la déconnexion.
    - Exemple : `nohup commande &`.

---

### 7. Utilisation de la Mémoire

- **`free`** : Affiche la mémoire utilisée et disponible.
    - Options :
        - **`-m`** : En méga-octets.
        - **`-g`** : En giga-octets.
- **`vmstat`** : Montre les statistiques sur la mémoire virtuelle.

---

## Chapitre 7:

### 1. Définition et Caractéristiques d’un Processus

- **Processus** : Programme en cours d'exécution. Chaque exécution d’un programme crée un processus unique avec un contexte d’exécution.
- Caractéristiques principales :
    - Identifié par un **PID** (Process ID).
    - Peut être associé à un **PPID** (Parent Process ID) pour indiquer son processus parent.
    - États possibles : actif, prêt, bloqué, zombie.
    - Contient des informations comme :
        - **Compteur ordinal** : Prochaine instruction à exécuter.
        - **Pile d’exécution** : Suivi des appels de fonctions.
        - **Contexte d’exécution** : Répertoire courant, fichiers ouverts, priorité, etc.

---
### 2. États et Transition des Processus

- **États principaux** :
    - **Actif/Élu** : Le processus est exécuté par le CPU.
    - **Prêt** : En attente d’être sélectionné par le CPU.
    - **Bloqué** : En attente d’une ressource (E/S, événement).
- **États supplémentaires** :
    - **R (Running)** : En cours d’exécution.
	- **S (Sleeping)** : Endormi mais interruptible.
	- **D (Dormant)** : Bloqué, non interruptible.
	- **T (Stopped)** : Mis en pause.
	- **Z (Zombie)** : Terminé mais non collecté.
- **Transitions importantes**:
    - **Activation** : De prêt à actif.
    - **Blocage** : De actif à bloqué.
    - **Réveil** : De bloqué à prêt.

---
### 3. Gestion et Commandes pour les Processus

- **Visualiser les processus** :
    - **`ps`** : Affiche les processus.
        - Options :
            - `-e` : Affiche tous les processus.
			- `-f` : Affiche un format détaillé avec les relations parents/enfants.
			- `-u utilisateur` : Affiche les processus d’un utilisateur spécifique.
			- `-a` : Affiche les processus des autres utilisateurs.
			- `x` : Affiche les processus sans terminal associé.
			- `aux` : Affiche tous les processus avec les détails utilisateurs.
			- `--forest` : Affiche les processus sous forme d’arborescence.
			- `-o champ1,champ2` : Permet de personnaliser l’affichage en choisissant les champs.
			    - Exemples de champs : `pid`, `ppid`, `cmd`, `%cpu`, `%mem`, `stat`.
			- `-l` : Affiche un format long avec des détails supplémentaires (états, priorités).
			- `-H` : Affiche les processus en mode hiérarchique.
	- **`time`** : utilisée pour **mesurer le temps d'exécution** d'une commande ou d'un programme sous Linux
		- Syntaxe : `time commande`
		- Sortie :
		    - **real** : Temps réel écoulé (temps "mur").
	        - **user** : Temps CPU passé dans l’espace utilisateur.
	        - **sys** : Temps CPU passé dans l’espace noyau.
    - **`top`** : Affichage en temps réel des processus actifs.
    - **`htop`**: Offre une interface plus intuitive et colorée pour surveiller les processus.
	    - Options :
		    - `-u <user>`: Affiche uniquement les processus d’un utilisateur spécifique.
            - `-p <pid>`: Surveille uniquement les processus avec les PIDs spécifiés.
            - `-s <column>`: Trie les processus selon une colonne spécifique (comme `%CPU` ou `MEM`).
            - `-d <delay>`: Définit l’intervalle de rafraîchissement en secondes.
            - `--tree`: Affiche les processus sous forme d’arborescence.
    - **`pstree`** : Affiche les processus sous forme d’arbre.
- **Arrêter un processus** :
    - **`kill PID`** : Envoie un signal pour terminer un processus.
        - Options :
            - `-l` : Liste des signaux disponibles.
            - `-9` : Force la terminaison immédiate (signal KILL).
    - **`killall nom_processus`** : Termine tous les processus du même nom.

---
### 4. Création et Hiérarchie des Processus

- **Création de processus** : 
    - La fonction **`fork()`** crée un nouveau processus (fils).
    - Héritage du processus fils :
        - Propriétaire et priorité.
        - Descripteurs de fichiers ouverts.
        - Comportement vis-à-vis des signaux.
    - **Différenciation père/fils** :
        - **Retour de `fork()`** :
            - Valeur **0** : Processus fils.
            - PID du fils : Dans le processus père.
    - Exemple simple :
```c
int pid = fork(); 
if (pid == 0) { 
	printf("Fils\n"); 
} else { 
	printf("Père\n"); 
}
```

- **Exécution d’un nouveau programme** :
    - **`execl()`** : Remplace le processus courant par un autre programme.
        - Exemple : `execl("/bin/ls", "ls", "-l", NULL);`.

---
### 5. Priorités et Tâches en Fond

- **Changer la priorité** :
    - **`nice`** : Lance un processus avec une priorité spécifique (valeur entre -20 et 20).
    - **`renice`** : Change la priorité d’un processus existant (par PID, UID ou GID).
- **Tâches en fond** :
    - **`&`** : Lance un processus en arrière-plan.
        - Exemple : `commande &`.
    - **`nohup`** : Permet de continuer un processus après déconnexion.

---
### 6. Gestion des Fin de Processus et Zombie

- **Synchronisation des fins** :
    - **`wait()`** : Suspend l’exécution du parent jusqu’à la fin d’un fils.
    - **Zombie** : Un fils terminé mais non collecté reste un zombie. Utilisez `wait()` pour éviter cela.

---
### 7. Gestion de la Mémoire

- **`free`** : Affiche l’utilisation de la mémoire.
    - Options : `-m` (Mo), `-g` (Go).
- **`vmstat`** : Donne des informations sur la mémoire virtuelle.

---
### 8. Points Clés des Appels Systèmes

- **`getpid()`** : Récupère le PID du processus courant.
- **`getppid()`** : Récupère le PID du parent.
- **`exit()`** : Termine un processus.
- **`sleep()`** : Suspend l’exécution pour une durée spécifiée.


<img src="UNIX Images/image-1.png" style="border-radius: 7px;" width="400">
<img src="UNIX Images/image-2.png" style="border-radius: 7px;" width="400">
<img src="UNIX Images/image-3.png" style="border-radius: 7px;" width="400">
<img src="UNIX Images/image-4.png" style="border-radius: 7px;" width="400">

## Chapitre 8
### **Montage et Maintenance des Partitions**

- **Montage de partitions** : Utiliser `fdisk` pour identifier les partitions et `mount` pour les monter dans l’arborescence Linux.
- **Fichier `/etc/fstab`** : Configure les systèmes de fichiers pour le montage automatique au démarrage.
    <img src="UNIX Images/image-5.png" style="border-radius: 7px;" width="400">
- **Commande `fdisk`** : Gère les partitions, mais attention aux pertes de données lors des modifications.
    - **Options** : `fdisk -l` (liste les partitions), `fdisk -p` (affiche la table de partition), `fdisk -n` (crée une nouvelle partition), `fdisk -w` (écrit les modifications).
    - `gparted` : Interface graphique pour gérer les partitions.

### **Archivage, Compression et Backup**

- **Sauvegarde incrémentale** : Utiliser `dump` pour les sauvegardes et `restore` pour les restaurations.
  - **Niveau 0** : Sauvegarde complète.
  - **Niveau 1** : Sauvegarde des modifications depuis la dernière sauvegarde de niveau 0.
  - **Niveaux 1-9** : Sauvegardes des modifications depuis la dernière sauvegarde du niveau inférieur.
  - `/etc/dumpdates` : Fichier de suivi des sauvegardes.

    <img src="UNIX Images/image-6.png" style="border-radius: 7px;" width="400">
    
    <img src="UNIX Images/image-7.png" style="border-radius: 7px;" width="400">

  - RESTORE

    <img src="UNIX Images/image-8.png" style="border-radius: 7px;" width="400">

    <img src="UNIX Images/image-9.png" style="border-radius: 7px;" width="400">

- **Commandes `tar` et `gzip`** :
  - `tar` : Utilitaire pour créer, afficher et extraire des archives.
    - `tar -zcvf nomarchive fichiers` : Crée une archive compressée.
    - `tar -zxvf nomarchive` : Extrait une archive.

    <img src="UNIX Images/image-10.png" style="border-radius: 7px;" width="400">
  - `gzip` : Compresse des fichiers.
    - `gzip fichier` : Compresse un fichier.
    - `gzip -d fichier.gz` : Décompresse un fichier.

### **Service d’Impression**

- **Systèmes d’impression** :

    - **System V (LP)** : Un des types de systèmes d'impression utilisés sous Unix.
    - **Berkeley (LPD)** : Le plus répandu sous Linux, développé par l’Université de Berkeley.

- **Fonctionnement du Système d'Impressio**n :

    - Les impressions reposent sur des files d'attente (spoules) où les demandes sont stockées avant d'être envoyées aux périphériques d'impression.
    - Le démon `lpd` gère ces files d'attente et vérifie régulièrement leur contenu pour appliquer les traitements spécifiés dans le fichier de configuration `/etc/printcap`.

- **Commandes BSD** :

    - `lpr` : Soumettre un travail d'impression.
    - `lpq` : Consulter les files d'attente.
    - `lprm` : Supprimer un travail d'impression.

- **Filtres d'Impression** :

    - Utilisés pour convertir des données dans un format compréhensible par l'imprimante.
    - Langages courants : PostScript, PCL (Hewlett-Packard), EPS (EPSON).
    - Outils comme APS Filters et Magic Filters facilitent l'installation des imprimantes.

- **LPRng** :

    - Une évolution du système LPR, offrant la compatibilité avec LPR classique.
    - Caractéristiques : support de plusieurs imprimantes pour une même file d'attente, chaînage de files d'attente, sécurité améliorée, contrôle à distance, gestion des priorités.

- **CUPS (Common Unix Printing System)** :

    - Un système d'impression standardisé pour tous les Unix, utilisant le protocole IPP (Internet Printing Protocol) et un démon serveur `cupsd`.
    - Fichier de configuration : `/etc/cups/printers.conf`.
    - Interface d'administration web accessible à `http://localhost:631/admin`.

- **Outils Graphiques** :

    - `system-config-printer` : Outil graphique pour configurer les files d'impression locales et réseau sous RedHat.
    - CUPS propose également une interface d’administration basée sur le Web, facilitant la gestion des imprimantes.

## Chapitre 9
### **Gestion des Quotas**

- **Introduction** : Les quotas permettent de limiter l'utilisation des systèmes de fichiers par utilisateur ou groupe, nombre de fichiers ou espace disque.

  - **Limite dure** : Dépassement refusé.
  - **Limite douce** : Dépassement avec avertissement, suivi d’un délai de grâce.

- **Configuration** :

  - Modifier `/etc/fstab` pour activer les quotas au demarrage (`usrquota` pour utilisateurs, `grpquota` pour groupes).

    <img src="UNIX Images/image-11.png" style="border-radius: 7px;" width="400">

  - `mount -o remount /` : remonte le système de fichiers avec les quotas activés.  
  - Utiliser `quotacheck` pour créer les fichiers `aquota.user` et `aquota.group`.
    - `-g` : Pour les quotas de groupe.
    - `-u` : Pour les quotas d’utilisateur.
    - `-a` : Pour tous les systèmes de fichiers.
    - `-v` : Mode verbeux (affiche les étapes).
    - `-m` : Pour ne pas essayer de faire un remount en mode read only avant le check.

    <img src="UNIX Images/image-12.png" style="border-radius: 7px;" width="400">

  - Activer les quotas avec `quotaon` et les désactiver avec `quotaoff` lorsque les fichiers n'existent pas au démarrage.
    - **Options** : `-u` (utilisateurs), `-g` (groupes), `-a` (tous).

- **Attribution des Quotas** :

  - Utiliser `edquota` pour définir les quotas (limite douce et dure) pour les utilisateurs et les groupes.

- **Attribution de Quotas à un Utilisateur** :
Pour attribuer des quotas à un utilisateur spécifique, utilisez la commande `edquota`.

    ```bash
    sudo edquota -u user1
    ```
    - Cette commande ouvre l'éditeur `vi` ou l'éditeur défini par `$EDITOR` pour modifier les quotas de l'utilisateur `user1`. 
    - Vous verrez une structure similaire :

        <img src="UNIX Images/image-13.png" style="border-radius: 7px;" width="400">

        - **Blocks** : Quantité d'espace disque utilisé en Ko.
        - **Soft limit** : Limite douce, après laquelle des avertissements sont envoyés.
        - **Hard limit** : Limite dure, qui ne peut pas être dépassée.
        - Modifiez les valeurs pour définir les nouvelles limites, puis sauvegardez et quittez l'éditeur.

- **Attribution de Quotas à un Groupe** : Pour un groupe, la procédure est similaire mais vous utilisez l'option `-g`.

    ```bash
    sudo edquota -g delphi
    ```

    - Cette commande permet de définir des quotas pour le groupe `delphi`. 
    - Vous pouvez éditer les limites similaires à celles des utilisateurs, avec les mêmes notions de soft limit, hard limit, et grace period.

- **Définitions Importantes** :
    - **Limite douce (Soft Limit)** : Le maximum qu'un utilisateur ou groupe peut utiliser avant de recevoir des avertissements.
    - **Limite dure (Hard Limit)** : La limite absolue qui ne peut pas être dépassée.
    - **Délai (Grace Period)** : Temps pendant lequel l'utilisateur peut dépasser la limite douce avant que la limite dure ne soit appliquée.


- **Système d'Alerte** : Utiliser `warnquota` pour alerter les utilisateurs dépassant leurs quotas.

- **Commandes Importantes** :

  - `quotacheck`(crée les fichiers de quota), `repquota`(affiche les quotas), `quotaon/quotaoff`(active/désactive les quotas), `warnquota`(envoie des alertes), `quota`(affiche les quotas), `quotastats`(statistiques des quotas), `setquota`(définit les quotas), `convertquota`(convertit les quotas).

---

### **Gestion des Paquetages**

- **Introduction** : `RPM` (Red Hat Package Manager) facilite la gestion des paquetages.

  - Gère l'installation, désinstallation, mise à jour, actualisation, recherche, et vérification des paquetages.

- **Utilisation de RPM** :

  - Commandes principales de `rpm` : 
    - `-i` (installation), `-e` (désinstallation), `-U` (mise à jour), `-q` (recherche), `-V` (vérification),`-v` (mode verbeux), `-h` (affiche les en-têtes), `-a` (tous les paquetages).
  - **Installation** : `rpm -i lftp-3.1.3-1.i386.rpm`.
    - lftp : Nom du paquetage.
    - 3.1.3 : Version du paquetage.
    - 1 : Numéro de version.
    - i386 : Architecture.
    - `package lftp-3.1.3-1 is already installed`: `--replacepkgs` pour forcer la réinstallation.
    - `error: Failed dependencies: libreadline.so.4 is needed by lftp-3.1.3-1`: `--nodeps` pour ignorer les dépendances.
  - **Désinstallation** : `rpm -e lftp` (nom du paquetage).
    - `error: Failed dependencies: lftp is needed by (installed) ncftp-3.1.3-1`: `--nodeps` pour ignorer les dépendances.
  - **Mise à Jour** : `rpm -Uvh lftp-3.1.4-1.i386.rpm`.
    - Met à jour ou installe un package.
    - `package lftp-3.1.4-1 (which is newer than lftp-3.1.3-1) is already installed`: `--oldpackage` pour rétrograder.
  - **Actualisation** : `rpm -Fvh lftp-3.1.4-1.i386.rpm`.
    - Met à jour uniquement les paquetages déjà installés.
  - **Recherche** : `rpm -q lftp`.
    - le retour est `lftp-3.1.4-1`: nom du paquetage, version, numéro de version.
  - **Signature d'un Paquetage** : `rpm --checksig lftp-3.1.4-1.i386.rpm`.
    - si la signature est valide, le message est `lftp-3.1.4-1.i386.rpm: rsa sha1 (md5) pgp md5 OK`.

- **Utilisation de Yum** :

  - `yum` gère les paquetages RPM avec résolution automatique des dépendances (**/etc/yum.conf**).
  - Defference entre `yum` et `rpm` : `yum` e yum résout automatiquement les problèmes de dépendances entre les paquetages, tout en notifiant à l’utilisateur les actions à entreprendre
  - **Commandes Importantes** :
    - `yum install lftp` : installe le paquetage `lftp`.
    - `yum update` : met à jour tous les paquetages, `yum check-update` pour vérifier les mises à jour.
    - `yum remove lftp` : désinstalle le paquetage `lftp`.
    - `yum list` : liste les paquetages installés.
      - **all** : tous les paquetages (default).
      - **available** : paquetages disponibles.
        - **updates** : paquetages mis à jour.
        - **installed** : paquetages installés.
        - **extras** : paquetages supplémentaires.
        - **obsoletes** : paquetages obsolètes.
    - `yum info lftp` : affiche les informations sur le paquetage `lftp`.
    - `yum provides /etc/passwd` : affiche le paquetage qui fournit le fichier `/etc/passwd`.
    - `yum search lftp` : recherche le paquetage `lftp`.

  - `service yum-updatesd start` : démarre le service de mise à jour automatique.

- **Interface Graphique** : `system-config-packages` est une interface simplifiée pour gérer les paquetages sous RedHat.

## Chapitre 10
### Cron

- **Définition** : Cron est un outil d'automatisation des tâches répétitives.
- **Configuration** :
    - Les tâches sont définies dans des fichiers crontab situés dans `/var/spool/cron` ou pour les tâches système dans `/etc/crontab`.
    - Suppose que le système est allumé en continu, si le système est éteint, les tâches ne s'exécuteront pas.
    - Une tâche cron est configurée avec une périodicité :
        ```plaintext
        minute heure jour mois jour_semaine commande
        ```
    - Par exemple, `0 5 * * 1 /path/to/script.sh` exécute `script.sh` tous les lundis à 5 heures du matin.
    - **Commandes** :
        - `crontab -e` : Édite le crontab de l'utilisateur.
        - `crontab -l` : Liste le crontab de l'utilisateur.
        - `crontab -r` : Supprime le crontab de l'utilisateur.
        - `crontab -u user` : Gère le crontab d'un utilisateur spécifique. 
    - Exemple de fichier crontab (/etc/crontab) :

        <img src="UNIX Images/image-15.png" style="border-radius: 7px;" width="400">

        <img src="UNIX Images/image-14.png" style="border-radius: 7px;" width="400">

        <img src="UNIX Images/image-16.png" style="border-radius: 7px;" width="400">
        
    - **Variables** :
        - **LOGNAME** : Nom de l'utilisateur (root par défaut).
        - **HOME** : Répertoire personnel de l'utilisateur (root par défaut).
        - **SHELL** : Shell par défaut (bash par défaut).
        - **PATH** : Chemin de recherche des exécutables (/usr/bin:/bin par défaut).
    - **Spécifications de Temps** :
        - **`*`** : Toutes les valeurs.
        - **`*/n`** : Toutes les `n` unités (par exemple, `*/5` pour toutes les 5 minutes).
        - **`n`** : Valeur spécifique.
        - **`n-m`** : Plage de valeurs (par exemple, `1-5` pour 1 à 5).
        - **`n,m`** : Valeurs spécifiques (par exemple, `1,3,5` pour 1, 3 et 5).
        - **`n/m`** : Toutes les `m` unités à partir de `n` (par exemple, `*/3` peut être utilisée dans le champ des mois pour passer un mois sur trois.).
    - **Exemples** :
        - `0 5 * * 1 /path/to/script.sh` : Exécute `script.sh` tous les lundis à 5 heures du matin.
        - `0 0 * * * /path/to/backup.sh` : Exécute `backup.sh` tous les jours à minuit.
        - `0 0 1 * * /path/to/monthly.sh` : Exécute `monthly.sh` le premier jour de chaque mois à minuit.
        - `0 0 * * 0 /path/to/weekly.sh` : Exécute `weekly.sh` tous les dimanches à minuit.
        - `@reboot /path/to/startup.sh` : Exécute `startup.sh` au démarrage du système.
- **Sorties** :
    - Par défaut, les sorties des tâches sont envoyées par email au propriétaire du crontab.
    - La variable `MAILTO` peut être définie dans le crontab pour rediriger ou annuler l'envoi d'email.
- **Gestion du service `crond`** :
    - **Démarrer le service** : `service crond start`
    - **Arrêter le service** : `service crond stop`
    - **Redémarrer le service** : `service crond restart`
    - **Vérifier le statut du service** : `service crond status`
    - **Activer le service au démarrage** : `systemctl enable crond`
    - **Désactiver le service au démarrage** : `systemctl disable crond`
- **Journalisation** :
    - Le fichier journal de cron est `/var/log/cron`, où les détails d'exécution sont enregistrés.

    <img src="UNIX Images/image-17.png" style="border-radius: 7px;" width="400">
- **Sécurité** :
    - Les fichiers `/etc/cron.allow` et `/etc/cron.deny` contrôlent l'accès à cron.
    - Si `cron.allow` existe, seuls les utilisateurs listés peuvent utiliser cron.
    - Si `cron.deny` existe et que `cron.allow` est absent, tous les utilisateurs sauf ceux listés peuvent utiliser cron.

### Anacron

- **Définition** : Anacron est similaire à `cron` mais est conçu pour exécuter des tâches qui auraient dû s'exécuter alors que le système était éteint.
- **Utilisation** : Utilisé pour des tâches journalières, hebdomadaires ou mensuelles.
- **Configuration** :
    - Le fichier de configuration est `/etc/anacrontab`.
    - Format typique d'une ligne :
        ```plaintext
        période délai job-id commande
        ```
        - **Période** : dure minimum entre deux exécutions de la tâche (en jours, par exemple `1` pour quotidien, `7` pour hebdomadaire).
        - **Délai** : délai en minutes après le démarrage du système avant l'exécution de la tâche (par exemple, `5` pour un délai de 5 minutes).
        - **Job-id** : identifiant unique pour la tâche (par exemple, `daily_backup`).
        - **Commande** : commande permet de spécifier le script ou la tâche à exécuter.
    - Par exemple, `1 5 daily_backup /path/to/backup.sh` exécute `backup.sh` tous les jours avec un délai de 5 minutes après le démarrage.

        <img src="UNIX Images/image-18.png" style="border-radius: 7px;" width="400">
- **Journalisation** :
    - Les dates d'exécution sont enregistrées dans `/var/spool/anacron`

        <img src="UNIX Images/image-19.png" style="border-radius: 7px;" width="400">
    - les journaux détaillés sont également disponibles dans `/var/log/cron`.

        <img src="UNIX Images/image-20.png" style="border-radius: 7px;" width="400">
- **Lancement** :
    - `service anacron start` : démarre le service.
    - `service anacron stop` : arrête le service.
    - `service anacron restart` : redémarre le service.
    - `service anacron status` : vérifie le statut du service.

### AT et ATD
- `AT` : Permet de planifier des tâches ponctuelles, qui doivent être exécutées une seule fois à une date et une heure précises.
- `ATD` : Un démon lancé au démarrage du système, gère les tâches planifiées comme une file d’attente (spoule).
- Defference entre `cron` et `at` : `cron` est utilisé pour les tâches répétitives, tandis que `at` est utilisé pour les tâches ponctuelles.
- Defference entre `at` et `atd` : `at` est la commande pour planifier une tâche, tandis que `atd` est le démon qui gère les tâches planifiées.

- **Lancement** :
    - `service atd start` : démarre le service.
    - `service atd stop` : arrête le service.
    - `service atd restart` : redémarre le service.
    - `service atd status` : vérifie le statut du service.

- **Utilisation de la Commande AT**
    Syntaxe :
    ```bash
    at [options1] <heure> [date] + <incrément>
    at [options2] <tâches>
    ```
    Les commandes sont saisies sur le canal d'entrée standard et terminées par EOF (Ctrl+D).
    L'heure peut être saisie sous forme numérique ou à l'aide de mots-clés (`now`, `midnight`, `teatime`, `tomorrow`, `noon` etc.).

    - Options :
        - `-f fichier` : Exécute les commandes contenues dans le fichier spécifié (ex : `at -f script.sh 10:00`).
        - `-m` : Envoie un email à l'utilisateur après l'exécution de la tâche.
        - `-l` (ou `atq`) : Liste les tâches en attente.
        - `-r` (ou `atrm`) : Supprime une tâche planifiée par son identifiant (ex : `atrm 1`).

    - Format de l'Heure :
        - Peut être saisie comme `hh:mm`, `hhmm`, ou avec des mots-clés (`now + x minutes/hours/days/weeks`).
        - Exemples : `at 10:00`, `at now + 1 hour`, `at midnight`.

    - Format de la Date :
        - Peut inclure le mois, le jour et l'année (mois nombre, année) avec des abréviations ou en toutes lettres.
        - Exemples : `at 10:00 2022-12-31`, `at 10:00 31 Dec 2022`, `at 10:00 31/12/2022`.

    - Incrément :
        - Utilisé pour planifier une tâche à un certain intervalle de temps à partir de maintenant (`minute`, `hour`, `day`, `week`, `month`, `year`).
        - Exemples : `at now + 1 hour`, `at now + 2 days`, `at now + 1 week`.
    

- **Contrôle des Travaux**
    - `atq` : Affiche les tâches planifiées encore en attente.

        <img src="UNIX Images/image-21.png" style="border-radius: 7px;" width="400">

        - **/var/spool/at** : Contient les fichiers de tâches planifiées.
    - `atrm` : Supprime les tâches planifiées par leur identifiant (equivalent à `at -d`).

- **Sécurité**
    Les fichiers `/etc/at.allow` et `/etc/at.deny` contrôlent l'accès à la commande `at`.
    - Si `at.allow` existe, seuls les utilisateurs listés peuvent utiliser `at`.
    - Si `at.allow` n'existe pas, mais `at.deny` existe, les utilisateurs non listés peuvent utiliser `at`.
    - Si les deux fichiers existent, seul `at.allow` est pris en compte.

- **Batch**
    - `batch` : Exécute les tâches dès que la charge de la machine le permet, sans nécessiter une heure précise, ou dès qu’une heure spécifiée est atteinte.
        - **Exemple** : `batch -f script.sh` exécute `script.sh` dès que possible (équivalent à `at -f script.sh now`).
        
        <img src="UNIX Images/image-22.png" style="border-radius: 7px;" width="400">
- **Sorties et Erreurs**
    - Les sorties et erreurs des tâches planifiées avec `at` sont envoyées par mail à l’utilisateur, sauf si elles sont redirigées.

### Commandes Importantes

- **Cron** :
    - `crontab -e` : Éditer les tâches.
    - `crontab -l` : Lister les tâches actuelles.
    - `crontab -r` : Supprimer les tâches.
    - `cron.allow` et `cron.deny` : Fichiers de contrôle d'accès.
    - Journalisation dans `/var/log/cron`.
- **Anacron** :
    - `anacrontab` : Fichier de configuration.
    - Journalisation dans `/var/log/cron` et `/var/spool/anacron`.
- **AT** :
    - `at` : Ajouter une tâche.
    - `atq` : Lister les tâches.
    - `atrm` : Supprimer une tâche.
    - `at.allow` et `at.deny` : Fichiers de contrôle d'accès.
    - Journalisation dans `/var/spool/at`.


## Chapitre 11
### Les Réseaux TCP/IP

- **Adressage IP** :

    - Chaque machine dans un réseau doit posséder une adresse IP, attribuée à une interface.
    - L'adresse IPv4 est composée de 4 octets (32 bits).
        - Exemple : `212.50.14.82` / `11010100.00110010.00001110.01010010` (binaire).
    - Une adresse IP se divise en deux parties : **partie réseau** et **partie machine**.
    - Le **masque** spécifie le nombre de bits réservés à la partie machine.

        - Exemple : `11010100.00110010.00001110.01010010/26` (masque de 26 bits).
            - cela signifie que les 26 premiers bits sont réservés à la partie réseau et les 6 derniers bits à la partie machine.

- **Adresses Spéciales** :
    - **Adresse de Réseau** : Adresse de la première machine du réseau, se spécifie en mettant tous les bits de la partie machine à 0.
        - Exemple : l'adresse de réseau de `212.50.14.82/26` est `212.50.14.64/26`.
    - **Adresse de Broadcast (diffusion)** : Permet d'envoyer un message à toutes les machines du réseau, se specifie en mettant tous les bits de la partie machine à 1.
        - Exemple : le broadcast de `212.50.14.64/26` est `212.50.14.127/26`.

- **Classes IP** :

    - La classe d’une adresse IP r´eseau d´etermine la taille de ce dernier. Pour d´eterminer de quelle classe appartient un r´eseau, il faut examiner ses deux premiers bits.

        <img src="UNIX Images/image-23.png" style="border-radius: 7px;" width="400">
    - **Adresse IP Privée** : Utilisée pour les réseaux locaux, ne sont pas routables sur Internet.

        <img src="UNIX Images/image-24.png" style="border-radius: 7px;" width="400">

    - **Sous Réseaux** : Permettent de diviser un réseau en plusieurs sous-réseaux, en utilisant un masque de sous-réseau.

        <img src="UNIX Images/image-25.png" style="border-radius: 7px;" width="400">
- **Suite TCP/IP** :

    - Protocoles fondamentaux : `IP`, `ICMP`, `UDP`, `TCP`.
    - Les **ports** servent à distinguer les applications, avec des ports réservés au système (0-1023) et des ports dynamiques (1024-65535).
        - Exemple : `80` pour HTTP, `22` pour SSH, `25` pour SMTP.
        - `/etc/services` : Fichier de correspondance entre les ports et les services.

        <img src="UNIX Images/image-26.png" style="border-radius: 7px;" width="400">

    - **Protocole IP** : Permet de router les paquets entre les réseaux.
    - **Protocole ICMP** : Permet de gérer les erreurs et les messages de contrôle.
    - **Protocole UDP** : Permet d'envoyer des paquets sans garantie de livraison.
    - **Protocole TCP** : Permet d'envoyer des paquets avec garantie de livraison.


### Configuration du Réseau

- **Fichiers de Configuration** :

    - `/etc/hosts` : Résolution des noms sans DNS.
        - Exemple :
            ```plaintext
                127.0.0.1   localhost
                192.168.1.10   server1.example.com   server1
            ```
            - Ici, `localhost` est mappé à l'adresse IP `127.0.0.1`.
            - `server1.example.com` et son alias `server1` sont mappés à l'adresse IP `192.168.1.10`.
    - `/etc/resolv.conf` : Configuration du client DNS (adresse IP du serveur DNS et domaine de recherche par défaut).
        - Exemple :
            ```plaintext
                nameserver 8.8.8.8
                nameserver 8.8.4.4
                search example.com
            ```
            - `nameserver` : Spécifie l'adresse IP du serveur DNS (ici, Google DNS).
            - `search` : Définit le domaine de recherche par défaut (ici `example.com`)

    - `/etc/nsswitch.conf` : Spécifie la source de résolution des noms.
        - Exemple :
            ```plaintext
                hosts:      files dns
            ```
            - Cela signifie que le système cherchera d'abord dans le fichier `/etc/hosts`, puis utilisera DNS.
    - `/etc/sysconfig/network` : Contient la configuration réseau globale, comme le nom de la machine et la passerelle.
        - Exemple :
            ```plaintext
                NETWORKING=yes
                HOSTNAME=myserver.example.com
                GATEWAY=192.168.1.1
            ```
            - `NETWORKING` : Active ou désactive la mise en réseau.
            - `HOSTNAME` : Définit le nom de la machine.
            - `GATEWAY` : Spécifie l'adresse IP de la passerelle par défaut.
    - `/etc/sysconfig/network-scripts` : Informations spécifiques aux interfaces réseau, typiquement nommées `ifcfg-<interface>`.
        - Exemple pour `ifcfg-eth0` :
            ```plaintext
                DEVICE=eth0
                BOOTPROTO=dhcp
                ONBOOT=yes
            ```
            - `DEVICE` : Nom de l'interface réseau.
            - `BOOTPROTO` : Définit le protocole de démarrage (`dhcp` pour une adresse dynamique).
            - `ONBOOT` : Indique si l'interface doit être activée au démarrage.
    - `/etc/network/interfaces` : Configuration des interfaces réseau sous Debian.
        - Exemple :
            ```plaintext
                auto eth0
                iface eth0 inet static
                    address 192.168.1.100
                    netmask 255.255.255.0
                    gateway 192.168.1.1
                    dns-nameservers 8.8.8.8 8.8.4.4
            ```
            - `auto` : Active l'interface au démarrage.
            - `iface` : Définit l'interface et le type d'adressage (`static` pour une adresse statique).
            - `address` : Adresse IP de l'interface.
            - `netmask` : Masque de sous-réseau.
            - `gateway` : Adresse IP de la passerelle.
            - `dns-nameservers` : Serveurs DNS à utiliser.

- **host et dig** :

    - **`host`** : Utilitaire pour résoudre les noms de domaine.
        - Exemple : `host www.google.com` affiche l'adresse IP de `www.google.com`.
    - **`dig`** : Utilitaire pour interroger les serveurs DNS.
        - Exemple : `dig www.google.com` affiche les informations DNS de `www.google.com`.

- **Démarrage et Arrêt du Réseau** :

    - **D´emarrage classique** : 
        - `ifconfig eth0 up` : Active l'interface `eth0`.
        - `ifconfig eth0 down` : Désactive l'interface `eth0`.
        - `ifconfig eth0 192.168.1.12 netmask 255.255.255.0` : Définit l'adresse IP de `eth0`, avec un masque de sous-réseau.
    
    - **D´emarrage en utilisant les fichiers de configuration** : Pour r´ecup´erer la configuration depuis les fichiers `/etc/sysconfig/network` et `/etc/sysconfig/network-scripts`, on utilise la commande `/sbin/ifup`
        - Exemple : `ifup eth0` pour activer l'interface `eth0`.
    
    - **D´emarrage de toutes les interfaces** : Pour d´emarrer toutes les interfaces r´eseaux sur un redhat on utilise la commande: 
        - `/etc/rc.d/init.d/network start` 
        - Cette commande r´ecup´erera des informations depuis le fichier `/etc/sysctl.conf` (pour le routage par exemple)

### Routage

- **Commande `route`** :
    - **Ajouter une Passerelle par Défaut** :
        ```bash
        route add default gw 192.168.1.1 eth0
        ```
        - `default` : Définit une route par défaut.
        - `gw` : Spécifie l'adresse IP de la passerelle (gateway).
        - `eth0` : Interface réseau utilisée pour cette route.
    - **Ajouter une Route Statique** :
        ```bash
        route add -net 192.168.1.0/24 gw 192.168.2.1 eth2
        ```
        - `-net` : Spécifie un réseau.
        - `192.168.1.0/24` : Adresse du réseau avec son masque.
        - `gw` : Adresse de la passerelle pour ce réseau.
        - `eth2` : Interface réseau à utiliser.
    - **Suppression d'une Route** :
        ```bash
        route del default
        ```
        - Supprime la route par défaut existante.

- **Commande `ifup`** :
    - **Récupération de la Passerelle** :
        ```bash
        ifup eth0
        ```
        - Active l'interface `eth0` en utilisant les paramètres du fichier `/etc/sysconfig/network`.

- **Fichier `/etc/sysconfig/static-routes`** :
    - **Ajout Automatique de Routes Statistiques** :
        - Ce fichier permet de définir des routes statiques qui sont appliquées automatiquement au démarrage.

- **Commande `ping`** :
    - **Exemple d'Utilisation** :
        ```bash
        ping -c 4 google.com
        ```
        - `-c 4` : Envoie 4 paquets ICMP.
        - Vérifie la connectivité avec `google.com`.

- **Commande `arp`** :
    - **Afficher le Cache ARP** :
        ```bash
        arp -a
        ```
        - Montre les correspondances actuelles entre adresses IP et adresses MAC dans le cache ARP.

- **Commande `netstat`** :
    - **Afficher la Table de Routage** :
        ```bash
        netstat -r
        ```
        - `-r` : Affiche la table de routage.
    - **Statistiques des Interfaces** :
        ```bash
        netstat -i
        ```
        - `-i` : Montre les statistiques des interfaces réseau.

- **Commande `traceroute`** :
    - **Tracer le Chemin Vers une Destination** :
        ```bash
        traceroute google.com
        ```
        - Affiche chaque saut (routeur) entre votre machine et `google.com`.


## Chapitre 12
### Introduction

DHCP (Dynamic Host Configuration Protocol) est un protocole permettant la configuration automatique des paramètres TCP/IP des clients sur un réseau.

- **Avantages** :
    - Simplifie la maintenance et la gestion des adresses IP.
    - Les modifications de configuration sont appliquées automatiquement lors du redémarrage des clients.
    - Les adresses IP sont attribuées uniquement aux appareils en fonctionnement, optimisant l'utilisation des adresses disponibles.

### Fonctionnement du Protocole DHCP

- **Types d'Allocation** :
    - **Allocation Manuelle** : L'administrateur attribue une adresse IP spécifique à un client.
    - **Allocation Automatique** : Le serveur DHCP attribue une adresse IP permanente à un client.
    - **Allocation Dynamique** : Le serveur attribue une adresse IP pour une durée limitée, optimisant l'utilisation des adresses.

    <img src="UNIX Images/image-27.png" style="border-radius: 7px;" width="400">

### Types et Format des Messages DHCP

- **Types de Messages** :
    - **DHCPDISCOVER** : Diffusion pour détecter les serveurs DHCP.
    - **DHCPOFFER** : Réponse d'un serveur DHCP contenant une offre de configuration.
    - **DHCPREQUEST** : Demande du client pour prolonger ou conserver l'offre reçue.
    - **DHCPACK** : Acquittement du serveur pour confirmer l'attribution de l'adresse.
    - **DHCPDECLINE** : Indication que l'adresse IP proposée est déjà utilisée.
    - **DHCPRELEASE** : Le client libère son adresse IP.

- **Format du Message DHCP** :

    <img src="UNIX Images/image-28.png" style="border-radius: 7px;" width="400">

    - **Code d'Opération** : Type de message DHCP (1 pour requête, 2 pour réponse).
    - **Identificateur de Transaction** : Identifiant unique pour chaque transaction.
    - **Adresse IP Client** : Adresse IP du client.
    - **Votre Adresse IP** : Adresse IP attribuée au client.
    - **Adresse IP Serveur** : Adresse IP du serveur DHCP.
    - **Adresse IP Passerelle** : Adresse de la passerelle par défaut.
    - **Adresse Matérielle Client** : Adresse MAC du client.

### Détection et Offre

- **Détection d'un Serveur DHCP** :
    - Le client envoie un message DHCPDISCOVER pour trouver les serveurs DHCP disponibles.

    <img src="UNIX Images/image-29.png" style="border-radius: 7px;" width="400">

- **Offre de Configuration** :
    - Le serveur répond avec un message DHCPOFFER, proposant une configuration IP au client.

    <img src="UNIX Images/image-30.png" style="border-radius: 7px;" width="400">

### Le Relais DHCP

- **Rôle du Relais DHCP** :
    - Utilisé lorsque les clients et le serveur DHCP ne sont pas sur le même sous-réseau.
    - Le relais DHCP permet de transmettre les messages DHCP entre sous-réseaux, évitant la nécessité d'avoir un serveur DHCP sur chaque sous-réseau.

    <img src="UNIX Images/image-31.png" style="border-radius: 7px;" width="400">