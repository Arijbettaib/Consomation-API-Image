# Application RecyclerView - Photos

Ceci est une application Android qui récupère une liste de photos à partir d'une API publique (jsonplaceholder.typicode.com) et les affiche dans un `RecyclerView`. L'application utilise **Retrofit** pour effectuer des appels réseau et **Gson** pour analyser les réponses JSON.

## Fonctionnalités

- Récupération d'une liste de photos à partir de l'API publique **jsonplaceholder**.
- Affichage des photos dans un `RecyclerView` avec un `Adapter` personnalisé.
- Gestion des erreurs de chargement avec des messages conviviaux pour l'utilisateur.

## Technologies utilisées

- **Java** : Langage de programmation utilisé pour développer l'application.
- **Android SDK** : SDK principal pour créer des applications Android.
- **RecyclerView** : Composant utilisé pour afficher une liste défilante de photos.
- **Retrofit** : Bibliothèque utilisée pour effectuer les appels réseau et récupérer les données depuis l'API.
- **Gson** : Bibliothèque pour la conversion des réponses JSON en objets Java.

## Prérequis

- Android Studio
- Une connexion Internet pour récupérer les données depuis l'API.

## Instructions de mise en place

1. **Cloner le dépôt** :
   Clonez ce projet en utilisant la commande suivante :
   ```bash
   git clone https://github.com/yourusername/recyclerview-photo-app.git
Ouvrir le projet dans Android Studio :

Ouvrez Android Studio.
Sélectionnez Open an existing project.
Naviguez vers le dossier où vous avez cloné le projet et ouvrez-le.
Vérifier les dépendances : Assurez-vous que votre fichier build.gradle (niveau app) contient les dépendances suivantes :

gradle
Copier
implementation 'com.squareup.retrofit2:retrofit:2.9.0'
implementation 'com.squareup.retrofit2:converter-gson:2.9.0'
implementation 'androidx.recyclerview:recyclerview:1.2.1'
Synchroniser le projet : Après avoir ajouté les dépendances, cliquez sur Sync Now dans Android Studio pour que les dépendances soient téléchargées et disponibles.

Point de terminaison API
L'application récupère les photos depuis l'API jsonplaceholder. Le point de terminaison utilisé est :

GET /photos : Ce point de terminaison renvoie une liste de photos.
Exemple de réponse de l'API
json

[
    {
        "albumId": 1,
        "id": 1,
        "title": "Accusamus ea aliquid et amet sequi nemo",
        "url": "https://via.placeholder.com/600/92c952",
        "thumbnailUrl": "https://via.placeholder.com/150/92c952"
    },
    {
        "albumId": 1,
        "id": 2,
        "title": "Reprehenderit est deserunt velit ipsam",
        "url": "https://via.placeholder.com/600/771796",
        "thumbnailUrl": "https://via.placeholder.com/150/771796"
    },
    ...
]
Composants principaux

RecyclerView est utilisé pour afficher une liste de photos récupérées depuis l'API.
Retrofit est utilisé pour effectuer un appel réseau afin de récupérer la liste de photos.
PhotosAdapter est utilisé pour lier les données récupérées avec le RecyclerView.
