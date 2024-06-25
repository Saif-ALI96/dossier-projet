# Cécile --[**Discord-Simplon/doc/technical-proposition.md = line:23-->70**]

## 📄 Proposition d'une API

![API proposition image](https://i.imgur.com/OdKnUjw.png)

    Lors de nos réfléxions, la question de l'architecture API ou Monolithique s'est posée.
    Nous proposons d'utiliser une API car l'architecture d'une API est bien plus modulaire
    qu'une architecture monolithique, ce qui permet par exemple à d'autres développeurs
    d'utiliser notre application afin d'ajouter des fonctionnalités et d'être capable de créer
    de nouveaux outils à partir de notre de application.

    Cela permettra d'apporter une évolutivité du projet dans son ensemble en permettant l'agrégation
    de nouveaux outils sans besoin de retravailler l'architecture de l'application préalablement
    en plus de permettre l'utilisation de l'API en tant que source d'informations.

Nous avons choisi d'utiliser une architecture **RESTful** pour notre **API** car elle présente plusieurs avantages pour notre cas d'utilisation. <br>

- **l'interopérabilité** est un point clé pour notre API, qui doit être utilisable par un large éventail de clients et de technologies. L'utilisation de l'architecture RESTful nous permet de nous assurer que notre API sera compatible avec tout client qui parle HTTP.

- **l'évolutivité** est un autre aspect important pour notre API. Avec une architecture RESTful, nous pouvons facilement mettre à jour et changer les ressources sans impacter les clients existants. Cela nous permet de mieux gérer l'évolution de notre API au fil du temps.

- **La performance** est également un facteur important pour notre API, qui doit être capable de gérer un volume élevé de demandes. L'architecture RESTful nous permet de mieux gérer la charge et d'utiliser efficacement les ressources du serveur, ce qui améliore les performances de notre API.

- **la séparation des préoccupations** pour finir est un autre avantage de l'architecture RESTful. En donnant à chaque ressource une URL unique, nous pouvons mieux séparer les différentes parties de notre API et les maintenir de manière plus simple.

En résumé, l'architecture RESTful nous permet de créer une API interopérable, évolutive, performante et facile à maintenir, ce qui correspond parfaitement à nos besoins.

    Une API peut être considérée comme RESTful si elle respecte les principes de l'architecture REST. 
    Si une API ne respecte pas ces principes, elle ne peut pas être considérée comme RESTful, 
    même si elle utilise l'hypertext transfer protocol (HTTP) pour envoyer et recevoir des données.

Voici quelques exemples de situations où une **API REST** ne serait pas considérée comme **RESTful** :

- Si elle ne respecte pas le principe de l'uniformité de l'interface : dans l'architecture REST, toutes les ressources doivent être - identifiées de la même manière et le client doit être en mesure d'interagir avec elles de la même manière, quelle que soit leur emplacement ou leur type. Si une API ne respecte pas ce principe, elle ne peut pas être considérée comme RESTful.

- Si elle ne respecte pas le principe de l'étatless : dans l'architecture REST, chaque demande doit être indépendante et ne doit pas dépendre de l'état précédent de la conversation. Si une API nécessite que l'état soit conservé entre les demandes, elle ne peut pas être considérée comme RESTful.

- Si elle ne respecte pas le principe de la cache : dans l'architecture REST, les ressources doivent être clairement identifiées comme étant cacheables ou non. Si une API ne respecte pas ce principe, elle ne peut pas être considérée comme RESTful.

- Si elle ne respecte pas le principe de la séparation des préoccupations : dans l'architecture REST, chaque ressource doit avoir sa propre URL et ne doit pas dépendre des autres ressources. Si une API ne respecte pas ce principe, elle ne peut pas être considérée comme RESTful.

Nous avons également choisi d'utiliser un **Modèle Stateless** car celui-ci présente plusieurs avantages pour notre cas d'utilisation. <br>

- **La Scalabilité** : un modèle stateless permet de traiter les requêtes de manière indépendante, ce qui peut améliorer la scalabilité de l'application. En effet, le système n'a pas à conserver l'état de la session entre les requêtes, ce qui peut réduire la charge sur les ressources serveur.
- La Facilité de développement et de maintenance **: un modèle stateless rend l'application plus facile à développer et à maintenir, car le système n'a pas à gérer l'état de la session entre les requêtes. Cela peut réduire la complexité de l'application et faciliter l'ajout de nouvelles fonctionnalités.
- **Interopérabilité** : un modèle stateless rend l'application plus facile à intégrer à d'autres systèmes et à utiliser avec différents clients, car il ne nécessite pas de maintenir l'état de la session entre les requêtes. Cela peut être particulièrement utile dans le cas d'applications distribuées ou utilisant différents protocoles de communication.
- **La Sécurité** : un modèle stateless peut améliorer la sécurité de l'application en réduisant le risque de fuites d'informations sensibles liées à l'état de la session. En effet, comme le système n'a pas à conserver l'état de la session, il n'y a pas de données sensibles à protéger.

C'est pourquoi, notre proposition d'utilisation d'API s'est portée sur **l'API RESTful** avec un modèle **Stateless** plutôt qu'une **API REST** ou qu'un modèle **Stateful**.<br>

---

# Cécile --[**Discord-Simplon/doc/technical-proposition.md = line:72-->94**]

## ⚛️ Proposition de langage

![Langage proposition image](https://i.imgur.com/7kaaBB5.png)

La proposition de TypeScript plutôt que JavaScript a été motivé par plusieurs facteurs. <br>

Tout d'abord, TypeScript est un langage de programmation open-source qui est une extension de JavaScript,<br>
ajoutant la vérification de type statique au code, ce qui rends le debogage d'une application plus efficient.<br>

En plus de la vérification de type, TypeScript ajoute également un support de la programmation orientée objet au JavaScript,<br>
ce qui permet d'utiliser des concepts tels que les classes, les interfaces et les types génériques pour structurer le code de manière plus claire et plus évolutive.<br>

TypeScript est également connu pour sa meilleure documentation, grâce à la possibilité de définir les types de chaque variable et fonction dans le code. <br>
Cela rend la documentation plus complète et facilite la compréhension du code par d'autres développeurs,<br>
de ce fait, la maintenabilité et la lisibilité du code sont assurées de façon plus efficace.<br>

Enfin, TypeScript est compatible avec de nombreux outils et frameworks populaires pour le développement JavaScript, <br>
ce qui consistue un atout dans le cadre d'utilisation d'Angular par exemple.<br>

En résumé, TypeScript est un langage de programmation polyvalent et performant qui ajoute certains concepts<br> 
et une meilleure documentation au JavaScript, ce qui peut rendre le développement plus fiable et plus facile à maintenir.<br>

C'est pourquoi, notre proposition de langage s'est portée sur TypeScript plutôt que JavaScript.<br>

---
# Cécile --[**Discord-Simplon/doc/technical-proposition.md = line:179-->209 du doc**] 

## 🧐 Proposition d'ORM

![ORM proposition image](https://i.imgur.com/GPDIYHZ.jpg)

Nous proposons d'utiliser **TypeORM** en tant qu'ORM afin de sécuriser les<br> 
interactions entre l'application et les bases de données.<br>

Voici quelques raisons pour lesquelles **TypeORM** peut être un choix judicieux :<br>

**TypeORM** est un ORM entièrement conçu en **TypeScript**, ce qui correspond à nos besoins en termes de langage.<br>
Il dispose d'une large communauté de développeurs et d'une documentation détaillée,<br>
ce qui peut apporter un nombre conséquent de ressources en termes de résolution de problèmes éventuels<br>
pouvant survenir lors du développement, ainsi que de nombreuses solutions pour le développement des fonctionnalités<br> 
dont nous aurons besoin.
- **TypeORM** est un ORM **open source**, ce qui est intéressant en termes de<br>
liberté quant à l'utilisation et la manipulation de ce dernier.
- **TypeORM** est performant et est utilisé par un grand nombre de développeurs<br>
en raison de sa flexibilité. Il prend en charge de nombreux SGBD, dont **PostgreSQL**.
- **TypeORM** gère automatiquement les schémas de base de données en termes<br>
de création et de modifications, selon les modèles établis dans le code, ce qui<br>
permet de gagner du temps<br>
- **TypeORM** prend en charge la migration de base de données, ce qui permet de<br>
gérer plus facilement les mises à jour du schéma de base de données.<br>
- **TypeORM** est très intuitif et simple d'utilisation, <br>
ce qui rend la manipulation de bases de données facile et intuitive.

En résumé, **TypeORM** est un ORM complet et polyvalent qui peut s'intégrer facilement à notre projet<br> 
et nous offrir une gestion sécurisée et efficace des interactions avec les bases de données.<br>

Sa grande communauté de développeurs et sa documentation détaillée en font également,<br>
un choix de qualité pour le développement de notre application.<br>

---
# Cécile --[**Discord-Simplon/doc/technical-proposition.md = line:211-->fin du doc**] 
**↪️ /!\ sur cette partie, il y a dû y avoir une modification qui n'apparait pas dans le REPO (voir: line 142-->fin ici)**

## 👷‍♀️ Proposition de l'architecture d'application.

Nous proposons de ne pas utiliser une architecture micro-services pour notre application car elle présente plusieurs inconvénient, notament en ce qui est de la deadline :

- **Complexité accrue** : une architecture microservices peut être plus complexe à mettre en place et à maintenir qu'une architecture monolithe, car elle implique la mise en place de plusieurs services indépendants qui doivent être coordonnés.
- **Développement et déploiement plus longs** : le développement et le déploiement d'une application basée sur une architecture microservices peuvent être plus longs, car ils impliquent la mise en place et le déploiement de plusieurs services indépendants.
- **Intégration et tests plus complexes** : dans une architecture microservices, il peut être plus complexe de mettre en place des tests et de s'assurer que l'ensemble des services fonctionnent correctement ensemble.

En résumé, nous ne pouvons à l'heure actuelle opter pour une architecture micro-services par manque de temps mais également car cela require des compétences qu'aucun membre de Nore équipe dispose pour effectuer cela dans les temps.

## Choix de la couche N-tier

La couche N-tier (ou N-tier architecture) est une approche de design d'applications qui consiste à séparer l'application en plusieurs couches de responsabilité logiques. Chaque couche est responsable d'une tâche spécifique et peut être développée et mise à jour indépendamment des autres couches.

La couche d'administration sera développée en utilisant le Framework Angular pour gérer l'interface utilisateur du panel.

La couche logiciel de l'administration sera développée en utilisant le Framework NestJS pour gérer les interactions entre l'interface utilisateur et les données de l'application.

La couche logiciel publique sera développé en TS via l'API Discord pour permettre de gérer les interactions sur le logiciel Discord.

La couche de données sera développé en utilisant PostgreSQL et TypeORM pour gérer l'acces et la manipulation des données de l'application, qui seront stockées dans une base de données relationnelle.

En utilisant cette architecture N-tier, nous espérons rendre l'application plus facile à maintenir et à évoluer, tout en séparant clairement les responsabilités de chaque couche. Cela nous permettra également de développer et mettre à jour chaque couche de manière indépendante, ce qui accélère le processus de développement.

<<<<<<< HEAD
=======
## 👷‍♀️ Proposition de l'architecture d'application.

Nous proposons de ne pas utiliser une architecture micro-services pour notre application car elle présente plusieurs inconvénient, notament en ce qui est de la deadline :

- **Complexité accrue** : une architecture microservices peut être plus complexe à mettre en place et à maintenir qu'une architecture monolithe, car elle implique la mise en place de plusieurs services indépendants qui doivent être coordonnés.
- **Développement et déploiement plus longs** : le développement et le déploiement d'une application basée sur une architecture microservices peuvent être plus longs, car ils impliquent la mise en place et le déploiement de plusieurs services indépendants.
- **Intégration et tests plus complexes** : dans une architecture microservices, il peut être plus complexe de mettre en place des tests et de s'assurer que l'ensemble des services fonctionnent correctement ensemble.

En résumé, nous ne pouvons à l'heure actuelle opter pour une architecture micro-services par manque de temps mais également car cela require des compétences qu'aucun membre de Nore équipe dispose pour effectuer cela dans les temps.

## Choix de la couche N-tier

La couche N-tier (ou N-tier architecture) est une approche de design d'applications qui consiste à séparer l'application en plusieurs couches de responsabilité logiques. Chaque couche est responsable d'une tâche spécifique et peut être développée et mise à jour indépendamment des autres couches.

La couche d'administration sera développée en utilisant le Framework Angular pour gérer l'interface utilisateur du panel.

La couche logiciel de l'administration sera développée en utilisant le Framework NestJS pour gérer les interactions entre l'interface utilisateur et les données de l'application.

La couche logiciel publique sera développé via en TS via l'API discord pour permettre de gérer les interactions sur le logiciel Discord.

La couche de données sera développé en utilisant PostgreSQL et TypeORM pour gérer l'acces et la manipulation des données de l'application, qui seront stockées dans une base de données relationnelle.

En utilisant cette architecture N-tier, nous espérons rendre de l'application plus facile à maintenir et à évoluer, tout en séparant clairement les responsabilités de chaque couche. Cela nous permettra également de développer et mettre à jour chaque couche de manière indépendante, ce qui accélère le processus de développement.
>>>>>>> 9d97350 (docs(common) : add explication for ntiers choice)

---
# Cécile --[**Discord-Simplon/doc/benchmarks/back-end-framework.md**] 

# Introduction

Le présent document fait office de **fiche comparative** ou **Benchmark** concernant<br>
les différents Frameworks Back-end disponibles.<br>

Plus les points attribués sont hauts, plus l'entrée du **Benchmark** est qualitative.<br>
Nous nous sommes appuyés sur ce document afin de rédiger notre document de proposition<br>
technique.<br>

| Critères                 | Koa     | Fastify | Nest    | Adonis  |
| ------------------------ | ------- | ------- | ------- | ------- |
| Personnalisation         | 1       | 1       | 4       | 1       |
| Rapidité                 | 3       | 4       | 4       | 2       |
| Popularité               | 3       | 2       | 4       | 1       |
| Maturité                 | 4       | 2       | 1       | 3       |
| Releases                 | 1       | 4       | 2       | 3       |
| Bonnes pratiques         | 1       | 1       | 4       | 1       |
| Stars Github             | 3       | 2       | 4       | 1       |
| Equipe Développement     | 1       | 4       | 2       | 2       |
| Communauté Github        | 2       | 2       | 3       | 1       |
| Communauté StackOverflow | 2       | 2       | 4       | 1       |
| Documentation            | 1       | 2       | 4       | 4       |
| Magie                    | 1       | 1       | 1       | 1       |
| Mariage librairies       | 4       | 4       | 4       | 1       |
| Prise Politique          | 4       | 4       | 1       | 4       |
| Tarifs                   | Gratuit | Gratuit | Gratuit | Gratuit |
| License                  | MIT     | MIT     | MIT     | MIT     |
| Total                    | 31      | 35      | 42      | 26      |

---

# Cécile --[**Discord-Simplon/doc/benchmarks/orm.md**] 

# Introduction

Le présent document fait office de **fiche comparative** ou **Benchmark** concernant<br>
les différents ORM disponibles.<br>

Plus les points attribués sont hauts, plus l'entrée du **Benchmark** est qualitative.<br>
Nous nous sommes appuyés sur ce document afin de rédiger notre document de proposition<br>
technique.<br>

| Critères                 | TypeORM | Prisma  |
| ------------------------ | ------- | ------- |
| Rapidité                 | 2       | 1       | 
| Popularité               | 2       | 1       | 
| Maturité                 | 2       | 1       |
| Releases                 | 1       | 2       |
| Bonnes pratiques         | 1       | 2       | 
| Stars Github             | 2       | 1       |
| Equipe Développement     | 1       | 2       |
| Communauté Github        | 2       | 1       |
| Dernier commit           | 1       | 2       |
| Sonsors                  | 2       | 1       |
| Communauté StackOverflow | 2       | 2       |
| Documentation            | 1       | 2       |
| Prise Politique          | 1       | 0       |
| Tarifs                   | Gratuit | Gratuit |
| License                  | Apache2 | MIT     |
| Total                    | 20      | 18      |


*****************************************************************************************