## Chapitre 1: Introduction

> Ce chapitre sert à **introduire les concepts et méthodes de l'analyse et de la conception orientée objet** (OO), qui sont des éléments essentiels pour le développement structuré et efficace des systèmes logiciels.

---
### 1. **Crise du logiciel**

- **Problèmes rencontrés** à la fin des années 1970 :
    - Augmentation des **coûts** de développement.
    - Difficultés de **maintenance**.
    - Logiciels souvent **non fiables**.
    - Non-respect des **spécifications** et des **délais**.
- Ces défis ont conduit à la nécessité de **nouvelles méthodes**, donnant naissance au **génie logiciel**.

---

### 2. **Étude du Standish Group**

- Publication du **Rapport Chaos** (1994) :
    - **16,2%** des projets conformes aux prévisions initiales.
    - **52,7%** dépassent les coûts et les délais.
    - **31,1%** sont **abandonnés**.
- Met en évidence l'importance d'adopter des méthodes plus efficaces en génie logiciel.

---

### 3. **Génie logiciel**

- Vise à **maximiser** la réussite des projets grâce à :
    - **Méthodes**, **pratiques**, et **outils** efficaces.
- Objectif : Produire des logiciels au meilleur **rapport qualité/prix**.

---

### 4. **Cycle de vie d’un logiciel**

- Comprend les étapes clés suivantes :
    - **Définition des besoins** : Clarification des attentes du client (*besoins*).
    - **Analyse** : Traduction des besoins en un modèle clair (*LE-QUOI*: ce que le système doit faire).
    - **Conception** : Organisation du développement et choix technologiques (*LE-COMMENT* : comment le problème est résolu).
    - **Codage** : Écriture du code.
    - **Tests** : Vérification du bon fonctionnement du logiciel.
    - **Validation** : S'assurer de la conformité aux besoins.
    - **Déploiement** : Installation et configuration du logiciel.
    - **Maintenance** : Mises à jour et adaptations continues.

---

### 5. **Qu’est-ce qu’un modèle ?**

- Représentation **abstraite** d'une entité utilisée pour :
    - **Décrire**, **expliquer**, et **prévoir** des systèmes.
    - Aider à **comprendre**, **communiquer**, et **documenter**.

---

### 6. **Génie logiciel et la modélisation**

- La modélisation crée des représentations abstraites pour :
    - **Faciliter** la communication et la documentation.
    - **Clarifier** les besoins et organiser le développement.

| **Type de Modélisation** | **Exemples de Diagrammes**        | **Objectif**                                |
|---------------------------|-----------------------------------|---------------------------------------------|
| **Fonctionnelle**             | Cas d'utilisation, Activités     | Décrire les fonctionnalités et workflows    |
| **Structurelle**              | Classes, Composants              | Montrer la structure statique               |
| **Dynamique**                 | Séquences, États                 | Décrire le comportement et interactions     |
| **Données**                   | Entité-Association, Bases relationnelles | Modéliser l'organisation des données   |
| **Architecturale**            | Architecture logicielle, Déploiement | Représenter la vue d'ensemble          |
| **Processus Métiers**         | BPMN                             | Représenter les processus d'affaires        |


---

### 7. **Enjeux de la modélisation**

- **Simplification** du monde réel.
- Lien entre modèle et réalité via des **objets**.
- **Maîtrise** de la complexité et garantie de cohérence.
- Établissement d'un **langage commun** entre les parties prenantes.
    - **Maîtrise d'ouvrage (MOA)** : Représente les besoins métiers et les exigences des utilisateurs.
    - **Maîtrise d'œuvre (MOE)** : Assure la réalisation technique du projet.
- Respect des **contraintes techniques**.

---

### 8. **UML (Unified Modeling Language)**

- **Langage** de modélisation unifié avec :
    - **Notations graphiques** pour représenter des systèmes orientés objet.
    - Indépendance vis-à-vis des langages de **programmation**.
    - **Diagrammes** pour visualiser et documenter les systèmes.

---

### 9. **Les principales parties d’UML**

- **Vues** :
    - **Structurelle** : Décrit les composants et objets.
    - **Comportementale** : Montre les interactions et activités.
- **Diagrammes** : Représentations graphiques illustrant les différents aspects.
- **Éléments du modèle** : Concepts tels que **classes**, **objets**, **messages**.

---

### 10. **Diagrammes UML**

- 14 types de diagrammes regroupés par aspects :
    - **Fonctionnels** : Diagrammes de cas d'utilisation.
    - **Architecturaux (statique)** : Diagrammes de classes et de composants.
    - **Dynamiques** : Diagrammes d'interaction et d'états.

| **Concept**            | **Description**                                                                                      |
|------------------------|------------------------------------------------------------------------------------------------------|
| **Cas d'utilisation**   | Interactions entre le système et les utilisateurs.                                                  |
| **Activités**           | Modélisation des processus métier et des échanges de données.                                        |
| **Classes**             | Modélisation des classes, types, interfaces et relations entre eux.                                  |
| **Objets**              | Instances de classes.                                                                                 |
| **Machine à états**     | États des classes à travers leur cycle de vie.                                                      |
| **Interaction**         | Interactions entre des objets.                                                                       |
| **Composants**          | Rassemblement de classes ou de composants.                                                           |
| **Paquetage**           | Rassemblement d’éléments de modélisation.                                                            |
| **Déploiement**         | Unités d’installation, de configuration et de déploiement.                                           |

---

### 11. **Le modèle 4+1 vues de Kruchten**

- Organise la description d’un système en cinq vues :
    - **Logique** : Structure statique (classes, objets) [diagrammes de classes].
    - **Développement** : Organisation du code source [diagrammes de 
composants ou de packages].
    - **Processus** : Aspects dynamiques (interactions, comportements) [diagrammes de séquence et d'activités].
    - **Physique** : Déploiement sur le matériel [diagrammes de déploiement].
    - **Cas d’utilisation** : Scénarios d'utilisation des fonctionnalités.

---

### 12. **Principes de l’Orienté Objet**

- Concepts clés de la **programmation orientée objet** :
    - **Objet** : Entité modélisant un élément du monde réel.<br>
        - Types :
            - **concret** : le livre intitulé « Initiation à… »
            - **abstrait** : le compte bancaire n° 1915233C 
        - Caractéristiques :
            - **Identité** : Unique et attribuée à la création.
            - **État** : Valeurs des attributs, évolue avec le temps.
            - **Comportement** : Actions définies par des méthodes.

            `Objet = État + Comportement + Identité`

        - Cycle de vie :
            - **Construction** : Création en mémoire.
            - **Utilisation** : Modifications d'état et d'exécution de méthodes.
            - **Destruction** : Fin de l'objet.

    - **Classe** : La classe est un modèle ou un moule à partir duquel des objets (ou instances) sont créés.
        - Caractéristiques :
            - **Nom** : Identifiant de la classe.
            - **Attributs** : Propriétés ou variables associées à chaque objet.
            - **Méthodes** : Fonctions ou actions que les objets peuvent réaliser.
    - **Encapsulation** : Regroupement de données et méthodes, protection des données.
        - Niveaux de visibilité :
            - **Publique** : Moins de protection, accessible par toutes les classes.
            - **Protégée** : Accès limité aux méthodes des classes dérivées.
            - **Privée** : Niveau de protection maximal, l'accès est limité aux méthodes de la même classe.


    - **Héritage** : Création de nouvelles classes à partir d'existantes, favorisant la réutilisation.
        - Types :
            - **Simple** : Une seule classe dérivée d'une seule classe de base.
            - **Multiple** : Une classe dérivée hérite de plusieurs classes de base.
            - **Hiérarchique**	: Plusieurs classes dérivées d'une seule classe de base.
            - **Multiniveau** : Une chaîne d'héritage où chaque classe hérite de la précédente.
            - **Hybride** : Combinaison de l'héritage multiple et hiérarchique.
    - **Polymorphisme** : Méthodes pouvant avoir des comportements différents selon le contexte.
        - **Polymorphisme ad hoc** : Méthodes de même nom dans des classes sans relation.
        - **Polymorphisme d'héritage** : Redéfinition de méthodes dans les classes dérivées.
        - **Polymorphisme paramétrique** : Méthodes de même nom avec des paramètres différents.

---

## Chapitre 2: Diagramme de cas d’utilisation

> Ce chapitre explore la **modélisation des besoins** à l'aide des **diagrammes de cas d'utilisation (DCU)** en UML, outil essentiel pour organiser et définir les fonctionnalités d’un système en fonction des attentes des utilisateurs.

---

### 1. Modélisation des besoins

- La modélisation permet de structurer et d’organiser les **fonctionnalités attendues**.
- Elle aide à **faire l'inventaire des besoins**, en les organisant pour établir des relations (comme les réutilisations possibles).
- Le **diagramme de cas d'utilisation** (DCU) en UML est utilisé pour illustrer ces besoins, permettant de savoir précisément à quoi servira le système.

---

### 2. Diagramme de cas d’utilisation

- Définit les **éléments essentiels** d'un système, tels que :
    - Le système lui-même
    - Les **acteurs** (entités externes qui interagissent avec le système)
    - Les **cas d’utilisation** (fonctionnalités que le système doit fournir)
    - Les **liens** entre acteurs et cas d’utilisation (montrent les interactions spécifiques)
- Ce diagramme visualise les interactions entre le système et ses utilisateurs, facilitant la compréhension des fonctionnalités essentielles.

---

### 3. Acteurs

- Un **acteur** représente une entité externe (humain, périphérique, ou autre système) interagissant avec le système.
- Types d'acteurs :
    - **Humains** : Utilisateurs du logiciel via l’interface graphique.
    - **Périphériques** : Dispositifs matériels utilisés par le système.
    - **Autres systèmes** : Systèmes logiciels interagissant avec le système par API, ODBC, etc.
- L'identification des acteurs est cruciale, car elle détermine les rôles et interactions au sein du DCU.

---

### 4. Cas d’utilisation

- Les **cas d'utilisation** représentent des fonctionnalités spécifiques que le système doit offrir.
- Ils permettent de définir :
    - Le **comportement du système** sans spécifier comment chaque fonction est réalisée.
    - Les **limites du système** et les attentes des utilisateurs.
- Ce sont également des indicateurs de l'avancement du projet et de la validation des fonctionnalités via des tests.
---
### 5. Exemple:
<img src="UML Images/image-5.png" style="border-radius: 7px;" width="600">

---

### 6. Acteurs principaux et secondaires

- **Acteurs principaux** : Ceux qui initient les échanges dans un cas d’utilisation (par exemple, un client passant une commande).
- **Acteurs secondaires** : Ceux qui assistent le processus ou effectuent des tâches en soutien (souvent d'autres systèmes).

<img src="UML Images/image-6.png" style="border-radius: 7px;" width="400">

---

### 7. Relations de généralisation/spécialisation

- Les **relations de généralisation** permettent de structurer les acteurs et cas d’utilisation.
    - Un acteur ou un cas peut être une **spécialisation** d’un élément plus général, facilitant la gestion des rôles et des interactions.
- En UML, cela reflète le concept d’**héritage** dans la programmation orientée objet.

    Types de généralisation :
    - Entre les cas d’utilisation :
        
        <img src="UML Images/image-7.png" style="border-radius: 7px;" width="400">

    - Entre les acteurs :

        <img src="UML Images/image-8.png" style="border-radius: 7px;" width="400">
---

### 8. Relation d’inclusion

- le cas A inclut le cas B (B est une partie obligatoire de A)
- Implique le déclenchement automatique de B sans intervention 
externe.

<img src="UML Images/image-9.png" style="border-radius: 7px;" width="400">

le cas d’utilisation « Passer commande » implique que le client est déjà connecté. 

---

### 9. Relation d’extension

- le cas B étend le cas A (B est une partie optionnelle de A).
- B est un « cas spécial » de A qui ajoute une(des) fonctionnalité(s) optionnelle(s). 

<img src="UML Images/image-10.png" style="border-radius: 7px;" width="400">

Le cas d’utilisation «imprimer ticket de reçu» est cas optionnel 
qui étende le cas d’utilisation «effectuer une transaction»

---

### 10. Réutilisabilité

- Les relations d'inclusion et d'extension permettent de réutiliser les cas d'utilisation dans différents contextes, rendant le développement plus modulaire et évitant la duplication de code.

<img src="UML Images/image-11.png" style="border-radius: 7px;" width="400">

---

### 11. Décomposition des cas d’utilisation

- Les cas d'utilisation complexes peuvent être **décomposés** en cas plus simples via les relations d'inclusion et d'extension, facilitant la gestion et la compréhension des fonctionnalités.

    <img src="UML Images/image-12.png" style="border-radius: 7px;" width="400">
---

### 12. Conseils pour rester lisible

- Limiter chaque diagramme à **6 à 8 cas d'utilisation** pour éviter l’encombrement.
- Créer plusieurs diagrammes si nécessaire, et n’ajouter des relations qu’en cas de besoin.

---

### 13. Méthodologie de construction d’un DCU

- **Étapes principales** :
    - **Identifier les acteurs** : Principaux / Secondaires
    - **Hiérarchiser les acteurs** : généralisation / spécialisation.
    - **Associer acteurs et cas d'utilisation** : Relier chaque acteur aux cas d'utilisation correspondants.
    - **Structurer les cas d'utilisation** : Inclusion, Généralisation/Spécialisation et Extension.

---

### 14. Recensement des cas d’utilisation

- Identifier les cas d'utilisation pertinents du point de vue de chaque acteur, en évitant les redondances et en conservant un niveau d’abstraction adapté.
- **Exemple concret de cas d’utilisation** :
    > Un client peut effectuer un virement bancaire. Le transfert peut être un virement sur place ou par Internet. Le client doit être identifié (en fournissant son code d’accès) pour effectuer un virement, mais si le montant dépasse 500DH, la vérification du solde de son compte est réalisée
    >
    ><img src="UML Images/image-13.png" style="border-radius: 7px;" width="400">
---

### 16. Description textuelle

- Une description textuelle de chaque cas d’utilisation est recommandée

    **Structure de la Description Textuelle**
    - **Partie 1 - Identification :**
        - **Titre** : Nom du cas d’utilisation.
        - **Résumé** : Brève description du cas d’utilisation.
        - **Acteurs** : Identification des acteurs principaux et secondaires impliqués.
        - **Dates** : Date de création et mise à jour.
        - **Responsable** : Personne(s) responsable(s) du cas d’utilisation.
        - **Version** : Numéro de version du cas d’utilisation.
    - **Partie 2 - Scénarios** :
        - **Pré-conditions** : État du système avant l'exécution du cas d’utilisation.
        - **Scénario nominal** : Déroulement standard du cas d’utilisation.
        - **Scénarios alternatifs** : Variantes possibles du scénario standard.
        - **Scénarios d'exceptions** : Actions à prendre en cas d'erreur ou de situation exceptionnelle.
        - **Post-conditions** : État final du système après l'exécution du cas d'utilisation.
    - **Partie 3 - Contraintes Optionnelles** :
        - **Non fonctionnelles** : Exigences telles que la sécurité (fiabilité) et la confidentialité des données.
        - **Interface homme-machine** : Règles concernant l'interface utilisateur, comme la validation des actions importantes (par exemple, les opérations bancaires).

### exemple de description
### Cas d'Utilisation : Retirer de l'argent

1. **Identification**
    - **Titre** : Retirer de l'argent
    - **Résumé** : Ce cas d'utilisation permet à un porteur de carte bancaire de retirer de l'argent à un guichet automatique bancaire (GAB).
    - **Acteur principal** : Porteur de carte bancaire
    - **Acteurs secondaires** : Système d’Information de la banque, Système d’Autorisation Globale Carte Bancaire
    - **Date** : 18/09/2024
    - **Responsable** : Nom
    - **Version** : 1.0

2. **Description des Scénarios**

    **Pré-conditions** :
    - Le GAB contient des billets.
    - Les connexions avec le Système d'Autorisation et le Système d'Information de la banque sont opérationnelles.
    - Aucune carte ne se trouve coincée dans le lecteur.

    **Scénario Nominal** :
    - Le porteur de carte introduit sa carte dans le GAB.
    - Le GAB vérifie que la carte est valide.
    - Le GAB demande le code PIN.
    - Le porteur saisit son code PIN.
    - Le GAB vérifie le code et demande une autorisation au Système d'Autorisation.
    - Le système donne son accord et indique le crédit hebdomadaire.
    - Le GAB demande le montant désiré.
    - Le porteur saisit le montant.
    - Le GAB compare le montant au solde autorisé.
    - Le GAB demande si un ticket est souhaité.
    - Le porteur choisit de recevoir un ticket.
    - Le GAB éjecte la carte.
    - Le porteur récupère sa carte.
    - Le GAB délivre les billets et le ticket.
    - Le porteur prend le ticket et les billets.

    **Scénarios Alternatifs** :
    - A1 : Code erroné (1ère ou 2ème tentative).
    - A2 : Montant supérieur au crédit hebdomadaire.
    - A3 : Le porteur ne souhaite pas de ticket.

    **Scénarios d'Exception** :
    - E1 : Carte non valide.
    - E2 : Code erroné (3ème tentative).
    - E3 : Retrait non autorisé.
    - E4 : Carte non reprise.
    - E5 : Billets non récupérés.
    - E6 : Annulation de la transaction.

    **Post-conditions** :
    - Le GAB contient moins de billets.
    - Une transaction est enregistrée, même en cas d'échec.

3. **Contraintes Non Fonctionnelles**
    - Le code PIN ne doit pas s'afficher à l'écran.
    - Le compte du client est débité uniquement après la distribution des billets.

## Chapitre 3: Diagramme de classes et diagramme d’objets

> Ce chapitre explore la **modélisation de la structure statique** d'un système en utilisant des **diagrammes de classes** et **diagrammes d'objets**. Cette vue logique statique se concentre sur les éléments et relations qui ne changent pas au fil du temps.

---

### 1. Introduction

- Présentation de la **vue logique statique** qui capture la structure des objets du système indépendamment de leur dynamique.
- Outils principaux :
    - **Diagramme de classes** : représente la structure des classes et les relations entre elles.
    - **Diagramme d'objets** : montre les instances de classes et leurs relations dans un état spécifique.

---

### 2. Diagramme de classe

- **Vue abstraite des objets** du système permettant de visualiser les classes, leurs attributs, opérations, et les relations entre elles.
- Types de relations :
    - **Associations** : liens entre classes, telles que agrégation/composition.
    - **Héritage** : montre la généralisation/spécialisation entre classes.

---

### 3. Classe

- **Classe** : modèle abstrait décrivant une collection d’objets ayant des attributs (données) et des opérations (méthodes).
- Structure de classe :
    - **Nom unique** de la classe, **attributs** et **opérations** listés dans des compartiments du rectangle UML.
- Exemples d'attributs :

    <image src="UML Images/image-14.png" style="border-radius: 7px;" width="400">

---

### 4. Attributs

- **Définition** : propriétés caractérisant un objet, avec une syntaxe définissant leur visibilité et type.
- syntaxe : `<visibilité> <nom> : <type> = <valeur par défaut>`
    - Visibilité :
        - **Public** : `(+)` visible par tous.
        - **Privé** : `(-)` accessible uniquement par la classe.
        - **Protégé** : `(#)` accessible par la classe et ses sous-classes.
    - types :
        - **Primitifs** : types de base (entier, chaîne, booléen).
        - **Complexes** : classes ou types définis par l'utilisateur.
        - **Collections** : tableaux, listes, ensembles.
- **Attribut dérivé** : attribut calculé à partir d'autres attributs, précédé d'une barre oblique `(/)`.
- Types :
    - **Attribut d'instance** : spécifique à chaque instance d’une classe.
        - Syntaxe : `Visibilité attribut: type[= valeur initiale]`
    - **Attribut de classe** : commun à toutes les instances de la classe, noté en italique ou souligné.
        - Syntaxe : <u>`Visibilité attribut: type[= valeur initiale]`</u>

        <image src="UML Images/image-15.png" style="border-radius: 7px;" width="400">

---

### 5. Opérations

- **Opération** : action ou transformation que peut réaliser un objet, décrivant son comportement.
- Types d'opérations :
    - **Accesseurs/getters** et **modificateurs/setters** : pour accéder ou modifier l'état d'un objet.
    - **Constructeurs** : méthodes de création d’instances.
- Syntaxe : `Visibilité Nom_opération([arguments:type[=valeur initiale]]):type de résultat`

    <image src="UML Images/image-16.png" style="border-radius: 7px;" width="400">

- **note** : un symbole permettant de décrire des contraintes, des commentaires ou des algorithmes associés à un élément du modèle. 

    <img src="UML Images/image-17.png" style="border-radius: 7px;" width="400">

---

### 6. Relations entre classes

- Types de relations :
    1. **Association** :
        - **Définition** : Relation entre une ou plusieurs classes, représentant des liens logiques ou physiques.
        - Éléments clés :
            - **Nom** : Indique la nature de la relation.
            - **Sens de lecture** : Direction dans laquelle la relation est interprétée.

                <image src="UML Images/image-18.png" style="border-radius: 7px;" width="400">
            - **Degré** (arité) : Nombre de classes impliquées dans l'association (unaire, binaire, ternaire, n-aire).

                <img src="UML Images/image-20.png" style="border-radius: 7px;" width="400">
            - **Multiplicité** : Contraintes sur le nombre d'instances associées (min..max).

                <img src="UML Images/image-21.png" style="border-radius: 7px;" width="400">
            - **Rôle** : Décrit la fonction d'une classe dans l'association (utile pour relations réflexives).

                <img src="UML Images/image-22.png" style="border-radius: 7px;" width="400">
            - **Navigabilité** : Définit la direction d'accès entre classes (par défaut, bidirectionnel).

                <img src="UML Images/image-23.png" style="border-radius: 7px;" width="400">
            - **Réflexivité** : Une classe est associée à elle-même.

                <img src="UML Images/image-24.png" style="border-radius: 7px;" width="400">
            - **Classe-association** : Permet d'ajouter des attributs spécifiques à l'association.
                
                <img src="UML Images/image-19.png" style="border-radius: 7px;" width="400">
            - **Qualification** : Restreint la multiplicité selon une donnée précise.

                > <img src="UML Images/image-25.png" style="border-radius: 7px;" width="400">

                > Supposons que Grâce à l’attribut NomFichier de la classe Fichier, une instance de la classe Répertoire peut accéder à une instance de la classe Fichier
                >
                > <img src="UML Images/image-26.png" style="border-radius: 7px;" width="400">
                >
                > En connaissant le nom de fichier, il y’a un seul fichier
        - Sous-types :
            - **Agrégation** : Relation "partie-tout" où les composants sont séparables (losange vide).

                > <img src="UML Images/image-27.png" style="border-radius: 7px;" width="400">
                >
                >La suppression d’une équipe n’implique pas la suppression des personnes qui la composent.
            - **Composition** : Relation forte où les composants dépendent de l'existence de l'agrégat (losange plein).

                >la destruction de l’agrégat (ou conteneur) implique automatiquement la destruction de tous les composants liés.
                >
                > <img src="UML Images/image-28.png" style="border-radius: 7px;" width="400">
    2. **Généralisation/Spécialisation** :
        - **Définition** : Relation hiérarchique entre une classe générale (super-classe) et une ou plusieurs classes spécialisées (sous-classes).
        - Éléments clés :
            - **Généralisation** : Met en facteur les caractéristiques communes de plusieurs classes dans une super-classe.
            - **Spécialisation** : Ajoute des détails spécifiques aux sous-classes.

                <img src="UML Images/image-29.png" style="border-radius: 7px;" width="400">
            - **Notation** : Représentée par un triangle pointant vers la super-classe.
        - Caractéristiques des sous-classes :
            - Héritent des attributs et méthodes de la super-classe.
            - Peuvent ajouter leurs propres attributs et méthodes.
            - Peuvent redéfinir les comportements hérités (surcharge).
        - **Perspective** :
            - **Top-down** : Spécialisation pour définir des sous-classes.
            - **Bottom-up** : Généralisation pour regrouper les caractéristiques communes.
        - **Polymorphisme** :
            - Les sous-classes partagent des opérations de même nom, mais avec des comportements spécifiques.
                
            <img src="UML Images/image-30.png" style="border-radius: 7px;" width="400">
        - **Héritage multiple** : Une classe peut hériter de plusieurs super-classes.

            <img src="UML Images/image-31.png" style="border-radius: 7px;" width="400">
    3. **Dépendance** :
        - **Définition** : Relation unidirectionnelle où un élément source dépend d'un élément cible.
        - Caractéristiques :
            - Une modification dans l’élément cible peut affecter l’élément source.
            - Représentée par un trait discontinu avec une flèche pointant vers l’élément cible.
            - Exemple : si le cours change, l’emploi du temps change.

                <img src="UML Images/image-32.png" style="border-radius: 7px;" width="400">

---

### 7. Classes spéciales

- **Classe abstraite** : 
    - Définition : Une classe abstraite contient au moins une méthode abstraite (méthode dont seule la signature est définie, sans implémentation).
        - Une méthode abstraite est une opération non définie dans la classe mère mais destinée à être implémentée par ses sous-classes.
    - Caractéristiques :
        - Une classe abstraite ne peut pas être instanciée.
        - Elle sert de modèle pour ses classes filles qui doivent compléter sa spécification.
        - Le nom d'une classe abstraite est écrit en **italique** ou accompagné du stéréotype `<<abstract>>`.
    - Exemple UML :

        <img src="UML Images/image-33.png" style="border-radius: 7px;" width="400">

- **Interface** : Une interface est une classe spéciale où toutes les méthodes sont abstraites.
    - Elle représente une liste d'opérations ou un contrat que les classes implémentant cette interface doivent respecter.
    - Caractéristiques :
        - Une interface ne peut pas être instanciée.
        - Elle décrit de manière abstraite le comportement attendu d'une classe qui l'implémente.
        - Une classe peut implémenter plusieurs interfaces, permettant une forme d'héritage multiple.
        - En UML, une interface est notée avec le stéréotype <<interface>> ou un symbole spécifique.
    - Exemple UML :

        <img src="UML Images/image-34.png" style="border-radius: 7px;" width="400">

---

### 8. Concepts avancés des associations
1. Contraintes et invariants
    - Définition :
        - Les contraintes sont des propriétés qui doivent être vérifiées à tout moment lors de l’exécution du système.
        - Elles permettent de définir des règles à respecter, notamment lors du passage à l’implémentation.
    - Représentation :
        - Les contraintes sont placées entre accolades (`{}`) et peuvent être exprimées sous forme de :
            - Notes dans le diagramme.
            - Texte accompagnant le diagramme.
            - OCL (Object Constraint Language), un langage formel associé à UML.
    - Elles peuvent s’appliquer à :
        - Les valeurs des attributs.
        - Les conditions sur les associations.
        - Les relations entre attributs.
2. Contraintes sur les associations
    >Les contraintes permettent d’imposer des relations spécifiques entre objets associés. Voici les contraintes les plus courantes :
    - Contrainte `{ordonné}`
        - Les objets sont ordonnés selon un critère précis.
        - Exemple : 

            <img src="UML Images/image-35.png" style="border-radius: 7px;" width="200">
    - Contrainte `{sous-ensemble}`
        - Indique qu’une collection est incluse dans une autre.
        - Nécessite au moins deux relations.
        - Exemple : 

            <img src="UML Images/image-36.png" style="border-radius: 7px;" width="400">
    - Contrainte `{xor}`
        - Indique que parmi un groupe d’associations, une seule est valide à la fois.
        - Exemple :

            <img src="UML Images/image-37.png" style="border-radius: 7px;" width="300">
    - Contrainte `{addOnly}`
        - Autorise uniquement l’ajout de nouveaux objets, sans possibilité de suppression ou de mise à jour.
        - Exemple : 

            <img src="UML Images/image-38.png" style="border-radius: 7px;" width="300">
    - Contrainte `{frozen}`
        - Interdit l’ajout, la suppression ou la mise à jour des liens d’un objet une fois initialisé.
        - Exemple : La contrainte {frozen} est utilisée pour indiquer qu'une fois qu'un lien de parenté est défini entre un parent et un enfant, ce lien est figé et ne peut pas être modifié.

            <img src="UML Images/image-39.png" style="border-radius: 7px;" width="300"> 
3. Utilité des contraintes en UML
    - Modélisation précise : Elles garantissent la cohérence des relations entre classes.
    - Conception robuste : Elles permettent de réduire les erreurs lors de l’implémentation en spécifiant les comportements autorisés.
    - Documentation claire : Les diagrammes deviennent plus explicites avec des contraintes décrites directement.

---

### 9. Diagramme de classes : Méthodologie
**Étapes principales** :
- **Analyse du texte** :
    - Identifier les noms (potentielles classes métier).
    - Identifier les verbes qui relient ces noms (potentielles associations).
- **Construction initiale** :
    - Créer un premier diagramme de classes en incluant les noms identifiés comme classes.
- **Ajout des associations** :
    - Enrichir le diagramme avec les associations trouvées dans le texte.
- **Affinage** :
    - Supprimer les associations redondantes.
    - Rechercher des relations généralisation/spécialisation (hiérarchie).
    - Identifier les relations d'agrégation ou de composition.
- **Multiplicités** :
    - Ajouter les multiplicités pour préciser les relations (exemple : 1..*).
- **Ajout des attributs et opérations** :
    - Ajouter les attributs et opérations aux classes pour refléter leurs propriétés et comportements.
- **Validation** :
    - Vérifier que tous les concepts métier sont bien représentés.
    - S'assurer que le diagramme permet de réaliser tous les cas d’utilisation.

---

### 10. Diagramme d’objets
**Définition** :
- Représente les objets (instances de classes) et leurs liens (instances d’associations) dans un système à un instant donné.

**Caractéristiques** :
- **Structure** :
    - Les objets sont reliés par des liens, similaires aux associations du diagramme de classes.
    - Les liens sont une instance d’une association.
    - Les noms des objets sont soulignés et précédés de `:` (par exemple: `:NomDeClasse`).
- **Différences avec le diagramme de classes** :
    - Pas de multiplicités : Elles n’ont pas de sens au niveau des objets.
    - Représente une vue spécifique et concrète du système.
- **Utilité** :
    - Aide à comprendre ou illustrer des parties complexes d’un diagramme de classes.
    - Fournit un exemple concret du fonctionnement d’un système.

Exemple de notation :
- Objet : `nomObjet:NomClasse`
- Lien entre objets : Instance d’association (nom de l’association souligné si elle est nommée).

    <img src="UML Images/image-40.png" style="border-radius: 7px;" width="400">

---

## Chapitre 4 :
## 1: Diagramme de séquences

>Ce chapitre traite de la **modélisation dynamique** des systèmes à l'aide des diagrammes UML pour capturer les interactions, les comportements et les changements dans le temps.

### 1. Introduction

- La modélisation dynamique complète la modélisation statique en ajoutant une dimension temporelle.
- Objectifs :
    - Décrire **comment les objets interagissent**.
    - Montrer l’**évolution du système** dans le temps.

### 2. Modèle Dynamique

- Utilisé pour modéliser le **comportement dynamique** d’un système.
- Basé sur plusieurs diagrammes UML :
    - **Diagrammes de séquences** : représentent les interactions entre objets pour chaque scénario.
    - **Diagrammes de communication** : illustrent la collaboration entre objets.
    - **Diagrammes d’état** : décrivent le comportement d’un objet selon ses états.
    - **Diagrammes d’activités** : décrivent les flux de traitement ou workflows.

    <img src="UML Images/image-41.png" style="border-radius: 7px;" width="400">

### 3. Diagramme de séquences

- Type de diagramme dynamique qui modélise les **interactions temporelles**.
- Utilisé pour décrire une instance d’un cas d’utilisation.
- Concepts principaux :
    - **Objets** : Entités participantes représentées par des rectangles avec des lignes de vie.
    - **Ligne de vie** : Représente la durée d’existence d’un objet dans une séquence.
    - **Messages** : Interactions entre objets représentées par des flèches.
        - La forme d’un message est : `[condition] message (paramètres)`.

    <img src="UML Images/image-42.png" style="border-radius: 7px;" width="400">

### 4. Messages dans un diagramme de séquences

- **Messages simples** : Communication standard sans critère spécifique.

    <img src="UML Images/image-43.png" style="border-radius: 7px;" width="300">
- **Messages minutés (Timeout)** : Bloque l’expéditeur pendant un délai.
    - **Exemple** : La porte d’un ascenseur s’ouvre pendant un certain délai avant d’être refermée.

    <img src="UML Images/image-44.png" style="border-radius: 7px;" width="300">
- **Messages synchrones** : Bloque l’expéditeur jusqu'à réponse du récepteur.

- **Messages asynchrones** : Non bloquants, le récepteur traite le message à son rythme.

    <image src="UML Images/image-45.png" style="border-radius: 7px;" width="300">
- **Messages récursifs (réflexive)** : Messages qu’un objet s’envoie à lui-même.

    <img src="UML Images/image-46.png" style="border-radius: 7px;" width="300">

- **Message perdu (Lost Message)** : Un message dont l’émetteur est connu, mais le récepteur est hors de portée du diagramme.
- **Message trouvé (Found Message)** : Un message dont le récepteur est connu, mais l’émetteur est inconnu ou non représenté dans le diagramme.

    <img src="UML Images/image-47.png" style="border-radius: 7px;" width="300">
### 5. Création et suppression de participants

- **Création d’un objet** : Indiquée par une flèche pointant vers le sommet de la ligne de vie.
- **Destruction d’un objet** : Représentée par une croix en bas de la ligne de vie.

<img src="UML Images/image-48.png" style="border-radius: 7px;" width="400">

### 6. Fragments dans un diagramme de séquences
**Concepts généraux** :
- **Définition** : Un fragment est une portion du diagramme encadrée par un rectangle avec un pentagone dans le coin supérieur gauche. Le pentagone indique le type de fragment.
- Types courants de fragments :
    - `alt` : alternative.
    - `loop` : boucle.
    - `opt` : option.
    - Autres : `ref`, `par`, etc.

    <img src="UML Images/image-49.png" style="border-radius: 7px;" width="400">

**Types de fragments et leur utilisation** :
- Fragment `loop` :
    - Représente une boucle (similaire aux boucles `for` ou `while`).
    - La séquence est exécutée tant qu’une condition de garde est vraie.
    - Exemple : `loop[2, 5, code=true]` signifie que la séquence est exécutée deux fois obligatoires, et jusqu’à trois fois supplémentaires si `code=true`.

    <img src="UML Images/image-50.png" style="border-radius: 7px;" width="400">
- Fragment `opt` :
    - Utilisé pour une interaction conditionnelle unique.
    - La séquence n’est exécutée que si la condition de garde est satisfaite.

    <img src="UML Images/image-51.png" style="border-radius: 7px;" width="400">
- Fragment `alt` :
    - Représente des alternatives conditionnelles multiples.
    - Chaque condition est associée à un opérande. Si aucune condition n’est satisfaite, l’opérande `else` est exécuté (si défini).

    <img src="UML Images/image-52.png" style="border-radius: 7px;" width="400">
- Différences entre `alt` et `opt` :
    - `opt` : Comporte un seul opérande, exécuté uniquement si la condition est vraie.
    - `alt` : Comporte plusieurs opérandes, où la première condition vraie détermine l’exécution.
- Fragment `ref` :
    - Fait référence à un autre diagramme de séquences.
    - Permet de simplifier les diagrammes en évitant les duplications d’informations.

    <img src="UML Images/image-53.png" style="border-radius: 7px;" width="400">
- Fragment `par` :
    - Utilisé pour représenter des traitements concurrents.
    - Les sous-fragments s’exécutent simultanément, séparés par des pointillés.

    <img src="UML Images/image-54.png" style="border-radius: 7px;" style="border-radius: 7px;" width="400">

**Autres fragments** :
- `ignore` : Fragments facultatifs.
- `critical` : Sections critiques ne devant pas être interrompues.
- `break` : Fragments représentant des scénarios exceptionnels ou de rupture.
- `assert` : Fragments où les paramètres du message sont prédéfinis.
- `seq` : Sous-fragments exécutables dans n’importe quel ordre (pas simultanément).
- `strict` : Messages respectant un ordre précis.
- `neg` : Indique que la séquence à l’intérieur du fragment est invalide.

### 7. Relation avec d’autres diagrammes

- Les diagrammes de séquences sont souvent combinés avec les diagrammes de classes pour valider la cohérence des interactions et des structures statiques.

    <img src="UML Images/image-55.png" style="border-radius: 7px;" style="border-radius: 7px;" width="400">


---

## 2: Diagramme de communication
### 1. Définition et rôle :
- Le diagramme de communication est un diagramme dynamique UML qui illustre les interactions entre différents participants d’un système.
- Il est aussi appelé diagramme de collaboration dans UML1.
- Version simplifiée d’un diagramme de séquence, il se concentre davantage sur les relations et les échanges entre les participants que sur l’ordre exact des messages.
- **Composants** :
    - Les **sommets** représentent les **objets** ou les **acteurs**.
    - Les **arêtes** représentent les **messages échangés**.
### 2. Composants principaux :
**Participants** :
- Identiques aux participants des diagrammes de séquence.
- Représentés par un rectangle contenant le nom du type (objet, acteur).
- Ne possèdent pas de ligne verticale pointillée comme dans le diagramme de séquence.

**Lien d’interaction (connecteur)** :
- Ligne continue entre deux participants.
- Indique qu’une communication peut exister entre ces participants.
- Peut inclure une multiplicité pour montrer combien de connexions existent.

<img src="UML Images/image-70.png" style="border-radius: 7px;" width="400">

**Message** :
- Représenté par une flèche pleine :
    - Flèche simple pour un message asynchrone.
    - Flèche avec une tête fermée pour un message synchrone.

    <img src="UML Images/image-71.png" style="border-radius: 7px;" width="400">
- Peut inclure :
    - **Ordre** (numérotation).

        <img src="UML Images/image-72.png" style="border-radius: 7px;" width="300">
    - **Condition de franchissement** (ex. : **[condition]**).

        <img src="UML Images/image-73.png" style="border-radius: 7px;" width="300">
    - **Boucle** (**[for each item]**, **[while condition]**).
    - **Valeur de retour** (optionnelle, représentée par une flèche en pointillés).
    - **Messages récursifs** (un participant s’envoie un message à lui-même).

        <img src="UML Images/image-74.png" style="border-radius: 7px;" width="300">
### 3. Spécificités des messages :
- **Message conditionné** : Ajout de conditions au message.
- **Messages simultanés** : Identifiés par un même numéro de séquence avec des lettres suffixées (ex. : 1a, 1b).
- **Message de retour** : Utilise une flèche pointillée pour indiquer une réponse ou un retour.

    <img src="UML Images/image-75.png" style="border-radius: 7px;" width="400">
- **Boucles** : Indiquées par des conditions spécifiques ou des annotations.

### 4. Différences entre diagrammes de séquence et de communication :

| **Caractéristique**            | **Diagramme de séquence (DS)**       | **Diagramme de communication (DC)**       |
|----------------------------|----------------------------------|---------------------------------------|
| **Objectif principal**         | Montrer l’ordre des interactions | Montrer les participants et leurs liens |
| **Structure visuelle**         | Représente le temps avec des lignes verticales | Montre des liens visuels directs       |
| **Gestion des itérations**     | Utilise des fragments           | Utilise une numérotation des messages |
| **Complexité de construction** | Plus détaillé, demande plus d’efforts | Plus simple à construire et adapter   |

<img src="UML Images/image-76.png" style="border-radius: 7px;" width="500">

### 5. Cas d'utilisation :
- **Diagramme de séquence** :
    - Utile pour les processus complexes nécessitant un ordre précis des interactions.
    - Recommandé pour montrer les itérations, les conditions, et les messages asynchrones.
- **Diagramme de communication** :
    - Idéal pour des interactions simples avec un focus sur les liens entre participants.
    - Plus proche du diagramme de classes UML pour les relations visuelles.

## Chapitre 5: Diagramme d’activités

>Ce chapitre explore le **diagramme d’activités** en UML, utilisé pour modéliser les flux de contrôle d’un processus ou d’une activité. Il illustre les étapes, décisions, boucles et parallélismes dans un système.

### 1. Introduction

- Le diagramme d'activités représente le **déroulement d’un processus** ou d'une activité sous forme de flux de contrôle.
- Utilisé pour :
    - Décrire les **actions et décisions**.
    - Modéliser des **boucles** et des **flux parallèles**.

    <img src="UML Images/image-56.png" style="border-radius: 7px;" style="border-radius: 7px;" width="400">

---

### 2. Objectifs des diagrammes d’activités

1. **Support à la conception logicielle** :
    
    - Guider la conception des fonctionnalités et comportements d’un système.
    - Décrire les **algorithmes complexes** avant implémentation.
2. **Analyse et optimisation des processus** :
    
    - Détecter les inefficacités, doublons ou goulets d’étranglement.
    - Identifier des opportunités d’**automatisation**.
3. **Modélisation des processus métier** :
    
    - Illustrer les workflows (exemple : processus de commande ou réservation).
    - Identifier les **dépendances** entre tâches.

---

### 3. Différences avec d'autres diagrammes UML

- **Diagrammes de cas d’utilisation** : Répondent à la question "Quoi ?", tandis que les diagrammes d’activités montrent "Comment ?".
- **Diagrammes de séquences** : Les diagrammes d'activités se concentrent sur le **flux de processus**, alors que les diagrammes de séquences modélisent la communication entre objets avec une chronologie précise.

---

### 4. Éléments de notation UML spécifiques

1. **Nœud de départ** : Indique le début d’un flux (cercle noir rempli).

    <img src="UML Images/image-57.png" style="border-radius: 7px;" width="80">
2. **Nœud de fin** : Marque la fin d’un processus.

    <img src="UML Images/image-58.png" style="border-radius: 7px;" width="80">
3. **Action** : Représente une tâche simple ou opération (exemple : "Faire commande").

    <img src="UML Images/image-59.png" style="border-radius: 7px;" width="110">
4. **Transition** : Montre le passage d'une action à une autre.

    <img src="UML Images/image-60.png" style="border-radius: 7px;" width="250">
5. **Activité** : Modélise un ensemble d’actions ou un processus complexe.

    <img src="UML Images/image-61.png" style="border-radius: 7px;" width="250">
6. **Décision** : Noeud conditionnel où le flux peut diverger (losange).

    <img src="UML Images/image-62.png" style="border-radius: 7px;" width="250">
7. **Convergence** : Réunit plusieurs chemins d'exécution.

    <img src="UML Images/image-63.png" style="border-radius: 7px;" width="250">
8. **Itération** : Représente des boucles sur des actions ou activités.

    <img src="UML Images/image-64.png" style="border-radius: 7px;" width="250">
9. **Synchronisation (Fork et Join)** :
    - **Fork** : Division d’un flux en sous-flux parallèles.
    - **Join** : Synchronisation des flux parallèles en un flux unique.

    <img src="UML Images/image-65.png" style="border-radius: 7px;" width="250">
10. **Fin locale** : Termine une branche sans affecter le processus global.

    <img src="UML Images/image-66.png" style="border-radius: 7px;" width="250">
11. **Object Node** : Représente les objets produits ou consommés par une action.

    <img src="UML Images/image-67.png" style="border-radius: 7px;" width="250">

---

### 5. Événements

- **Signal reçu** : Déclenche un traitement dans le processus.
- **Signal envoyé** : Émet un résultat ou message externe.

<img src="UML Images/image-68.png" style="border-radius: 7px;" width="350">

---

### 6. Partitions (Couloirs d’activités)

- Permettent de **délimiter les responsabilités** dans un processus.
- Chaque activité est attribuée à une **ressource** (acteur ou système externe) dans un couloir.

<img src="UML Images/image-69.png" style="border-radius: 7px;" width="350">
