## Chapitre 1

> Ce chapitre sert à introduire les concepts fondamentaux de Java EE (Enterprise Edition), une plateforme essentielle pour le développement d'applications d'entreprise. En expliquant les bases de l'architecture Java EE et de ses composants

---

### 1. **Objectifs de Java EE**

- Comprendre l'architecture de la plateforme Java EE.
- Utiliser Java EE pour développer des applications d'entreprise multi-tiers.
- Maîtriser les frameworks Java EE : `JSF` (pages dynamiques), `EJB` (couche métier) et `JPA` (couche de persistance).

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

- **Java** : Langage orienté objet et **semi-compilé** (**bytecode** interprété par la JVM).
- **JVM (Java Virtual Machine)** : Permet la portabilité, sécurité et performance.
- **JRE (Java Runtime Environment)** : Exécute les programmes Java.
- **JDK (Java Development Kit)** : Contient les outils pour compiler et exécuter le code Java.
- **Java SE (Java Standard Edition)** : Plateforme de base pour développer des applications Java, incluant les bibliothèques standard, le JDK et le JRE.Anciennement appelée J2SE (Java 2 Platform, Standard Edition).

    <img src="JEE Images/image-5.png" style="border-radius: 7px;" style="border-radius: 7px;" width="300">

---

### 4. **Rappel : Principes de l’Orienté Objet (OO)**

- **Objet** : Instance d'une classe représentant une entité.
- **Classe** : Modèle définissant les propriétés et comportements des objets.
- **Encapsulation** : Protéger les données via des méthodes d'accès.
- **Héritage** : Réutiliser les propriétés et comportements d'une classe par une autre.
- **Polymorphisme** : Adapter un comportement selon le contexte.

### 5. **Architecture Multi-Tiers**

- **Principe** : Diviser l'application en couches distinctes pour mieux organiser le code.
- **Couches Principales** :
  - **Web (Frontend)** : Interface utilisateur.
  - **Métier (Backend)** : Logique métier, traitement des données.
  - **DAO (Data Access Object)** : Gestion de l'accès aux données et interactions avec la base de données.

---

### 6. **Rappel : Architecture Multi-Tiers d'une Application Web**

- **SGBD (Système de Gestion de Base de Données)** : Stockage et organisation structurée des données.
- **Couche DAO** : Gestion des interactions avec le SGBD.
- **Couche Métier** : Règles métier, logique de traitement, opérations spécifiques.
- **Couche Web** : Présentation et interaction utilisateur (frontend).

<img src="JEE Images/image-6.png" style="border-radius: 7px;" width="200">

---

### 7. **Serveurs Web et Serveurs d'Applications**

- **Serveur Web** : Gère les **requêtes HTTP** et les **ressources statiques** (HTML, images, CSS).
  - Exemples : *Apache*, *Nginx*, *Microsoft IIS*.
- **Serveur d'Applications** : Environnement d'exécution complet pour la logique métier (transactions, sécurité, persistance).
  - Exemples : *WildFly*, *GlassFish*, *WebLogic*, *TomCat*.

---

### 8. **Java EE : Définition et Historique**

- **Java EE** : Plateforme pour développer des applications d'entreprise évolutives et distribuées.
- **Avantages** :
  - **Modularité** pour un code réutilisable et maintenable,
  - **Évolutivité** adaptée aux grandes applications,
  - **Gestion des transactions** pour garantir la cohérence,
  - **Interopérabilité** entre technologies via des standards ouverts,
  - **Persistance des données** grâce à des API comme JPA,
  - **Sécurité** avancée pour protéger les applications et les données,
  - **Services web** pour les architectures modernes.
- **Historique** :
  - **J2EE 1.2 (1999)** : Première version officielle avec Servlets, JSP, JDBC, et EJB.
  - **Transition vers Jakarta EE (2018)** : Passage de Java EE à la Fondation Eclipse, renommé Jakarta EE.
  - **Jakarta EE 9 (2020)** : Suppression des technologies obsolètes pour moderniser la plateforme.
  - **Jakarta EE 10 (2022)** : Introduction de mises à jour et d'améliorations pour répondre aux besoins actuels.

        <img src="JEE Images/image-7.png" style="border-radius: 7px;" width="400">

---

### 9. **Composants de Java EE**

- **Définition des composants** :
  - Unités réutilisables écrites en Java, compilées en bytecode, assemblées et déployées dans un serveur Java EE.
- **Types de composants** :
  - **Clients** :
    - **Clients Web** : Pages HTML, XML, JavaScript, etc.
    - **Applets** : Petites applications Java exécutées dans un navigateur.
    - **Applications clientes** : Logiciels installés sur la machine utilisateur avec interface graphique.
  - **Web** :
    - **Servlets** : Gestion des requêtes/réponses HTTP.
    - **JSP (JavaServer Pages)** : Création de pages web dynamiques en combinant Java et HTML.
    - **JSF (JavaServer Faces)** : Framework pour accélérer le développement d'applications Web.
  - **Métier** :
    - **Entités beans** : Gestion de la persistance des données.
    - **EJB (Enterprise JavaBeans)** : Encapsulation de la logique métier, gestion des transactions et de la sécurité.

<img src="JEE Images/image-8.png" style="border-radius: 7px;" width="600">

---

### 10. **Conteneurs Java EE**

- **Définition** :
  - Environnement d'exécution pour héberger et gérer les composants Java EE.
  - Fournit des services tels que la **sécurité**, la **gestion des transactions**, les **cycles de vie**, et l'**injection de dépendances**.
- **Types de conteneurs** :
  - **Conteneur de Servlets** :
    - Gère les servlets : leur exécution, cycle de vie, threads, et sessions utilisateur.
    - Traite les requêtes et réponses HTTP.
    - Offre des services de sécurité et d'authentification.
  - **Conteneur EJB (Enterprise JavaBeans)** :
    - Supporte les session beans (avec/sans état) et message-driven beans.
    - Gère le cycle de vie, les transactions, la sécurité et l'injection de dépendances.
  - **Conteneur Web** :
    - Gère les composants web comme les servlets et JSP.
    - Gère les sessions utilisateur, cookies, et les requêtes/réponses HTTP.
    - Assure la sécurité des applications web.
  - **Conteneur de Persistance** :
    - S'occupe des opérations de persistance des données via JPA (Java Persistence API).
    - Transforme les objets Java en entités persistantes pour les bases de données relationnelles.
  - **Conteneur de Message** :
    - Gère la communication asynchrone avec l'API JMS (Java Message Service).
    - Assure la livraison fiable des messages et gère les files d'attente/sujets.

---

### 11. **Structure et Déploiement d'une Application Java EE**

1.**Déploiement d’une application Java EE**

> Le déploiement dans un conteneur implique plusieurs étapes essentielles, organisées autour de fichiers et structures spécifiques. Voici une présentation synthétique :

- **Éléments nécessaires pour le déploiement**
  - **Application empaquetée :**
    - Tous les composants (classes compilées, ressources statiques, fichiers de configuration, etc.) regroupés dans une archive ou un module.
    - Chaque type de conteneur possède un format d’archive adapté :
      - `WAR` (Web Application Archive) pour les applications web.
      - `JAR` (Java Archive) pour les modules EJB.
      - `EAR` (Enterprise Archive) pour les applications d’entreprise combinant plusieurs modules.
  - **Fichier descripteur de déploiement** :
    - Contenu dans chaque module.
    - Fournit au conteneur des informations pour exécuter correctement l’application (déclarations de sécurité, configurations spécifiques).
    - Exemples :
      - `web.xml` (pour les applications web).
      - `ejb-jar.xml` (pour les modules EJB).
      - `application.xml` (pour l’application globale empaquetée dans un EAR).

- **Structure d’une application Java EE**
  - **Module Web (`.WAR`)** :
    - Répertoire racine public : Contient les pages HTML, JSP, images, etc.
    - `WEB-INF/` :
      - `web.xml` : Descripteur de déploiement.
      - `classes/` : Contient les classes compilées (servlets, helpers, etc.).
      - `lib/` : Contient les bibliothèques externes nécessaires (`JAR`).
    - **Empaquetage** : Le tout est regroupé dans un fichier `WAR`.
  - **Module EJB (`.JAR`)** :
    - `META-INF/` : Contient le fichier descripteur `ejb-jar.xml`.
    - Classes Java nécessaires :
      - Interfaces locales et distantes (home et remote).
      - Classe d’implémentation et classes auxiliaires (exemple : exceptions).
    - **Empaquetage** : Le tout est regroupé dans un fichier `JAR`.
  - **Fichier EAR (`.EAR`)** :
    - `META-INF/` :
      - Contient le fichier descripteur `application.xml`, qui déclare les modules constituant l’application.
    - **Modules inclus** :
      - Modules `WAR` pour les applications web.
      - Modules `JAR` pour les composants EJB.
    - **Empaquetage** : Le tout est regroupé dans un fichier `EAR`.

    <img src="JEE Images/image-9.png" style="border-radius: 7px;" width="400">

---

### 12. **Architecture MVC dans Java EE**

**Structure MVC** :

- **Modèle** :
  - Représente et gère les données de l'application.
  - Responsable de la gestion, de la récupération et de la mise à jour des données.
  - Interagit souvent avec la couche DAO (Data Access Object) pour accéder à la base de données.
- **Vue** :
  - Génère l'interface utilisateur.
  - Affiche les données sous forme compréhensible (ex. pages HTML dynamiques).
  - Implémentée avec des technologies comme JSP (Java Server Pages).
- **Contrôleur** :
  - Sert d'intermédiaire entre le Modèle et la Vue.
  - Gère les requêtes HTTP (via des Servlets).
  - Déclenche les traitements dans la couche métier et fournit les données à la Vue.

**Étapes du Flux MVC** :

- **Requête Client** :
  - Un client (navigateur web ou application mobile) envoie une requête HTTP vers le serveur.
  - Une Servlet agit comme le Contrôleur pour recevoir cette requête.
- **Traitement par la Couche Métier** :
  - La Servlet analyse la requête et invoque des services dans la couche métier (EJB).
  - Les EJB (Enterprise JavaBeans) encapsulent la logique métier et gèrent des services tels que les transactions.
- **Interaction avec la Couche DAO** :
  - La couche métier peut déléguer des opérations à la couche DAO pour interagir avec la base de données.
- **Stockage des Résultats** :
  - Les résultats retournés par la couche DAO/métier sont placés dans le Modèle.
- **Préparation de la Vue** :
  - La Servlet utilise les données du Modèle et les transmet à une page JSP.
  - Le forwarding vers JSP permet d'injecter les données dans la Vue.
- **Rendu de la Vue** :
  - JSP génère une page HTML dynamique contenant les résultats.
- **Réponse Client** :
  - La page HTML générée est renvoyée au client dans une réponse HTTP.

<img src="JEE Images/image-10.png" style="border-radius: 7px;" width="700">

---

### 13. **Avantages de Java EE**

- **Modularité et Réutilisabilité** : Code organisé et réutilisable.
- **Évolutivité et Performance** : Gère efficacement de nombreux utilisateurs.
- **Interopérabilité et Services Web** : Compatibilité avec d’autres systèmes via des API standardisées.
- **Gestion des Transactions et Persistance des Données** : Garantit l’intégrité des données.
- **Sécurité** : Contrôle des accès et protection des données.

---

## Chapitre 2

> Ce chapitre sert à introduire les servlets, un composant central de Java EE, et à expliquer leur rôle dans le développement d'applications web dynamiques côté serveur

---

### 1. **Introduction aux Servlets**

- **Définition** : Un servlet est un composant Java côté serveur, exécuté dans un conteneur de servlets (comme Tomcat), qui reçoit les requêtes HTTP, les traite et renvoie des réponses HTTP dynamiques.
- **Fonctionnalités** :
  - **Créer des applications dynamiques** : Génère des réponses HTML basées sur les requêtes des utilisateurs.
  - **Collecter des entrées** : Gère les soumissions de formulaires HTML.
  - **Accès aux bases de données** : Peut interagir avec des bases pour présenter ou mettre à jour des enregistrements.

---

### 2. **Avantages des Servlets**

- **Portabilité** : indépendante du système exploitation et des serveurs web.
- **Efficacité** : semi compilée, gestion du cache, connexions persistantes.
- **Puissance** :
  - Communication bidirectionnelle avec le serveur.
  - Partage de données et chaînage entre servlets.
- **Modularité** : possibilité d’avoir plusieurs servlets, chacune pouvant accomplir une tâche spécifique.
- **Gestion des sessions et des cookies** : gestion des cookies, suivi des sessions, manipulation simple du
protocole HTTP…

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

- **Servlet** : Interface de base de chaque servlet, qui définit les méthodes
  - `init()`
  - `service(req: ServletRequest,rep: ServletResponse)`
  - `getServletConfig()`
  - `getServletInfo()`
  - `destroy()`.
- **GenericServlet** : Classe abstraite, simplifie la création de servlets indépendants du protocole HTTP.
- **HttpServlet** : Spécialisée pour les requêtes HTTP, avec des méthodes pour chaque type de requête.
  - `doGet(req: HttpServletRequest,rep: HttpServletResponse)`
  - `doPost(req: HttpServletRequest,rep: HttpServletResponse)`
  - `doPut(req: HttpServletRequest,rep: HttpServletResponse)`
  - `doDelete(req: HttpServletRequest,rep: HttpServletResponse)`

---

### 5. **API de Servlet**

- **ServletRequest**
  - **Description** : Représente la requête envoyée par le client au serveur.
  - **Principales Méthodes** :
    - `getMethod()` : Récupère la méthode HTTP utilisée par le client (GET, POST, etc.).
    - `getHeader(String key)` : Récupère la valeur d'un en-tête HTTP donné.
    - `getRemoteHost()` : Retourne le nom de domaine du client.
    - `getRemoteAddr()` : Fournit l'adresse IP du client.
    - `getParameter(String key)` : Récupère la valeur d'un paramètre envoyé dans l'URL ou un formulaire.
    - `getParameterValues(String key)` : Récupère toutes les valeurs d'un paramètre (cas de sélections multiples).
    - `getParameterNames()` : Retourne la liste des noms des paramètres passés à la requête.
    - `getServerName()` : Retourne le nom du serveur.
    - `getServerPort()` : Retourne le port utilisé par le serveur.
- **HttpServletRequest**
  - **Description** : Étend ServletRequest avec des fonctionnalités spécifiques au protocole HTTP.
  - **Principales Méthodes** :
    - `getSession()` : Gère les sessions utilisateur.
    - `getCookies()` : Récupère les cookies associés à la requête.
    - `getHeader(String name)` : Récupère la valeur d'un en-tête HTTP spécifique.
- **ServletResponse**
  - **Description** : Représente la réponse envoyée par la servlet au client.
  - **Principales Méthodes** :
    - `setStatus(int statusCode)` : Définit le code de statut HTTP (e.g., 200, 404).
    - `setHeader(String name, String value)` : Ajoute un en-tête HTTP personnalisé.
    - `setContentType(String type)` : Définit le type MIME de la réponse (e.g., text/html).
    - `setContentLength(int len)` : Définit la longueur du contenu de la réponse.
    - `getWriter()` : Retourne un objet PrintWriter pour envoyer des données texte au client.
    - `sendError(int statusCode, String msg)` : Envoie une réponse d'erreur HTTP avec un code et un message.
    - `sendRedirect(String location)` : Redirige le client vers une nouvelle URL.
    - `addCookie(Cookie cookie)` : Ajoute un cookie à la réponse HTTP.
- **HttpServletResponse**
  - **Description** : Étend ServletResponse pour inclure des fonctionnalités spécifiques au protocole HTTP.
  - **Principales Méthodes** :
    - `sendRedirect(String location)` : Redirige le client vers une nouvelle URL.
    - `setStatus(int sc)` : Définit le statut de la réponse HTTP.
    - `addCookie(Cookie cookie)` : Ajoute un cookie à la réponse.
- **ServletContext**
  - **Représentation** : Représente le contexte global de l'application web.
  - **Utilisation** : Permet aux servlets de partager des informations et de communiquer avec le serveur.
  - **Caractéristiques** :
    - Un seul contexte par application web dans une JVM.
    - Permet de partager des données entre servlets.
  - **Méthodes principales** :
    - `getInitParameter(String name)`: Récupère un paramètre d'initialisation global.
    - `getInitParameterNames()`: Récupère tous les noms des paramètres d'initialisation.
    - `setAttribute(String name, Object value)`: Stocke un attribut d'application.
    - `getAttribute(String name)`: Récupère un attribut d'application.
    - `log(String message)`: Enregistre des messages dans le journal.
    - `getResource(String path)`: Récupère une ressource sous forme d'URL.

    Exemple d'utilisation de ServletContext

    ```java
    @WebServlet("/contextDemo")
    public class ContextDemoServlet extends HttpServlet {
        @Override
        public void init() throws ServletException {
            ServletContext context = getServletContext();
            context.setAttribute("globalMessage", "Message disponible pour toutes les servlets.");
        }

        @Override
        protected void doGet(HttpServletRequest request, HttpServletResponse response) 
                throws ServletException, IOException {
            ServletContext context = getServletContext();
            String message = (String) context.getAttribute("globalMessage");
            response.getWriter().println("Message de ServletContext : " + message);
        }
    }
    ```

- **ServletConfig**
  - **Représentation** : Fournit un accès à la configuration spécifique d'une servlet.
  - **Utilisation** : Facilite la personnalisation et la configuration des servlets individuellement.
  - **Méthodes principales** :
    - `getServletName()`: Renvoie le nom de la servlet.
    - `getServletContext()`: Récupère l'objet ServletContext.
    - `getInitParameter(String name)`: Récupère un paramètre d'initialisation spécifique à la servlet.
    - `getInitParameterNames()`: Récupère tous les paramètres d'initialisation.
    Exemple d'utilisation de ServletConfig

    Fichier `web.xml` :

    ```xml
    <servlet>
        <servlet-name>configDemoServlet</servlet-name>
        <servlet-class>com.example.ConfigDemoServlet</servlet-class>
        <init-param>
            <param-name>message</param-name>
            <param-value>Hello from ServletConfig!</param-value>
        </init-param>
    </servlet>
    <servlet-mapping>
        <servlet-name>configDemoServlet</servlet-name>
        <url-pattern>/configDemo</url-pattern>
    </servlet-mapping>
    ```

    Fichier Java :

    ```java
    @WebServlet("/configDemo")
    public class ConfigDemoServlet extends HttpServlet {
        @Override
        protected void doGet(HttpServletRequest request, HttpServletResponse response) 
                throws ServletException, IOException {
            ServletConfig config = getServletConfig();
            String message = config.getInitParameter("message");
            response.getWriter().println("Message de ServletConfig : " + message);
        }
    }
    ```

- **HttpSession**
  - **Représentation** : Utilisée pour gérer les sessions utilisateur dans une application web.
  - **Utilisation** : Permet de stocker et de récupérer des objets pendant une session utilisateur spécifique.
  - **Méthodes principales** :
    - `getId()`: Renvoie l'identifiant unique de session.
    - `invalidate()`: Détruit la session utilisateur.
    - `setAttribute(String name, Object value)`: Stocke un objet dans la session.
    - `getAttribute(String name)`: Récupère un objet stocké dans la session.
    - `removeAttribute(String name)`: Supprime un attribut spécifique de la session.

---

### 7. **Cycle de Vie d'une Servlet**

- **Étapes** :
  - **Charger la classe Servlet**.
    - Se produit lors du déploiement de l'application ou lors de la première requête.
    - Informations extraites du fichier `web.xml`
  - **Créer une instance de Servlet**.
    - Une seule instance est créée, les requêtes concurrentes sont gérées via des threads.
  - **Appeler la méthode `init()`**.
    - Appelée une seule fois lors de l'initialisation.
    - Configure les paramètres d'initialisation définis dans `web.xml`.
    - Syntaxe : `public void init(ServletConfig config) throws ServletException{...}`
  - **Appeler la méthode `service()` pour traiter chaque requête**.
    - Traite chaque requête HTTP.
    - Détermine le type de requête (GET, POST, etc.) et appelle les méthodes correspondantes (doGet, doPost...).
    - Crée des objets `HttpServletRequest` et `HttpServletResponse`.
    - Syntaxe : `public void service(ServletRequest req, ServletResponse res) throws ServletException, IOException{...}`
  - **Appeler la méthode `destroy()` avant la suppression de la servlet**.
    - Appelée une seule fois avant la suppression de l'objet servlet.
    - Permet de libérer les ressources (fermer les connexions à la base de données, arrêter les threads, etc.).
    - Syntaxe : `public void destroy(){...}`.

    <img src="JEE Images/image-11.png" style="border-radius: 7px;" width="400">

---

### 8. **Développement d’une Servlet**

- **Étapes** :
    1. Créer une classe qui hérite de `HttpServlet`.
    2. Redéfinir `doGet()` ou `doPost()` pour répondre aux requêtes.
    3. Configurer la servlet dans `web.xml` ou utiliser l’annotation `@WebServlet`.
- **Exemple de Code Servlet** :
  - **Avec `web.xml`** :

    ```java
    public class HelloServlet extends HttpServlet {
        protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
            response.setContentType("text/html");
            PrintWriter out = response.getWriter();
            out.println("<h1>Hello, World!</h1>");
        }
    }
    ```

    ```xml
    <servlet>
        <servlet-name>HelloServlet</servlet-name>
        <servlet-class>com.example.HelloServlet</servlet-class>
    </servlet>
    <servlet-mapping>
        <servlet-name>HelloServlet</servlet-name>
        <url-pattern>/hello</url-pattern>
    </servlet-mapping>
    ```

  - **Avec Annotation** :

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

- **Exemple de Servlet avec Paramètres** :

    ```java
    @WebServlet("/hello")
    public class HelloServlet extends HttpServlet {
        protected void doGet(HttpServletRequest request, HttpServletResponse response) throws IOException {
            String name = request.getParameter("name");
            response.setContentType("text/html");
            PrintWriter out = response.getWriter();
            out.println("<h1>Hello, " + name + "!</h1>");
        }
    }
    ```

    ```html
    <form action="/hello" method="GET">
        <input type="text" name="name" />
        <button type="submit">Submit</button>
    </form>
    ```

---

### 9. **Type MIME**

- **Définition** : Standard qui informe le navigateur sur le type de contenu, permettant de traiter correctement les données.
- **Exemples courants** :
  - `text/html` pour le HTML.
  - `application/json` pour des données JSON.

---

## Chapitre 3

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

    <img src="JEE Images/image-12.png" style="border-radius: 7px;" width="400">

---

### 3. **Éléments de Syntaxe JSP**

- **Directives JSP** : Fournissent des informations de configuration au moteur JSP.
  - **Syntaxe** : `<%@ ... %>`, `<jsp:directive.nom_directive … />` (Syntaxe XML).
  - **Page** (`<%@ page ... %>`) : Cette directive sert à configurer des attributs spécifiques de la page JSP.
    - **Principaux attributs** :
      - `import` : Permet d'importer des classes et des packages Java nécessaires à la page.
        - `<%@ page import="java.util.*, java.sql.Connection" %>`
      - `contentType` : Définit le type MIME et l'encodage des caractères de la réponse.
        - `<%@ page contentType="text/html;charset=UTF-8" %>`
      - `session` : Détermine si la page JSP fait partie d’une session HTTP (valeur par défaut : true).
        - `<%@ page session="false" %>`
      - `errorPage` : Spécifie la page JSP à afficher en cas d’exception.
        - `<%@ page errorPage="error.jsp" %>`
      - `isErrorPage` : Indique si la page gère les exceptions comme une page d'erreur (valeur par défaut : false).
        - `<%@ page isErrorPage="true" %>`
      - `language` : Définit le langage de programmation utilisé dans la page JSP (valeur par défaut : Java).
        - `<%@ page language="java" %>`
      - `extends` : Indique la classe parent de la servlet générée par la JSP.
        - `<%@ page extends="com.example.MyServlet" %>`
  - **Include** (`<%@ include ... %>`) : Inclut une autre page dans la JSP.
    - **Exemple** : `<%@ include file="header.jsp" %>`
  - **Taglib** (`<%@ taglib ... %>`) : Associe des bibliothèques de balises personnalisées.
    - **Exemple** : `<%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c" %>`
- **Déclarations (`<%! ... %>`)** : Définissent des méthodes et des variables accessibles sur toute la page.
  - **Exemple** : `<%! int count = 0; %>`
- **Scriptlets (`<% ... %>`)** : Permettent d'insérer du code Java.
  - **Exemple** : `<% for (int i = 0; i < 5; i++) {...} %>`
- **Expressions (`<%= ... %>`)** : Affichent le résultat d'une expression Java dans le HTML.
  - **Exemple** : `<%= "Hello, World!" %>`
- **Commentaires** :
  - **HTML (`<!-- ... -->`)** : Visible dans le code source HTML.
  - **JSP (`<%-- ... --%>`)** : Non transmis au client, réservé au moteur JSP.
- **Actions JSP** : Balises spéciales pour effectuer des actions spécifiques.
  - **Syntaxe** : `<jsp:action.nom_action ... />`.
  - **Principales Actions** :
    - **`<jsp:include>`** : Inclut une autre ressource (page, fichier, servlet).
      - **Exemple** : `<jsp:include page="header.jsp" />`
    - **`<jsp:forward>`** : Redirige la requête vers une autre ressource.
      - **Exemple** : `<jsp:forward page="error.jsp" />`
    - **`<jsp:param>`** : Définit des paramètres pour les actions `include` et `forward`.
      - **Exemple** : `<jsp:param name="id" value="123" />`

---

### 5. **JavaBeans et JSP**

permettent d'implémenter la logique métier et de séparer le traitement de la présentation.

1. **Caractéristiques des JavaBeans** :
    - Classe Java respectant certaines conventions :
        - Doit posséder un constructeur vide.
        - Utilise des getters (`getXxx`) et setters (`setXxx`) pour manipuler les attributs.
    - Utilisation pour gérer la logique métier de l'application web.
2. **Actions JSP pour les JavaBeans** :
    - `<jsp:useBean>` : Crée ou récupère une instance de JavaBean.
        - **Attributs** :
            - `id` (obligatoire) : Nom de la variable référencée.
            - `class` (obligatoire) : Classe Java du Bean.
            - `scope` : Portée de l'objet (page, request, session, application).
            - `type` : Spécifie un type pour le Bean.
            - `beanName` : Nom symbolique de l'objet Bean.
        - **Exemple** : `<jsp:useBean id="employe1" scope="session" class="ensa.Employe" type="Personne" />`
    - `<jsp:setProperty>` : Attribue une valeur à une propriété du JavaBean.
        - **Attributs** :
            - `name` : Identifiant du Bean.
            - `property` : Nom de la propriété à modifier.
            - `value` : Nouvelle valeur à assigner.
        - **Exemple** : `<jsp:setProperty name="employe1" property="nom" value="Anas" />`
    - `<jsp:getProperty>` : Récupère et affiche la valeur d'une propriété du JavaBean.
        - **Attributs** :
            - `name` : Identifiant du Bean.
            - `property` : Propriété dont la valeur doit être récupérée.
        - **Exemple** : `<jsp:getProperty name="employe1" property="nom" />`
3. **Portée (scope) des Beans** :
    - **page** : Accessible uniquement dans la page JSP en cours (valeur par défaut).
    - **request** : Disponible durant toute la requête HTTP.
    - **session** : Partagé entre toutes les JSP d'une même session utilisateur.
    - **application** : Accessible à toutes les JSP de l'application, même après le rechargement.

---

### 6. **Variables Implicites**
>
> Les variables implicites (ou objets implicites) sont des objets prédéfinis, automatiquement créés et disponibles dans les pages JSP sans importation ou déclaration explicite. Ces objets sont fournis par le conteneur JSP pour faciliter le développement des applications web.

- **Liste des Objets Implicites** :
  - `request` : Représente la requête HTTP courante. Utilisé pour accéder aux paramètres, en-têtes, cookies, etc.
    - **Exemple** : `<%= request.getParameter("parametre") %>`
  - `response` : Représente la réponse HTTP générée par la page JSP. Permet de modifier la réponse envoyée au client.
    - **Exemple** : `<%= response.encodeURL("page.jsp") %>`
  - `out` : Instance de javax.servlet.jsp.JspWriter utilisée pour écrire du contenu HTML dans la réponse.
    - **Exemple** : `<% out.println("Hello, World!"); %>`
  - `session` : Représente la session utilisateur courante. Utilisé pour stocker des données qui persistent durant la session.
    - **Exemple** : `<%= session.getAttribute("utilisateur") %>`
  - `application` : Représente le contexte de l'application. Utilisé pour partager des données entre les sessions et les requêtes.
    - **Exemple** : `<%= application.getAttribute("compteur") %>`
  - `config` : Fournit des informations sur la configuration de la servlet associée à la page JSP.
    - **Exemple** : `<%= config.getServletName() %>`
  - `pageContext` : Encapsule toutes les variables implicites et offre des méthodes pour inclure du contenu ou gérer les erreurs.
    - **Exemple** : `<%= pageContext.getErrorData() %>`
  - `exception` : Défini automatiquement en cas d'erreur. Contient des informations sur l'exception survenue.
    - **Exemple** : `<%= exception.getMessage() %>`
  - `page` : Représente la page JSP elle-même. Utile pour appeler des méthodes définies dans la page JSP.
    - **Exemple** : `<jsp:useBean id="myBean" class="com.example.MyBean" />`

---

### 7. **Langage d'Expression (EL)**

- **Définition** : Langage simplifié pour manipuler des données dans les JSP sans utiliser de code Java.
- **Syntaxe** : `${expression}`, permettant des opérations arithmétiques, logiques, et de comparaison.
- **Accès aux Beans et Collections** : Peut accéder aux propriétés des beans et manipuler des listes, sets et maps.

---

## Chapitre 4

> Ce chapitre sur la JavaServer Pages Standard Tag Library (JSTL) présente un ensemble d'outils qui facilitent le développement d'applications web dynamiques en simplifiant le code JSP

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

## Chapitre 5

> Ce chapitre sur **JPA (Java Persistence API)** joue un rôle essentiel en tant que fondation pour la **gestion de la persistance des données** dans les applications Java

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

## Chapitre 05 suite

### 1. **Les Relations avec JPA**

- **Définition** : Les relations entre entités sont utilisées pour définir comment les objets sont liés entre eux dans une base de données relationnelle, facilitant la navigation entre les entités.
- **Types de Relations** :
  - **Unidirectionnelle** : Une entité connaît l’autre sans réciprocité. Exemple : Une entité `A` connaît l’entité `B`, mais `B` ne connaît pas `A`.
  - **Bidirectionnelle** : Les deux entités se connaissent mutuellement et peuvent naviguer dans les deux sens.

- **Annotations** :
  - **@OneToOne** : Relation où une instance de l'entité A correspond à une seule instance de l'entité B.
  - **@OneToMany** : Une entité est associée à plusieurs instances d’une autre entité.
  - **@ManyToOne** : Plusieurs entités sont associées à une seule entité.
  - **@ManyToMany** : Plusieurs instances de chaque entité peuvent être associées à plusieurs instances d’une autre entité.

### 2. **Relations Unidirectionnelles**

- **Relation 1:1 Unidirectionnelle** :
  - Utilisation de **@OneToOne** pour spécifier que chaque instance d'une entité A est liée à une seule instance d'une entité B.
  - **@JoinColumn** est utilisée pour spécifier la colonne de clé étrangère dans la table source.
  - Exemple : Une entité `Individu` est liée à une entité `Abonnement`.

- **Relation 1:n Unidirectionnelle** :
  - Utilisation de **@OneToMany** pour définir qu'une instance d'une entité est associée à plusieurs instances d’une autre entité.
  - Une collection (comme `List`, `Set`) est utilisée pour stocker les références.
  - Par défaut, une table de jointure est créée. Pour éviter cela, on utilise **@JoinColumn** pour ajouter une clé étrangère dans la table cible.

- **Relation n:1 Unidirectionnelle** :
  - Utilisation de **@ManyToOne** pour lier plusieurs instances d’une entité à une seule instance d’une autre entité.
  - Exemple : Plusieurs `Employés` peuvent être liés à un seul `Département`.

### 3. **Relations Bidirectionnelles**

- **Concept** : Les deux entités connaissent l’existence l’une de l’autre, permettant une navigation bidirectionnelle.
- **`mappedBy`** : Utilisé pour indiquer le côté inverse d'une relation bidirectionnelle. Le côté avec `mappedBy` ne contrôle pas la relation.
- **Relation 1:1 Bidirectionnelle** :
  - Le côté propriétaire contrôle la clé étrangère. **@JoinColumn** est utilisé pour spécifier la colonne.
  - **`mappedBy`** sur le côté inverse indique quelle propriété contrôle la relation.
- **Relations @OneToMany et @ManyToOne** :
  - Le côté **@ManyToOne** contrôle la clé étrangère, et **@OneToMany** utilise `mappedBy` pour référencer cette relation.
- **Relation n:n Bidirectionnelle** :
  - Utilisation de **@ManyToMany** dans les deux entités.
  - **@JoinTable** est utilisé pour définir la table d'association entre les deux entités.

### 4. **Opérations en Cascade**

- **Cascade** : Les opérations effectuées sur une entité sont propagées à ses entités associées.
- **Types de Cascade** :
  - **CascadeType.PERSIST** : Persistance automatique des entités associées.
  - **CascadeType.MERGE** : Mise à jour des entités associées lors de la fusion.
  - **CascadeType.REMOVE** : Suppression automatique des entités associées.
  - **CascadeType.REFRESH** : Rafraîchissement des entités associées.
  - **CascadeType.DETACH** : Détachement des entités associées du contexte de persistance.
  - **CascadeType.ALL** : Applique toutes les opérations ci-dessus.

### 5. **Fetch Lazy et Fetch Eager**

- **Lazy (chargement différé)** : Les données sont chargées uniquement lorsque cela est nécessaire.
- **Eager (chargement immédiat)** : Toutes les données associées sont chargées immédiatement avec l'entité principale.
- **Impact** :
  - **Lazy** : Réduit l'utilisation de la mémoire mais peut entraîner plusieurs requêtes à la base de données.
  - **Eager** : Charge plus de données initialement, ce qui peut augmenter l'utilisation de la mémoire mais réduit le nombre de requêtes.

### 6. **Héritage avec JPA**

- **@Inheritance** : Déclare une hiérarchie d'héritage entre entités.
- **Stratégies d'Héritage** :
  - **SINGLE_TABLE** : Utilise une seule table pour stocker toutes les entités de la hiérarchie, avec une colonne discriminante pour identifier chaque type.
  - **JOINED** : Chaque classe de la hiérarchie a sa propre table, reliée par des clés étrangères.
  - **TABLE_PER_CLASS** : Chaque classe de la hiérarchie a sa propre table avec toutes les colonnes nécessaires.
- **@DiscriminatorColumn** : Utilisé dans **SINGLE_TABLE** et **JOINED** pour identifier le type d'entité stocké dans une ligne de la table.

### 7. **Annotations de Tri et Surcharge**

- **@OrderBy** : Trie les collections d'entités lors de leur récupération.
- **@AttributeOverride** : Permet de redéfinir le mappage d'un attribut hérité dans une sous-classe.

### Chapitre 06

### 1. Introduction aux EJB

- **EJB (Enterprise JavaBeans)** : Composants côté serveur encapsulant la logique métier.
- **Fonctionnalités** :
  - Persistance des données.
  - Gestion des transactions.
  - Sécurité.
  - Communication dans des applications distribuées.

### 2. Le Conteneur EJB

- Fournit un environnement d'exécution pour les EJB.
- Gère :
  - Cycle de vie des EJB.
  - Transactions.
  - Sécurité.
  - Accès aux bases de données.
  - Synchronisation des accès.

### 3. Architecture des EJB

- **Interfaces d'accès** :
  - **Distant** : Pour les clients dans différents conteneurs ou machines.
  - **Local** : Pour les clients dans le même conteneur EJB.

### 4. Types d’EJB

- **EJB Session** : Fournissent des services aux clients.
  - **Stateless** : Sans état entre les appels.
  - **Stateful** : Conservent l'état entre les appels.
  - **Singleton** : Une seule instance partagée entre tous les clients.
- **EJB Entity** : Représentent des objets persistants dans une base de données (remplacés par JPA).
- **Message-Driven** : Gèrent les communications asynchrones (JMS).

### 5. EJB Session

#### Bean sans État : Stateless

- **Fonctionnement** :
  - Ne stockent pas d'informations spécifiques au client.
  - Gérés via un pool d'instances.
- **Cycle de Vie** :
  1. Création de l'instance.
  2. Injection des dépendances.
  3. Méthode `@PostConstruct` (optionnelle).
  4. Prêt à être utilisé.
  5. Traitement des requêtes.
  6. Méthode `@PreDestroy` (optionnelle) avant la destruction.

#### Bean avec État : Stateful

- Conserve un état associé à un client entre les appels.
- **Cycle de Vie** :
  1. Création de l'instance.
  2. Injection des dépendances.
  3. Méthode `@PostConstruct`.
  4. Traitement des requêtes.
  5. Passivation et activation gérées via `@PrePassivate` et `@PostActivate`.
  6. Méthode `@Remove` pour indiquer la fin de l'utilisation.

#### Singleton

- Une seule instance partagée.
- Utilisé pour gérer des ressources partagées ou des caches.

### 6. EJB Entity

- Représentation d'objets persistants (remplacés par JPA).

### 7. Injection de Dépendances

- **Annotations** :
  - `@EJB` : Injection d'autres EJB.
  - `@Resource` : Injection de ressources.

### 8. Déploiement des EJB

- Packagés en fichiers `.jar` ou `.ear`.
- Contiennent des fichiers de configuration pour le conteneur.

### 9. JNDI (Java Naming and Directory Interface)

- Permet de localiser et d'accéder aux objets tels que les EJB, bases de données, et files d'attente.
- Utilisé pour la gestion des références d'EJB dans un annuaire.

## Chapitre 7

### 1. Introduction à JSF

- **JSF (JavaServer Faces)** : Framework standard pour la création d'interfaces utilisateur côté serveur dans les applications Web Java EE.
- **Objectifs** :
  - Simplifier la création d'interfaces utilisateur basées sur des composants.
  - Respecter le modèle MVC (Modèle-Vue-Contrôleur).
  - Fonctionne avec des pages XHTML.

### 2. Architecture JSF

- **Modèle MVC** :
  - **Contrôleur (Controller)** : Représenté par `FacesServlet`, gère le cycle de vie des requêtes JSF.
  - **Vue (View)** : Pages XHTML contenant des composants JSF.
  - **Modèle (Model)** : Représenté par les Managed Beans.

### 3. Fichiers de Configuration

- **web.xml** : Descripteur de toute application Web JEE.
- **faces-config.xml** : Configuration spécifique à JSF.

### 4. Composants d'une Application JSF

- Contient :
  - Pages web.
  - Tags (balises).
  - Managed Beans.
  - Fichiers de configuration (`web.xml` et `faces-config.xml`).
  - Autres objets (validateurs, convertisseurs, écouteurs).

### 5. FacesContext

- **FacesContext** : Classe représentant le contexte d'exécution de la requête JSF actuelle.
- Gère :
  - Le cycle de vie de la requête.
  - Les composants de l'interface utilisateur.
  - Les messages d'erreur.

### 6. Managed Beans

- **Définition** : Classes Java avec attributs, getters et setters.
- **Fonctionnalités** :
  - Validation des données des composants.
  - Gestion des événements.
  - Navigation entre les pages.
- **Portées** :
  - **@RequestScoped** : Persiste pour une seule requête.
  - **@SessionScoped** : Persiste pour la durée de la session utilisateur.
  - **@ApplicationScoped** : Partagé entre toutes les sessions utilisateurs.
  - **@ViewScoped** : Persiste pendant l'interaction avec une seule page.

### 7. Navigation entre les Pages

- **Types** :
  - **Statique** : Définie lors de l’écriture de l’application.
  - **Dynamique** : Déterminée au moment de l'exécution.
- **Mécanismes** :
  - **Navigation Implicite** : Résolution automatique des pages.
  - **Navigation Conditionnelle** : Basée sur l'état de l'application.

### 8. Tags JSF

- **HTML Tags (`h:`)** : Balises standard pour les composants HTML.
- **Core Tags (`f:`)** : Gestion du cycle de vie, validation, conversion.
- **Facelets Tags (`ui:`)** : Définir des templates et des compositions de pages.

### 9. Validation des Données

- **Méthodes** :
  - Validation intégrée avec balises (`required`, `validator`).
  - Balises `<f:validateXXX>` pour les règles de validation.
  - API Validator de JSF.
  - Annotations de validation dans les Beans.

### 10. Convertisseurs

- **Fonction** : Convertir des données entre le format de la page et celui des objets Java.
- **Types** :
  - **Standard** : `<f:convertNumber>`, `<f:convertDateTime>`.
  - **Personnalisés** : Implémentation de l'interface `Converter`.

### 11. Cycle de Vie d'une Requête JSF

- **Phases** :
  1. **Restore View** : Restauration de la vue.
  2. **Apply Request Values** : Association des valeurs soumises.
  3. **Process Validations** : Validation des données.
  4. **Update Model Values** : Mise à jour du modèle.
  5. **Invoke Application** : Exécution des actions.
  6. **Render Response** : Rendu de la réponse.
