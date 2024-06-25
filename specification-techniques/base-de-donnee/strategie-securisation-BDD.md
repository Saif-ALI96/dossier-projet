### Sécurisation des accès aux données via l'ORM

Passer par un ORM pour accéder aux données protège contre les attaques par injection SQL en générant des requêtes sécurisées et paramétrées. Les ORM facilitent la validation et la normalisation des données, réduisent les erreurs et améliorent la gestion des accès aux données grâce à des contrôles basés sur les rôles. Ainsi, cela renforce la sécurité des données et la fiabilité de l'application.

### Journalisation et stratégie de sauvegarde

Journalisation : Nous allons enregistrer toutes les actions importantes dans la base de données, telles que les connexions et les modifications de données. Cela permettra de surveiller les activités suspectes et d'enquêter sur les incidents, assurant ainsi la sécurité et la traçabilité des données.
Stratégie de sauvegarde : Nous mettrons en place une stratégie de sauvegarde robuste pour protéger les données de l'application contre les incidents tels que les pannes, les erreurs ou les attaques. Nous effectuerons des sauvegardes régulières tout au long de la journée et des sauvegardes complètes chaque nuit. Cette combinaison assure que les données sont disponibles et intactes en cas de problème, garantissant la continuité et la sécurité des informations des utilisateurs.

### Politique de sécurité des mots de passe

En définissant des règles strictes pour leur création, gestion et récupération, nous réduisons les risques de compromission, prévenons les attaques et garantissons la confidentialité des données. Cette politique est essentielle pour maintenir la sécurité et la confiance dans nos systèmes.

● longueur des mots de passe minimum 12 caractères pour les Administrateurs et 8 pour les Utilisateurs.

● règles de complexité des mots de passe doit inclure au moins une lettre minuscule et une majuscule, au moins un chiffre et au moins un caractère spéciaux pour les Administrateurs et les Utilisateurs.

● mécanismes de limitation d’essais d’authentification (voir tous les mécanismes existant et appliquer les plus pertinent)

● mécanismes de contrôle de la robustesse des mots de passe
Vérification de robustesse : Nous utiliserons une bibliothèque spécialisée qui permet d'évaluer la force des mots de passe en analysant leur complexité. Si le mot de passe est jugé trop faible, des suggestions d'amélioration sont fournies.
Interdiction de mots de passe communs : Nous appliquerons une comparaison des nouveaux mots de passe à une liste de mots de passe courants. Cela permet d'éviter l'utilisation de mots de passe faciles à deviner et empêche les utilisateurs d'utiliser des mots de passe trop prévisibles, renforçant ainsi la sécurité de leurs comptes.
En combinant ces deux méthodes, on assure que les mots de passe sont à la fois complexes et uniques, renforçant ainsi la sécurité des utilisateurs.

● méthode de conservation des mots de passe
Les mots de passe doivent être stockés de manière sécurisée en utilisant un hachage avec salage.

● méthode de recouvrement d’accès en cas de perte ou de vol des mots de passe
Un lien de réinitialisation sécurisé sera envoyé par e-mail à l'Utilisateur. Ce lien est à usage unique et expire après 24 heures. Une fois le lien cliqué, l'Utilisateur sera redirigé vers une page web sécurisée où il pourra renouveler son mot de passe.
Pour les Administrateurs, la procédure est similaire, mais inclut une vérification par SMS. Un code de vérification unique sera envoyé par SMS à l'Administrateur, qui devra le saisir pour confirmer son identité avant de pouvoir réinitialiser son mot de passe.

## Protection des données

<!-- **client-documents/fr/cdc.md** -->

Dans le cadre de ce projet, il est assuré que certaines données relatives aux utilisateurs seront stockées. Cependant, étant sur le territoire européen, ce projet est soumis à la législation sur la protection des données (RGPD), ce qui signifie que les données des utilisateurs ne pourront être utilisées à d'autres fins que pour le bon fonctionnement de la solution.

De plus, nous avons établi que les données utilisateurs doivent être supprimées après un an à partir de la date à laquelle les données ont été utilisées pour la dernière fois.

En cas de cessation d'activité de la part de la solution ou d'un utilisateur, ces données seront totalement supprimées de nos bases de données.

Un utilisateur souhaitant connaître les informations stockées le concernant a tout à fait le droit de réclamer son droit de regard, et nous ne saurions nous soustraire à ce droit.

En ce sens, le client a un droit de regard sur toutes les données qui concerne son service.

### Conformité au RGPD (Règlement Général sur la Protection des Données)

Pour assurer la conformité de notre application aux normes de protection des données définies par le RGPD, notamment en France, nous avons mis en place les mesures suivantes :
Consentement explicite : Lors de la création de profil, les utilisateurs devront donner un consentement clair et explicite pour le traitement de leurs données personnelles.
Minimisation des données : Nous ne collecterons que les informations indispensables, telles que le nom, l'e-mail et les détails de paiement, nécessaires à la réservation.
Droits des utilisateurs : Les utilisateurs seront informés de leurs droits, incluant :

1. Le droit à la consultation : Les utilisateurs peuvent demander et obtenir l'accès à leurs données personnelles.
2. Le droit de rectification : Les utilisateurs peuvent corriger leurs données inexactes.
3. Le droit à l'effacement (droit à l'oubli) : Les utilisateurs peuvent demander la suppression de leurs
   données personnelles dans certaines circonstances.
4. Le droit de retirer leur consentement : Les utilisateurs peuvent retirer leur consentement au
   traitement de leurs données à tout moment
