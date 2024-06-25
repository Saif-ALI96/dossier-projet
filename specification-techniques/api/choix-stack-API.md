## Choix de stacks pour l'API

- ### RESTFUL API

  Nous avons choisi d'utiliser une architecture RESTful pour notre API car elle présente plusieurs avantages pour notre cas d'utilisation.

  l'interopérabilité est un point clé pour notre API, qui doit être utilisable par un large éventail de clients et de technologies. L'utilisation de l'architecture RESTful nous permet de nous assurer que notre API sera compatible avec tout client qui parle HTTP.

  l'évolutivité est un autre aspect important pour notre API. Avec une architecture RESTful, nous pouvons facilement mettre à jour et changer les ressources sans impacter les clients existants. Cela nous permet de mieux gérer l'évolution de notre API au fil du temps.

  La performance est également un facteur important pour notre API, qui doit être capable de gérer un volume élevé de demandes. L'architecture RESTful nous permet de mieux gérer la charge et d'utiliser efficacement les ressources du serveur, ce qui améliore les performances de notre API.

  la séparation des préoccupations pour finir est un autre avantage de l'architecture RESTful. En donnant à chaque ressource une URL unique, nous pouvons mieux séparer les différentes parties de notre API et les maintenir de manière plus simple.

- ### TypeScript

  La proposition de TypeScript plutôt que JavaScript a été motivé par plusieurs facteurs.

  Tout d'abord, TypeScript est un langage de programmation open-source qui est une extension de JavaScript,
  ajoutant la vérification de type statique au code, ce qui rends le debogage d'une application plus efficient.

  En plus de la vérification de type, TypeScript ajoute également un support de la programmation orientée objet au JavaScript,
  ce qui permet d'utiliser des concepts tels que les classes, les interfaces et les types génériques pour structurer le code de manière plus claire et plus évolutive.

  TypeScript est également connu pour sa meilleure documentation, grâce à la possibilité de définir les types de chaque variable et fonction dans le code.
  Cela rend la documentation plus complète et facilite la compréhension du code par d'autres développeurs,
  de ce fait, la maintenabilité et la lisibilité du code sont assurées de façon plus efficace.

  Enfin, TypeScript est compatible avec de nombreux outils et frameworks populaires pour le développement JavaScript,
  ce qui consistue un atout dans le cadre d'utilisation d'Angular par exemple.

- ### Node.js

  - **Facilité de création d'applications Web**

    Node.js dispose d'une large gamme
    de frameworks pour le développement back-end et front-end,
    ce qui rend la création d'applications Web très facile.

  - **Environnement complet et puissant**
    Node.js est un environnement complet et puissant,
    avec une large communauté de développeurs.
    Cela permet d'avoir accès à de nombreuses ressources et à une documentation fournie.

  - **Développement de bots Discord**
    Dans le cadre de ce projet, nous souhaitons
    développer des bots Discord.
    Node.js offre une grande flexibilité et des performances élevées,
    ainsi qu'un large choix d'outils pour faciliter la communication entre les bots et Discord.
    - **Utilisation d'un seul environnement**
      Enfin, en choisissant Node.js comme
      environnement d'exécution, nous pouvons développer à la fois des bots Discord et une
      interface Web de configuration de ces bots et de consultation de données sur le serveur communautaire,
      tout en utilisant un seul et même environnement.

  **Node.js** a donc été retenu en tant qu'environnement d'exécution pour ce projet en raison de sa facilité de mise en place,de sa flexibilité, de ses hautes performances, de sa large communauté et de la disponibilité d'outils pour la communication avec Discord.
