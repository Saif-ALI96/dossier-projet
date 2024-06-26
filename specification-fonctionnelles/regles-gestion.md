### Règles de gestion

### Entités

**Utilisateur**

- **ID**: Identifiant unique de l'utilisateur (UUID)
- **Pseudo**: Nom de l'utilisateur
- **Email**: Adresse email de l'utilisateur

**Formation**

- **ID**: Identifiant unique de la formation (UUID)
- **Nom**: Nom de la formation
- **Type**: Type de formation
- **Date de début**: Date de début de la formation
- **Date de fin**: Date de fin de la formation
- **Statut**: La formation peut être active ou archivée

**Type de Formation**

- **ID**: Identifiant unique du type de formation (UUID)
- **Nom**: Nom du type de formation

**Invitation**

- **ID**: Identifiant unique de l'invitation (UUID)
- **Type d'invitation**: Indique si l'invitation est pour un apprenant ou un membre du staff
- **Lien d'invitation**: Lien généré pour l'invitation
- **Formation ID**: ID de la formation pour l'invitation
- **Validité**: Durée de validité du lien d'invitation
- **Utilisé**: Indique si le lien a été utilisé

### Gestion des Formations

**Création de Formation :**

- **Un administrateur, un directeur, le Staff Simplon, un Campus-manager ou un membre de Cap** peut créer une nouvelle formation en fournissant:
  - le nom
  - le type
  - la date de début
  - la date de fin

**Ajout d'Apprenant à une formation :**

- **Un administrateur, directeur, staff Simplon, campus-manager ou formateur**

- peut ajouter des apprenants ou utilisateurs existants à une formation.
- Les invitations sont envoyées avec des liens valides pour une seule personne et pour une durée déterminée.

**Fonctionnalités Formation :**

- Un administrateur, directeur, staff Simplon, campus-manager, Caps peut archiver ou de restaurer une formation active.
- Un administrateur, directeur campus-manager, Caps et formateur peut modifier les détails d'une formation.
- Un apprenant peut voir les formations auxquelles il est inscrit.

### Gestion des Invitations

**Création d'Invitation :**

- Un administrateur ou directeur peut générer une invitation pour un apprenant ou un membre du staff.
- L'invitation contient un lien unique, valable pour une seule personne et pour une durée déterminée.

**Utilisation d'Invitation :**

- Un utilisateur invité doit suivre le lien pour s'inscrire à la formation.
- Après utilisation, le lien d'invitation est marqué comme utilisé.

**Validation d'Invitation :**

- Un administrateur, directeur ou formateur doit valider l'identité du nouvel arrivant avant de lui attribuer le rôle.
