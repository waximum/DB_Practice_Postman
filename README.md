# DB_Practice_Postman
1. Obtenir la liste de toutes les chaussures

	•	Méthode : GET
	•	URL : http://10.163.114.4:8081/shoes
	•	Description : Récupère la liste complète de toutes les chaussures disponibles dans la base de données.
	•	Exemple de réponse :
    
[
  {
    "id": 1,
    "name": "Running Shoes",
    "brand": "Nike",
    "size": 42,
    "price": 120,
    "description": "Comfortable running shoes with cushioning.",
    "image": "images/Running Shoes.png"
  },
  {
    "id": 2,
    "name": "Basketball Shoes",
    "brand": "Adidas",
    "size": 44,
    "price": 150,
    "description": "High-performance shoes for basketball players.",
    "image": "images/Basketball Shoes.png"
  },
  ...
]
2. Obtenir les détails d’une chaussure par ID

	•	Méthode : GET
	•	URL : http://10.163.114.4:8081/shoes/:id
	•	Paramètre :
	•	id : L’ID de la chaussure que vous souhaitez récupérer.
	•	Exemple : http://10.163.114.4:8081/shoes/1
	•	Description : Récupère les informations d’une chaussure spécifique en fonction de son ID.
	•	Exemple de réponse :
    {
  "id": 1,
  "name": "Running Shoes",
  "brand": "Nike",
  "size": 42,
  "price": 120,
  "description": "Comfortable running shoes with cushioning.",
  "image": "images/Running Shoes.png"
}
3. Obtenir tous les commentaires d’une chaussure spécifique

	•	Méthode : GET
	•	URL : http://10.163.114.4:8081/comments?shoeId=:shoeId
	•	Paramètre :
	•	shoeId : L’ID de la chaussure pour laquelle vous souhaitez obtenir les commentaires.
	•	Exemple : http://10.163.114.4:8081/comments?shoeId=1
	•	Description : Récupère tous les commentaires associés à une chaussure spécifique en filtrant par shoeId.
	•	Exemple de réponse :
    [
  {
    "id": 1,
    "shoeId": 1,
    "user": "Moussa Seck",
    "comment": "Great shoes for long runs!",
    "rating": 5
  },
  {
    "id": 2,
    "shoeId": 1,
    "user": "Jane Smith",
    "comment": "A bit tight, but very comfortable.",
    "rating": 4
  }
]
4. Ajouter une nouvelle chaussure

	•	Méthode : POST
	•	URL : http://10.163.114.4:8081/shoes
	•	Body (JSON) :
    {
  "name": "New Running Shoes",
  "brand": "Nike",
  "size": 42,
  "price": 130,
  "description": "Brand new running shoes with extra cushioning.",
  "image": "images/New Running Shoes.png"
}
	•	Description : Crée une nouvelle chaussure dans la base de données.

5. Ajouter un commentaire à une chaussure

	•	Méthode : POST
	•	URL : http://10.163.114.4:8081/comments
	•	Body (JSON) :
    {
  "shoeId": 1,
  "user": "New User",
  "comment": "Amazing comfort and style!",
  "rating": 5
}
	•	Description : Ajoute un nouveau commentaire pour une chaussure spécifique.

6. Mettre à jour les informations d’une chaussure

	•	Méthode : PUT
	•	URL : http://10.163.114.4:8081/shoes/:id
	•	Paramètre :
	•	id : L’ID de la chaussure à mettre à jour.
	•	Exemple : http://10.163.114.4:8081/shoes/1
	•	Body (JSON) :
    {
  "name": "Updated Running Shoes",
  "brand": "Nike",
  "size": 42,
  "price": 125,
  "description": "Updated description for the running shoes.",
  "image": "images/Updated Running Shoes.png"
}
	•	Description : Met à jour les informations d’une chaussure spécifique en fonction de son ID.

7. Supprimer une chaussure

	•	Méthode : DELETE
	•	URL : http://10.163.114.4:8081/shoes/:id
	•	Paramètre :
	•	id : L’ID de la chaussure à supprimer.
	•	Exemple : http://10.163.114.4:8081/shoes/1
	•	Description : Supprime une chaussure spécifique de la base de données.

8. Supprimer un commentaire

	•	Méthode : DELETE
	•	URL : http://10.163.114.4:8081/comments/:id
	•	Paramètre :
	•	id : L’ID du commentaire à supprimer.
	•	Exemple : http://10.163.114.4:8081/comments/1
	•	Description : Supprime un commentaire spécifique de la base de données.

    Instructions pour utiliser ces requêtes dans Postman

	1.	Créer une Collection : Dans Postman, créez une nouvelle collection pour organiser toutes vos requêtes.
	2.	Ajouter des Requêtes : Ajoutez chaque requête dans votre collection, en utilisant les URLs et les méthodes fournies ci-dessus.
	3.	Paramétrer les Requêtes GET, POST, PUT, DELETE : Assurez-vous de bien sélectionner le type de requête (GET, POST, PUT, DELETE) pour chaque requête. Pour les requêtes POST et PUT, définissez le body en JSON dans l’onglet “Body” de Postman.
	4.	Tester les Requêtes : Exécutez chaque requête pour tester votre API. Vous devriez obtenir les réponses JSON attendues, ou bien des messages de succès ou d’erreur selon l’opération effectuée.

Ces exercices vous permettront de vous familiariser avec les opérations CRUD (Create, Read, Update, Delete) en utilisant Postman et de manipuler les données de chaussures et de commentaires dans votre API. Bon entraînement !







