App mise en ligne sur :

https://bmarchand.pythonanywhere.com/


## Documentation de l'API

**Vérifier si le serveur est actif**
- Endpoint : /api/alive
- Méthode : GET
- Description : Vérifie si le serveur est en fonctionnement.
- Réponse :
  - 200 OK : { "message": "Alive" }

**Liste de toutes les associations**
- Endpoint : /api/associations
- Méthode : GET
- Description : Retourne une liste de toutes les associations.
- Réponse :
  - 200 OK : Liste des noms des associations.

**Détails d'une association**
- Endpoint : /api/association/<int:id>
- Méthode : GET
- Description : Retourne les détails d'une association spécifique par son ID.
- Réponse :
  - 200 OK : Détails de l'association demandée.
  - 404 Not Found : { "error": "Association not found" }

**Liste de tous les événements**
- Endpoint : /api/evenements
- Méthode : GET
- Description : Retourne une liste de tous les événements.
- Réponse :
  - 200 OK : Liste des événements.

**Détails d'un événement**
- Endpoint : /api/evenement/<int:id>
- Méthode : GET
- Description : Retourne les détails d'un événement spécifique par son ID.
- Réponse :
  - 200 OK : Détails de l'événement demandé.
  - 404 Not Found : { "error": "Event not found" }

**Liste des associations par type**
- Endpoint : /api/associations/type/<type>
- Méthode : GET
- Description : Retourne une liste des associations par type (BDE, BDS, BDA, etc.).
- Réponse :
  - 200 OK : Liste des associations filtrées par type.

**Liste des événements d'une association**
- Endpoint : /api/association/<int:id>/evenements
- Méthode : GET
- Description : Retourne une liste des événements organisés par une association spécifique.
- Réponse :
  - 200 OK : Liste des événements de l'association demandée.

### Informations Générales

- Toutes les réponses sont au format JSON.
- Les codes de réponse HTTP standards sont utilisés pour indiquer le succès ou l'échec d'une requête.
- Pour les endpoints nécessitant un id, assurez-vous que l'ID est valide et existe dans la base de données pour éviter les erreurs 404 Not Found.
