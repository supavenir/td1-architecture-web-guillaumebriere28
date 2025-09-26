# Client Serveur Web - Architecture
## 1 - Méthodes GET et POST
### Méthode GET
#### 📌 But :

Envoyer une requête pour obtenir des données à partir du serveur.

#### ✅ Caractéristiques :

Les données sont envoyées dans l’URL (en tant que paramètres).

Moins sécurisé (visible dans l'historique, les logs, etc.).

Limité en taille (environ 2048 caractères).

Peut être mise en cache.

#### 📘 Exemple concret : Rechercher un produit sur un site e-commerce

##### URL utilisée :

https://www.maboutique.com/search?query=chaussures&couleur=noir

Requête envoyée au serveur :

GET /search?query=chaussures&couleur=noir HTTP/1.1
Host: www.maboutique.com

#### Données échangées :

query=chaussures

couleur=noir

➡️ Le serveur renvoie une page avec les résultats de la recherche.

### Méthode POST
#### 📌 But :

Envoyer des données vers le serveur (souvent pour créer ou modifier des ressources).

#### ✅ Caractéristiques :

Les données sont envoyées dans le corps (body) de la requête.

Plus sécurisé (les données ne sont pas visibles dans l’URL).

Pas de limite de taille pratique (utile pour des formulaires, fichiers, etc.).

Non mis en cache.

#### 📘 Exemple concret : Soumettre un formulaire d’inscription

##### URL utilisée :

https://www.maboutique.com/signup

##### Requête envoyée au serveur :

POST /signup HTTP/1.1
Host: www.maboutique.com
Content-Type: application/x-www-form-urlencoded

nom=Durand&email=durand@example.com&motdepasse=monSuperMotDePasse123

##### Données échangées :

nom = Durand

email = durand@example.com

motdepasse = monSuperMotDePasse123

➡️ Le serveur traite l’inscription, enregistre l’utilisateur et renvoie une réponse (confirmation, redirection, etc.).


## 2 – Comparaison méthodes
