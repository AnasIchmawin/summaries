# Résumé JEE

## Chapitre 1:

> Ce chapitre sert à introduire les concepts fondamentaux de Java EE (Enterprise Edition), une plateforme essentielle pour le développement d'applications d'entreprise. En expliquant les bases de l'architecture Java EE et de ses composants
> 

---

### 1. **Objectifs de Java EE**

- Comprendre l'architecture de la plateforme Java EE.
- Utiliser Java EE pour développer des applications d'entreprise multi-tiers.
- Maîtriser les frameworks Java EE : JSF (pages dynamiques), EJB (couche métier) et JPA (couche de persistance).

---

### 2. **Exigences d'un Projet Informatique**

- **Fonctionnelles** : Répondre aux besoins métiers de l'entreprise.
- **Techniques** :
    - **Performance** : Temps de réponse rapide, haute disponibilité, tolérance aux pannes.
    - **Maintenance** : Évolutif et extensible.
    - **Sécurité** : Protection des données sensibles.
    - **Portabilité** : Compatibilité multi-plateformes.
    - **Communication** : Supporte l'intégration avec d'autres applications et services

---

### 3. **Introduction à Java**

- **Java** : Langage orienté objet et semi-compilé (bytecode interprété par la JVM).
- **JVM (Java Virtual Machine)** : Permet la portabilité, sécurité et performance.
- **JRE (Java Runtime Environment)** : Exécute les programmes Java.
- **JDK (Java Development Kit)** : Contient les outils pour compiler et exécuter le code Java.

---

### 4. **Architecture Multi-Tiers**

- **Principe** : Diviser l'application en couches distinctes pour mieux organiser le code.
- **Couches Principales** :
    - **Web (Frontend)** : Interface utilisateur.
    - **Métier (Backend)** : Logique métier, traitement des données.
    - **DAO (Data Access Object)** : Gestion de l'accès aux données et interactions avec la base de données.

---

### 5. **Serveurs Web et Serveurs d'Applications**

- **Serveur Web** : Gère les requêtes HTTP et les ressources statiques (HTML, images, CSS).
- **Serveur d'Applications** : Environnement d'exécution complet pour la logique métier (transactions, sécurité, persistance).

---

### 6. **Java EE : Définition et Historique**

- **Java EE** : Plateforme pour développer des applications d'entreprise évolutives et distribuées.
- **Historique** :
    - **Java EE 1.2** (1999) : Première version de Java EE avec Servlets, JSP, EJB, etc.
    - **Jakarta EE** (depuis 2018) : Java EE transféré à la Fondation Eclipse, renommé Jakarta EE.

---

### 7. **Composants de Java EE**

- **Clients Web** : Pages HTML, XML, et applications Java (Applets).
- **Composants Serveur** :
    - **Servlets** : Gèrent les requêtes et réponses HTTP.
    - **JSP (JavaServer Pages)** : Génèrent des pages dynamiques en HTML.
    - **JSF (Java Server Faces)** : Framework pour les applications Web.
    - **EJB (Enterprise JavaBeans)** : Encapsulent la logique métier et assurent la gestion des transactions et sécurité.
    - **Entités (Beans)** : Utilisés pour la persistance des données.

---

### 8. **Conteneurs Java EE**

- **Conteneur de Servlets** : Exécute les servlets, gère leur cycle de vie et les sessions.
- **Conteneur EJB** : Gère les EJB, la logique métier et les transactions.
- **Conteneur de Persistance** : Gère les opérations de persistance via l’API JPA.
- **Conteneur de Message** : Gère la communication asynchrone via JMS (Java Message Service).

---

### 9. **Structure et Déploiement d'une Application Java EE**

- **Structure en Modules** :
    - **Module Web (.war)** : Contient les ressources Web (HTML, JSP, classes, bibliothèques).
    - **Module EJB (.jar)** : Inclut les classes EJB, avec le descripteur `ejb-jar.xml`.
    - **Module Entreprise (.ear)** : Archive globale pour les applications d'entreprise, contenant les modules `.war` et `.jar`.
- **Déploiement** : En utilisant des fichiers `.war`, `.jar`, ou `.ear` avec un fichier descripteur XML.

---

### 10. **Architecture MVC dans Java EE**

- **Modèle-Vue-Contrôleur (MVC)** : Motif de conception pour organiser le code :
    - **Modèle** : Gère les données de l'application.
    - **Vue** : Affiche l'interface utilisateur.
    - **Contrôleur** : Intermédiaire entre la vue et le modèle, gère les interactions de l’utilisateur.
- **Application Java EE en MVC** : Les servlets agissent comme contrôleurs, les JSP comme vues, et les EJB gèrent la logique métier dans le modèle.

---

### 11. **Avantages de Java EE**

- **Modularité et Réutilisabilité** : Code organisé et réutilisable.
- **Évolutivité et Performance** : Gère efficacement de nombreux utilisateurs.
- **Interopérabilité et Services Web** : Compatibilité avec d’autres systèmes via des API standardisées.
- **Gestion des Transactions et Persistance des Données** : Garantit l’intégrité des données.
- **Sécurité** : Contrôle des accès et protection des données.

---

## Chapitre 2:

> Ce chapitre sert à introduire les servlets, un composant central de Java EE, et à expliquer leur rôle dans le développement d'applications web dynamiques côté serveur
> 

---

### 1. **Introduction aux Servlets**

- **Définition** : Un servlet est un composant Java côté serveur, exécuté dans un conteneur de servlets (comme Tomcat), qui reçoit les requêtes HTTP, les traite et renvoie des réponses HTTP dynamiques.
- **Fonctionnalités** :
    - **Créer des applications dynamiques** : Génère des réponses HTML basées sur les requêtes des utilisateurs.
    - **Collecter des entrées** : Gère les soumissions de formulaires HTML.
    - **Accès aux bases de données** : Peut interagir avec des bases pour présenter ou mettre à jour des enregistrements.

---

### 2. **Avantages des Servlets**

- **Portabilité** : Indépendant des plateformes, exécutable sur n'importe quel serveur compatible Java EE.
- **Efficacité** :
    - Semi-compilé pour une exécution rapide.
    - Supporte la gestion de cache et les connexions persistantes.
- **Puissance** :
    - Communication bidirectionnelle avec le serveur.
    - Partage de données et chaînage entre servlets.
- **Modularité** : Permet d’organiser le code en plusieurs servlets, chaque servlet gérant une tâche spécifique (ex. affichage, traitement des formulaires).
- **Gestion des sessions et des cookies** : Suivi des sessions pour garder l’état des utilisateurs sur plusieurs requêtes.

---

### 3. **Fichier `web.xml` (Descripteur de déploiement)**

- **Fonction** : Configure les servlets, leurs mappages d’URL, et d'autres paramètres comme les filtres et pages d'erreur.
- **Localisation** : Situé dans le dossier `WEB-INF`.
- **Exemple de Configuration** :
    
    ```xml
    <servlet>
       <servlet-name>MyServlet</servlet-name>
       <servlet-class>com.example.MyServlet</servlet-class>
    </servlet>
    <servlet-mapping>
       <servlet-name>MyServlet</servlet-name>
       <url-pattern>/myPath</url-pattern>
    </servlet-mapping>
    ```
    

---

### 4. **API de Servlet : Interfaces et Classes Principales**

- **Servlet** : Interface de base de chaque servlet, qui définit les méthodes `init()`, `service()`, `destroy()`.
- **GenericServlet** : Classe abstraite, simplifie la création de servlets indépendants du protocole HTTP.
- **HttpServlet** : Spécialisée pour les requêtes HTTP, avec des méthodes pour chaque type de requête (`doGet()`, `doPost()`, `doPut()`, etc.).

---

### 5. **API de Servlet : Gestion des Requêtes et Réponses**

- **ServletRequest** : Représente la requête du client, permet d’accéder aux données envoyées par le client (ex. paramètres de formulaire).
    - Méthodes importantes :
        - `getParameter(String name)`: Récupère les paramètres de l’URL ou du formulaire.
        - `getHeader(String name)`: Récupère des informations d’en-tête de requête.
- **HttpServletRequest** : Spécifique à HTTP, ajoute la gestion des cookies et des sessions.
    - Méthodes importantes : `getCookies()`, `getSession()`.
- **ServletResponse** : Permet à la servlet de générer et d’envoyer la réponse HTTP.
    - Méthodes importantes :
        - `setContentType(String type)`: Définit le type MIME de la réponse.
        - `getWriter()`: Retourne un objet PrintWriter pour envoyer du texte au client.
- **HttpServletResponse** : Méthodes supplémentaires pour HTTP :
    - `sendRedirect(String location)`: Redirection vers une autre URL.
    - `setStatus(int sc)`: Définir le code de statut de la réponse (ex. 404 Not Found, 200 OK).

---

### 6. **Contextes et Configuration**

- **ServletContext** : Contexte global de l'application, permettant de partager des données entre les servlets d’une même application.
    - **Méthodes clés** :
        - `setAttribute(String name, Object value)`: Stocke un attribut accessible globalement.
        - `getInitParameter(String name)`: Récupère un paramètre d'initialisation global.
- **ServletConfig** : Contient la configuration propre à chaque servlet (paramètres spécifiques définis dans `web.xml`).
    - **Méthodes** :
        - `getServletName()`: Retourne le nom de la servlet.
        - `getInitParameter(String name)`: Récupère les paramètres spécifiques à la servlet.

---

### 7. **Gestion des Sessions : HttpSession**

- **Utilisation** : Conserve des données pour chaque utilisateur, permettant la persistance de l’état.
- **Méthodes importantes** :
    - `setAttribute(String name, Object value)`: Enregistre un objet dans la session.
    - `getAttribute(String name)`: Récupère un objet stocké.
    - `invalidate()`: Supprime la session et efface les données associées.

---

### 8. **Cycle de Vie d'une Servlet**

- **Étapes** :
    1. **Charger la classe Servlet** : Le serveur lit le fichier `web.xml` et charge la classe définie.
    2. **Créer une instance** : Une seule instance est créée et partagée par les requêtes concurrentes.
    3. **Appeler `init()`** : Initialise la servlet avec les configurations de `ServletConfig`.
    4. **Appeler `service()` pour chaque requête** :
        - Identifie le type de requête (GET, POST).
        - Appelle la méthode appropriée (`doGet`, `doPost`).
    5. **Appeler `destroy()`** : Termine la servlet, nettoie les ressources (base de données, threads, etc.).

---

### 9. **Développement d’une Servlet**

- **Étapes** :
    1. Créer une classe qui hérite de `HttpServlet`.
    2. Redéfinir `doGet()` ou `doPost()` pour répondre aux requêtes.
    3. Configurer la servlet dans `web.xml` ou utiliser l’annotation `@WebServlet`.
- **Exemple de Code Servlet** :
    
    ```java
    @WebServlet("/hello")
    public class HelloServlet extends HttpServlet {
        protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
            response.setContentType("text/html");
            PrintWriter out = response.getWriter();
            out.println("<h1>Hello, World!</h1>");
        }
    }
    ```
    

---

### 10. **Interaction avec les Formulaires HTML**

- **Envoi des données vers une servlet** :
    - Définir la servlet destinataire avec l’attribut `action` du formulaire.
    - Spécifier la méthode HTTP (`POST` ou `GET`) dans l’attribut `method`.
- **Exemple HTML** :
    
    ```html
    <form action="/hello" method="POST">
       <input type="text" name="username" />
       <button type="submit">Envoyer</button>
    </form>
    ```
    

---

### 11. **Type MIME**

- **Définition** : Standard qui informe le navigateur sur le type de contenu, permettant de traiter correctement les données.
- **Exemples courants** :
    - `text/html` pour le HTML.
    - `application/json` pour des données JSON.

---

## Chapitre 3:

> Ce chapitre sur les JavaServer Pages (JSP) introduit les concepts clés nécessaires pour créer des applications web dynamiques avec Java
> 

---

### 1. **Introduction aux JSP**

- **Définition** : Les JSP sont des pages HTML enrichies de code Java pour créer du contenu dynamique côté serveur.
- **Fonctionnement** : Les JSP permettent d’intégrer du code Java dans des pages HTML en utilisant des balises spéciales. Elles sont traitées sur le serveur et compilées en servlets.
- **Utilisation** : Répondent aux requêtes HTTP et servent à générer des pages dynamiques.

---

### 2. **Cycle de Vie d'une JSP**

- **Étapes du cycle de vie** :
    1. **Traduction** : Conversion de la JSP en servlet.
    2. **Compilation** : Conversion en bytecode.
    3. **Chargement** : Chargement en mémoire.
    4. **Instanciation** : Création de l’instance servlet.
    5. **Initialisation** : Appel de `jspInit()` pour initialiser la page.
    6. **Traitement des requêtes** : Appel de `_jspService()` pour chaque requête.
    7. **Destruction** : Appel de `jspDestroy()` pour libérer les ressources.

---

### 3. **Éléments de Syntaxe JSP**

- **Directives JSP** : Fournissent des informations de configuration au moteur JSP.
    - **Page** (`<%@ page ... %>`) : Spécifie des attributs comme `contentType`, `session`, etc.
    - **Include** (`<%@ include ... %>`) : Inclut une autre page dans la JSP.
    - **Taglib** (`<%@ taglib ... %>`) : Associe des bibliothèques de balises personnalisées.
- **Déclarations (`<%! ... %>`)** : Définissent des méthodes et des variables accessibles sur toute la page.
- **Scriptlets (`<% ... %>`)** : Permettent d'insérer du code Java.
- **Expressions (`<%= ... %>`)** : Affichent le résultat d'une expression Java dans le HTML.
- **Commentaires** :
    - **HTML (`<!-- ... -->`)** : Visible dans le code source HTML.
    - **JSP (`<%-- ... --%>`)** : Non transmis au client, réservé au moteur JSP.

---

### 4. **Actions JSP (`<jsp:... />`)**

- **Principales Actions JSP** :
    - **`<jsp:include>`** : Inclut des fichiers au moment de l'exécution.
    - **`<jsp:forward>`** : Transmet la requête à une autre ressource.
    - **`<jsp:useBean>`** : Instancie ou récupère un JavaBean pour le manipuler dans la JSP.
    - **`<jsp:setProperty>` / `<jsp:getProperty>`** : Modifient ou récupèrent les propriétés d'un JavaBean.

---

### 5. **JavaBeans et JSP**

- **JavaBean** : Classe Java avec un constructeur sans argument et des méthodes `get` et `set` pour les attributs.
- **Utilisation des JavaBeans** :
    - **`<jsp:useBean>`** : Instancie ou lie un bean à la page.
    - **`<jsp:setProperty>`** : Assigne une valeur à une propriété du bean.
    - **`<jsp:getProperty>`** : Récupère une valeur de propriété pour l'afficher.

---

### 6. **Variables Implicites**

- **Définition** : Objets prédéfinis disponibles automatiquement dans les JSP.
- **Principales Variables** :
    - **request** : Gère les données de la requête HTTP.
    - **response** : Représente la réponse HTTP.
    - **out** : Permet d’écrire du contenu HTML dans la réponse.
    - **session** : Stocke des informations utilisateur entre les requêtes.
    - **application** : Partage des données entre toutes les sessions de l’application.
    - **config** : Informations de configuration de la servlet.
    - **pageContext** : Accède aux fonctionnalités et variables implicites de la page.
    - **exception** : Accède aux erreurs survenues lors du traitement de la page.

---

### 7. **Langage d'Expression (EL)**

- **Définition** : Langage simplifié pour manipuler des données dans les JSP sans utiliser de code Java.
- **Syntaxe** : `${expression}`, permettant des opérations arithmétiques, logiques, et de comparaison.
- **Accès aux Beans et Collections** : Peut accéder aux propriétés des beans et manipuler des listes, sets et maps.

---

## Chapitre 4:

> Ce chapitre sur la JavaServer Pages Standard Tag Library (JSTL) présente un ensemble d'outils qui facilitent le développement d'applications web dynamiques en simplifiant le code JSP
> 

---

### 1. **Introduction à JSTL**

- **Définition** : JSTL (JavaServer Pages Standard Tag Library) est une bibliothèque de balises standard qui permet de simplifier le code JSP en évitant le mélange de Java et XHTML, améliorant la lisibilité.
- **Objectif** : Facilite la séparation entre logique métier et logique de présentation, en suivant le modèle MVC.
- **Utilisation** : Utilisée souvent avec le **Langage d’Expression (EL)** pour manipuler les données.

---

### 2. **Bibliothèques de JSTL et leur Utilisation**

- Chaque bibliothèque JSTL a son **URI** et est référencée par un **préfixe** dans les JSP.
    - **Core** : `c` - Opérations générales (boucles, conditions, etc.)
    - **Format** : `fmt` - Internationalisation, formats de date et de nombre.
    - **XML** : `x` - Manipulation de données XML.
    - **SQL** : `sql` - Exécution de requêtes SQL (déconseillé pour des raisons de sécurité).
    - **Fonctions** : `fn` - Fonctions de manipulation de chaînes.

---

### 3. **Bibliothèque Core JSTL**

- **Fonctionnalités** : Fournit des balises pour des opérations de base comme les boucles, conditions et manipulation de variables.
- **Principales Balises** :
    - `<c:out>` : Affiche du texte ou une valeur.
    - `<c:set>` : Définit une variable.
    - `<c:if>` : Conditionnelle (affiche si l'expression est vraie).
    - `<c:choose>`, `<c:when>`, `<c:otherwise>` : Structure conditionnelle similaire à `switch`.
    - `<c:forEach>` : Boucle sur une collection.
    - `<c:import>` : Importe une ressource (page).
    - `<c:redirect>` : Redirige vers une URL.

---

### 4. **Bibliothèque Format JSTL**

- **Utilité** : Internationalisation (i18n) des applications, formatage des dates, nombres et devises en fonction de la langue.
- **Principales Balises** :
    - `<fmt:setLocale>` : Définit la langue de l'utilisateur.
    - `<fmt:formatDate>` : Formate une date selon la région.
    - `<fmt:formatNumber>` : Formate un nombre, une devise ou un pourcentage.
    - `<fmt:setTimeZone>` : Définit la zone horaire.

---

### 5. **Bibliothèque SQL JSTL**

- **Fonction** : Permet d’exécuter des requêtes SQL dans les JSP (INSERT, UPDATE, DELETE), mais son usage est déconseillé pour des raisons de sécurité.
- **Principales Balises** :
    - `<sql:setDataSource>` : Définit la source de données (connexion JDBC).
    - `<sql:query>` : Exécute une requête SQL et stocke les résultats.
    - `<sql:update>` : Exécute des opérations de mise à jour (INSERT, UPDATE, DELETE).
    - **Exemple** : `<sql:query>` pour récupérer des enregistrements dans une base de données.

---

### 6. **Bibliothèque XML JSTL**

- **Fonction** : Manipule des données XML dans les JSP, pour extraire, transformer et afficher des informations XML.
- **Principales Balises** :
    - `<x:parse>` : Transforme une chaîne XML en structure de données.
    - `<x:forEach>` : Itère sur des éléments XML.
    - `<x:transform>` : Applique une feuille de style XSLT pour transformer XML.
    - `<x:if>` et `<x:choose>` : Effectuent des tests conditionnels sur les données XML.

---

### 7. **Bibliothèque Fonctions JSTL**

- **Fonction** : Traite les chaînes de caractères, utilisé avec EL pour manipuler du texte.
- **Principales Balises** :
    - `<fn:contains>`, `<fn:containsIgnoreCase>` : Vérifie si une chaîne contient une sous-chaîne.
    - `<fn:endsWith>`, `<fn:startsWith>` : Vérifie le début ou la fin d’une chaîne.
    - `<fn:indexOf>` : Trouve la première occurrence d'une sous-chaîne.
    - `<fn:join>`, `<fn:split>` : Joint ou découpe des chaînes.
    - `<fn:toLowerCase>`, `<fn:toUpperCase>` : Convertit la chaîne en minuscules ou majuscules.

---

## Chapitre 5:

> Ce chapitre sur **JPA (Java Persistence API)** joue un rôle essentiel en tant que fondation pour la **gestion de la persistance des données** dans les applications Java
> 

---

### 1. **Introduction à JPA**

- **Objectif** : JPA (Java Persistence API) est une API standard de Java pour gérer la persistance des données dans les applications Java. Elle permet de manipuler les données de manière orientée objet en facilitant les interactions avec les bases de données relationnelles.
- **Principes** : JPA utilise le **Mapping Objet-Relationnel (ORM)** pour représenter les données sous forme d'objets Java au lieu d'écrire directement des requêtes SQL.

---

### 2. **Mapping Objet-Relationnel (ORM)**

- **Concept** : L’ORM permet de mapper les objets Java aux tables de la base de données, rendant possible la manipulation des données via des entités Java.
- **Fonctionnement** : JPA fournit une API pour gérer les opérations de persistance, mise à jour et récupération de données.

---

### 3. **Entités JPA**

- **Définition** : Une entité JPA est une classe Java qui représente une table de la base de données. Chaque instance d’entité correspond à un enregistrement dans la table.
- **Cycle de Vie** :
    - **Nouvellement Créée (New)** : L'entité est créée en mémoire mais n'est pas encore persistée.
    - **Gérée (Managed)** : L'entité est associée à un contexte de persistance et suivie par l'EntityManager.
    - **Détachée (Detached)** : L'entité n'est plus suivie par l'EntityManager.
    - **Supprimée (Removed)** : L'entité est marquée pour suppression et sera supprimée de la base de données lors de la validation de la transaction.

---

### 4. **Unité de Persistance et `persistence.xml`**

- **Unité de Persistance** : Définit comment les entités sont liées à une source de données et est configurée dans le fichier `persistence.xml` situé dans le répertoire `META-INF`.
- **Configuration de `persistence.xml`** :
    - **persistence-unit** : Définit une unité de persistance avec un nom et un type de transaction (JTA ou RESOURCE_LOCAL).
    - **provider** : Spécifie le fournisseur JPA utilisé.
    - **jta-data-source** : Définit la source de données JTA.
    - **properties** : Spécifie des configurations comme la stratégie de création de tables et d'autres paramètres de persistance.

---

### 5. **EntityManager**

- **Rôle** : Classe principale de JPA, elle gère les entités en leur appliquant des opérations CRUD et des transactions.
- **Opérations CRUD** :
    - **Create** : `persist()` pour rendre une entité persistante.
    - **Read** : `find()` pour récupérer une entité ou `createQuery()` pour exécuter des requêtes JPQL.
    - **Update** : `merge()` pour synchroniser les changements.
    - **Delete** : `remove()` pour supprimer une entité.
- **Gestion des Transactions** : Commencées avec `begin()`, validées avec `commit()`, et annulées avec `rollback()` en cas d'échec.

---

### 6. **Annotations de JPA**

- **Principales Annotations** :
    - **@Entity** : Indique qu'une classe est une entité JPA.
    - **@Table** : Spécifie le nom de la table associée à l’entité.
    - **@Id** et **@GeneratedValue** : Définit la clé primaire et sa stratégie de génération.
    - **@Column** : Spécifie les propriétés de la colonne (nom, longueur, nullabilité, etc.).
    - **@Temporal** : Précise le type de date (DATE, TIME, TIMESTAMP).
    - **@Transient** : Champ non persistant.
    - **@Embeddable** et **@Embedded** : Utilisés pour intégrer des objets dans une entité principale.
    - **@ElementCollection** : Permet de gérer une collection d'éléments simples (comme des listes) sans créer une nouvelle entité.

---

### 7. **Requêtes JPA**

- **JPQL (Java Persistence Query Language)** : Langage de requêtes orienté objet pour manipuler les entités.
    - Exemples : `SELECT e FROM Employee e`, `SELECT COUNT(e) FROM Employee e WHERE e.department = :deptName`.
- **Requêtes Natives** : Permettent d'exécuter des requêtes SQL directes sur la base de données.
- **Requêtes Nommées** : Associées aux entités, elles sont définies via l'annotation `@NamedQuery` ou dans `persistence.xml` pour centraliser les requêtes et réutiliser le code.

---