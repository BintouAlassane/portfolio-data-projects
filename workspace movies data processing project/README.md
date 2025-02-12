# Système de recommandation sur le dataset MovieLens 

## Contexte
Ce projet porte sur la création d’un système de recommandation de films à partir du jeu de données MovieLens 
L’objectif est d’offrir des recommandations personnalisées en fonction des préférences des utilisateurs et de prédire les notes des films non évalués

## 🎯 Objectifs
- Analyser le jeu de données pour en extraire des informations pertinentes.
- Construire des modèles de régression pour prédire les revenus et la moyenne des votes des films.
- Développer un système de recommandation

## 📂 Données utilisées
Le jeu de données est accessible [ici](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset) et se compose de :
- `movies_metadata.csv` : Métadonnées sur 45 000 films (budget, société de production, etc.)
- `keywords.csv` : Mots-clés des intrigues des films (format JSON)
- `credits.csv` : Informations sur la distribution et l'équipe de production
- `links.csv` : Identifiants TMDB et IMDB des films
- `ratings.csv` : 26 millions d’évaluations sur une échelle de 1 à 5

## 🔍 Méthodologie
1. **Analyse des données** : Identification des corrélations, des tendances et nettoyage des données
2. **Modélisation** :
   - Création d’un système de recommandation basé sur :
     - Le contenu des films
     - Le comportement des utilisateurs
3. **Prédiction** : Calcul des notes prédictives à l’aide de méthodes statistiques (médiane, mode)

## ⚙️ Instructions d'exécution
1. **Installation** :
   - Installer les dépendances nécessaires (Python, bibliothèques : pandas, scikit-learn, etc.)
2. **Chargement des données** :
   - Placer les fichiers de données dans le répertoire racine
3. **Exécution** :
   - Lancer le script principal pour générer les recommandations et les prédictions

## 🛠 Technologies
- **Langage** : Python
- **Bibliothèques** : Pandas, NumPy, Scikit-learn, Matplotlib
- **Modèles** : Filtrage, modèles de régression
