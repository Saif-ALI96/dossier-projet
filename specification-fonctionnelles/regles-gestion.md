### Règles de gestion

#### Configuration du Bot

- Le bot doit disposer d'un système de configuration permettant de personnaliser ses fonctionnalités et comportements.

#### Gestion du Staff

- **Ajout des membres du staff** :
  - Commande de génération d'embed dans un canal pour ajouter des membres du staff.
  - L'embed doit inclure une liste déroulante pour sélectionner le rôle et générer un lien d'invitation.

#### Gestion des Formations

- **Création d'un nouveau type de formation** :

  - Commande de génération d'embed dans un canal pour créer un nouveau type de formation.
  - L'embed doit inclure un bouton pour envoyer une demande de nom pour le nouveau type de formation.

- **Ajout de formations** :
  - Commande de génération d'embed dans un canal pour ajouter une formation.
  - L'embed doit inclure une liste déroulante pour sélectionner le type de formation.
  - Une demande doit être envoyée pour compléter le nom de la formation.
  - Un nouvel embed doit être envoyé avec un bouton pour créer la formation.
  - Le bot doit demander la date de début et de fin de la formation.

#### Gestion des Apprenants

- **Ajout d'apprenants à une formation** :

  - Commande de génération d'embed dans un canal pour ajouter des apprenants.
  - L'embed doit inclure une liste déroulante pour générer un lien d'invitation spécifique à la formation.
  - Le lien d'invitation doit être valide pour une seule personne et temporaire.

- **Ajout de nouveaux utilisateurs présents sur le serveur à une formation** :
  - Commande de génération d'embed dans un canal pour ajouter des utilisateurs existants à une formation.
  - L'embed doit inclure une liste déroulante pour sélectionner une formation.
  - Un nouvel embed doit être envoyé avec un bouton pour afficher un formulaire d'ajout d'utilisateur.

#### Gestion des Catégories de Formation

- **Ajout ou modification de template de catégorie de formation** :

  - Commande de génération d'embed dans un canal pour ajouter ou modifier un template de catégorie de formation.
  - Une catégorie de formation est un ensemble de canaux dédiés à une formation.

- **Génération d'embed de configuration à la création d'une formation** :
  - Lors de la création d'une formation, le bot doit générer un embed de configuration dans un canal dédié à sa catégorie.
  - Le lien d'invitation généré par le bot doit fonctionner pour une seule personne et être temporaire.

#### Vérification et Sécurité

- **Détection et création d'embed** :

  - Le bot ne doit pas pouvoir créer deux fois le même embed de configuration.
  - Le bot doit pouvoir détecter si un embed a été supprimé pour permettre la création d'un nouveau.
  - Les administrateurs peuvent supprimer un embed.

- **Vérification à l'ajout d'utilisateur** :
  - Lors de l'ajout d'un utilisateur à une formation, le bot doit envoyer une demande de vérification dans un canal dédié à cette formation.
  - Le bot doit imposer une identification lors de l'arrivée d'un nouvel apprenant ou d'un nouveau membre du staff.
  - Lors de l'arrivée d'un nouvel apprenant, le bot doit envoyer un message de demande de vérification dans un canal dédié à cette formation.
  - Lors de l'arrivée d'un nouveau staff, le bot doit envoyer un message de demande de vérification dans un canal dédié au staff.
  - Une fois la vérification de l'identité validée, le rôle doit être attribué par le bot à l'utilisateur du lien.

#### Sélection des Formations Visibles

- **Visibilité des formations pour le staff** :
  - Le bot doit mettre en place un embed dans un canal permettant de sélectionner les formations visibles pour le staff.
