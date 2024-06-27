# Règles de gestion


## Définition des Entités

**bot** : *est un assistant qui aide à automatiser les tâches sur le serveur.*

**embed** : *est une fiche d'information interactive qui apparaît dans les messages.*

**lien d'invitation** : *est un lien qui permet à une nouvelle personne de rejoindre un serveur.*

**administrateur** : *est une personne qui a le pouvoir de modifier et de contrôler les paramètres d'un serveur.*

**catégorie de formation** : *est un ensemble de canaux dédiés à une formation.*


## Règles bot OnBoarding

- Un **bot** <u>doit disposer</u> d'un **système de configuration**.

  - Le **bot** doit avoir une commande de génération d'**embed** (dans un canal) pour l'ajout des membres du staff.

    - L'**embed** doit disposer d'une liste déroulante permettant de sélectionner le rôle afin de générer un **lien d'invitation**.

  - Le **bot** doit avoir une commande de génération d'**embed** (dans un canal) pour la création d'un nouveau type de formation.

    - L'**embed** doit disposer d'un bouton permettant d'envoyer une **demande** de nom pour le nouveau type de formation.
---

- Le **bot** doit avoir une commande de génération d'**embed** (dans un canal) pour l'ajout de formation.

    - L'**embed** doit disposer d'une liste déroulante permettant la sélection du type de formation.

      - Une **demande** doit être envoyée pour demander de compléter le nom de la formation.

      - Un nouvel **embed** doit être envoyé et doit disposer d'un bouton permettant de créer une nouvelle formation.

      - Le **bot** doit envoyer un message demandant la date de début et de fin de la formation.

      - À la date de fin de formation, le **bot** doit activer un bouton 'Terminer la promotion' (qui était grisé) pour cloturer la formation.
    
    - Après création d'une promotion, le **bot** doit permettre de toujours pouvoir éditer la date et le nom de la formation.

    - Lorsqu'un formateur souhaite supprimer une promotion, le **bot** doit envoyer une demande de suppression à l'**administrateur**.

      -  L'**administrateur** doit pouvoir exécuter la suppression de la formation.

  - Le **bot** doit avoir une commande de génération d'**embed** (dans un canal) pour l'ajout d'apprenants à une formation.

    - L'**embed** doit disposer d'une liste déroulante permettant de générer un **lien d'invitation** pour un nouvel apprenant, à une formation spécifique.

      - Le **lien d'invitation** doit être valide pour une seule personne.

  - Le **bot** doit avoir une commande de génération d'**embed** (dans un canal) pour l'ajout de nouveaux utilisateurs déjà présents sur le serveur Discord, à une formation.

    - L'**embed** doit disposer d'une liste déroulante permettant de sélectionner une formation spécifique.

      - Lors de la sélection de la formation, un nouvel **embed** doit être envoyé, il doit disposer d'un bouton permettant d'afficher un formulaire d'ajout d'utilisateur.

  - Le **bot** doit avoir une commande de génération d'**embed** pour l'ajout ou la modification de template de catégorie de formation.

    - Le **bot** doit à la création d'une formation, générer un **embed** de configuration dans un channel propre à sa catégorie.
---

- Le **lien d'invitation** généré par le **bot** ne doit fonctionner que pour une personne.
---

- Le **lien d'invitation** doit être temporaire.
---

- Le **bot** ne doit pas pouvoir créer deux fois le même **embed** de configuration.
---

- Le **bot** doit pouvoir détecter si un **embed** a été supprimé pour permettre la création d'une nouvelle.
---

- L'**administrateur** peut supprimer un **embed**.
---

- Lors de l'ajout d'un utilisateur à une formation, le **bot** doit envoyer une demande de vérification (dans un canal dédié à cette formation).
---

- Le **bot** doit imposer une identification lors de l'arrivée d'un nouvel apprenant ou nouveau membre du staff.

  - Lors de l'arrivée d'un nouvel apprenant, le **bot** doit envoyer un message de demande de vérification (dans un canal dédié à cette formation).

  - Lors de l'arrivée d'un nouveau staff, le **bot** doit envoyer un message de demande de vérification (dans un canal dédié au staff).

    - Une fois la vérification de l'identité validée, le rôle doit être attribué par le **bot** à l'utilisateur du lien.
---

- Le **bot** doit mettre en place un **embed** (dans un canal) permettant de sélectionner les formations visibles pour le staff.