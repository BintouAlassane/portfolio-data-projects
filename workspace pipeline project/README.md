# Analyse de la Demande et de l'Offre des Ventes Walmart pendant les Vacances

## Contexte
Ce projet consiste à construire un pipeline de données pour analyser les ventes de Walmart autour des périodes de vacances. L'objectif est d'étudier l'impact des jours fériés sur l'offre et la demande en utilisant des données provenant de ventes d'épicerie et de données complémentaires (température, prix des carburants, taux de chômage, etc.).



## 🎯 Objectifs
1. **Fusion des données** : Combiner les données de ventes et les données supplémentaires
2. **Nettoyage des données** : Sélectionner les colonnes nécessaires et extraire les mois à partir des dates
3. **Analyse des ventes mensuelles** : Agréger les ventes par magasin et par département
4. **Export des données** : Sauvegarder les résultats sous forme de fichiers CSV (`clean_data.csv` et `agg_data.csv`)



## 📂 Données utilisées
### 1. **grocery_sales** (table PostgreSQL mais ici sous format csv)
- `index` : Identifiant unique de la ligne
- `Store_ID` : Identifiant du magasin
- `Date` : Date de la semaine des ventes
- `Weekly_Sales` : Ventes hebdomadaires du magasin

### 2. **extra_data.parquet** (fichier Parquet)
- `IsHoliday` : Indique si la semaine comprend un jour férié (1 : Oui, 0 : Non)
- `Temperature` : Température pendant la vente
- `Fuel_Price` : Prix des carburants
- `CPI` : Indice des prix à la consommation
- `Unemployment` : Taux de chômage
- `MarkDown1` à `MarkDown4` : Promotions spéciales
- `Dept` : Numéro du département
- `Size` : Taille du magasin
- `Type` : Type de magasin (en fonction de la taille)



## ⚙️ Étapes du pipeline de données :
1. **Chargement des données** :
   - Connexion à la base PostgreSQL pour extraire les données `grocery_sales`
   - Chargement des données `extra_data.parquet`
2. **Fusion des données** : Combinaison des deux sources sur les colonnes `Date` et `Store_ID`
3. **Nettoyage et transformation** :
   - Conversion des dates au format `datetime`
   - Extraction du mois et ajout d'une colonne `Month`
   - Sélection des colonnes pertinentes pour l'analyse
4. **Agrégation** :
   - Calcul des ventes totales mensuelles (`Total_Sales`)
   - Moyenne des indices CPI (`Avg_CPI`) et des taux de chômage (`Avg_Unemployment`)
5. **Exportation des données** :
   - Sauvegarde des données nettoyées sous `clean_data.csv`
   - Sauvegarde des données agrégées sous `agg_data.csv`


## 🛠 Technologies utilisées
- **Langage** : Python
- **Bibliothèques** :
  - `pandas` : Manipulation des données


## Exécution du projet
### Pré-requis :
- Python 3.8 ou supérieur


### Instructions :
1. **Exécution** : Lancez le script principal pour fusionner, nettoyer et analyser les données

