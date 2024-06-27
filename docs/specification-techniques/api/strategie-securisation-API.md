### Introduction:

Dans le cadre de la réalisation de notre application, nous avons choisi de centraliser tous les enregistrements grâce à une API (Interface de Programmation d'Application). Cette API sera responsable du traitement de données personnelles sensibles de nos utilisateurs.

La nature sensible de ces informations soulève des questions cruciales de sécurité, notamment en ce qui concerne la protection contre l'accès et l'utilisation non autorisée. En appliquant les recommandations de l'Agence nationale de la sécurité des systèmes d'information (ANSSI) et en suivant le concept des trois piliers de la sécurité de l'information – la confidentialité, l'intégrité et la disponibilité – nous pouvons réduire considérablement les risques d'accès malveillant à ces données.

En mettant en œuvre ces mesures de sécurité rigoureuses, nous assurons à nos utilisateurs que leurs informations personnelles sont protégées contre les menaces potentielles, renforçant ainsi la confiance et la fiabilité de notre application.

### Liste de recommandations que nous souhaitons adopter à la couche logique

R8: Vérifier la conformités des données issues de sources externes

R11: Contrôler l’intégrité des contenus internes

R23: Ne pas stocker des informations sensibles dans les bases de données locales R28: Définir le path d’un cookie

R29 : Maîtriser l’accès aux cookies en JavaScript

R30 : Proscrire l’accès en JavaScript à un cookie de session

R34: Encoder les réponses XMLHttpRequest

R35: Choisir une API selon sa méthode HTTP

R36: Utiliser XHR avec la méthode POST

R37: Compléter la mise en œuvre de XHR par une configuration CSP

R38: Protéger les appels XHR par un contrôle anti-CSRF

R39: Mettre en œuvre un preflight lors des appels CORS

R40: Vérifier la valeur de l’Origin lors de la réception d’un requête CORS

R41: Cloisonner les services web au moyens de noms de domaines distincts

R42: Éviter l’utilisation de bibliothèques publiques effectuant des appels CORS

R43: Anonymiser le chargement des ressources en cross-origin

### Authentification et gestion de sessions

Afin de sécuriser l'accès aux ressources, nous utiliserons le protocole OAuth 2.0 avec des jetons d’accès JWT (JSON Web Token).
OAuth 2.0 agit comme un passeport temporaire, permettant d’accéder aux données des utilisateurs sans partager leur mots de passe. Il génère des jetons d’accès sécurisés JWT, qui contiennent des informations sur l’utilisateur et ses permissions.
Ils limitent ainsi la durée de vie des sessions, préviennent toute utilisation non autorisée des informations de l'utilisateur et permettent la détection de comportements suspects ou de compromissions. Offrant une solution robuste pour sécuriser les données et les accès dans l’application.

### Sécurisation des données en transit

● **Chiffrement des communications**
Pour garantir la sécurité et la confidentialité des communications entre les clients et notre API backend, nous utilisons plusieurs mesures de sécurité, similaires à celles déjà mises en place pour la couche frontend. Cela inclut l'utilisation de HTTPS, TLS et HSTS pour chiffrer les données, assurer leur intégrité et garantir l'authenticité des communications. Ces mesures sont cruciales pour protéger les données sensibles contre les accès non autorisés.

● **Transmission sécurisé des mots de passe**

La transmission sécurisée des mots de passe protège les identifiants des utilisateurs en empêchant leur interception par des attaquants. En chiffrant le mot de passe dès sa saisie et en utilisant une connexion HTTPS sécurisée pour l'envoyer du
client (comme un navigateur) vers le serveur de l'application, nous nous assurons que le mot de passe ne peut pas être lu en cours de route. Cela nous permettra de renforcer la sécurité en garantissant que les mots de passe ne sont jamais exposés en clair, réduisant ainsi le risque de vol et d'utilisation non autorisée.

● **Journalisation et Sécurisation des Requêtes API**

Pour garantir la sécurité de notre application et la confidentialité des données de nos utilisateurs, nous avons mis en place des mesures robustes pour journaliser et sécuriser les requêtes API. Cela inclut la surveillance et l'enregistrement de toutes les interactions avec l'API, ce qui permet de détecter et de répondre rapidement à toute activité suspecte. De plus, des techniques de sécurisation telles que l'authentification, l'autorisation et l'utilisation de connexions sécurisées (HTTPS) sont employées pour protéger contre les accès non autorisés et les attaques potentielles.
Simultanément, notre application assure l'intégrité et la sécurité des données en effectuant une validation et une sanitization rigoureuses des données entrantes. La validation consiste à vérifier que les données fournies par les utilisateurs sont correctes et conformes aux attentes (comme le bon format d'une adresse email).

● **Limitation et Surveillance des Requêtes**

Pour protéger notre application contre les abus et garantir une performance optimale, nous avons mis en place des mécanismes de limitation et de surveillance des requêtes. La limitation des requêtes (rate limiting) contrôle le nombre de requêtes qu'un utilisateur peut effectuer dans un certain laps de temps, empêchant ainsi les surcharges du système et les attaques. Cela nous permettra de détecter et de répondre rapidement à tout comportement anormal ou suspect, assurant ainsi la sécurité et la fiabilité de notre application.

### Gestion des Utilisateurs et des Permissions

Pour renforcer la sécurité et la confidentialité des données de nos utilisateurs, notre application adopte une stratégie d'identification basée sur des identifiants uniques, appelés UUID (Unique User ID), et plus spécifiquement sur la version 4 (UUIDv4). Les UUIDv4 génèrent des identifiants de manière totalement aléatoire. Cela rend très difficile pour un attaquant de deviner ces numéros et de voler des informations. Ainsi, l'utilisation des UUIDv4 constitue une barrière robuste contre les tentatives d'accès non autorisé.
En complément de cette stratégie, nous avons mis en place un système de gestion des permissions basé sur les rôles (RBAC, Role-Based Access Control). Ce système assigne des permissions aux utilisateurs en fonction des rôles qu'ils occupent dans l’application. En définissant les rôles qui est une mesure fondamentale pour respecter le principe du moindre privilège, qui vise à limiter les permissions des utilisateurs uniquement à ce dont ils ont besoin pour accomplir leurs tâches.
