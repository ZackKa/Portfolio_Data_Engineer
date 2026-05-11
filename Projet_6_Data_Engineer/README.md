# 🌆 Projet 6 — Prédiction de la consommation énergétique des bâtiments de Seattle & Déploiement ML API
## 📌 Contexte du projet

Ce projet a été réalisé autour d’un cas concret proposé par la ville de Seattle.

L’objectif était de développer un modèle de Machine Learning capable de prédire :

- la consommation énergétique ;
- les émissions de CO₂ ;

des bâtiments non résidentiels à partir de leurs caractéristiques structurelles.

Le projet répond à un enjeu environnemental fort : aider la ville de Seattle à atteindre son objectif de neutralité carbone d’ici 2050.

Une seconde partie du projet consistait à industrialiser le modèle via :

- une API REST avec BentoML ;
- une validation des données avec Pydantic ;
- une conteneurisation Docker ;
- un déploiement Cloud sur Google Cloud Platform (GCP).

## 🎯 Objectifs du projet

- Réaliser une analyse exploratoire des données énergétiques des bâtiments ;
- Préparer et transformer les données pour la modélisation ;
- Tester plusieurs modèles supervisés de régression ;
- Identifier les variables ayant le plus d’impact sur la consommation énergétique ;
- Construire une API de prédiction en temps réel ;
- Déployer le modèle dans un environnement Cloud.

## 🛠 Technologies & Outils utilisés
### Data Science & Machine Learning
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
### API & MLOps
- BentoML
- Pydantic
- Swagger UI
### Conteneurisation & Cloud
- Docker
- Google Cloud Platform (GCP)
- Google Cloud Run
- Artifact Registry
- Google Cloud SDK

## 📊 Données utilisées

Dataset officiel de la ville de Seattle :

- bâtiments non résidentiels ;
- caractéristiques structurelles ;
- surface totale ;
- nombre d’étages ;
- âge des bâtiments ;
- usages des bâtiments ;
- consommation énergétique ;
- émissions carbone.

## 🔍 Travaux réalisés
### 📈 Analyse exploratoire des données (EDA)

Réalisation d’une analyse complète afin de :

- comprendre la structure des données ;
- détecter les valeurs incohérentes ;
- identifier les valeurs manquantes ;
- analyser les distributions ;
- identifier les variables les plus pertinentes.

#### Exemples d’analyses :
- consommation énergétique selon la taille des bâtiments ;
- impact du nombre d’étages ;
- influence de l’ancienneté des bâtiments ;
- analyse des bâtiments atypiques.

## ⚙️ Feature Engineering

Création et sélection de variables pertinentes :

- âge du bâtiment ;
- ratio d’étages par surface ;
- nombre de types d’usages ;
- indicateur de grands bâtiments ;
- surface de parking ;
- nombre de bâtiments.

Nettoyage et préparation des données :

- suppression des incohérences ;
- gestion des outliers ;
- encodage ;
- scaling.

## 🤖 Modélisation Machine Learning
### Modèles testés
- Régression linéaire
- Random Forest Regressor
- autres modèles supervisés de régression

### Évaluation des performances
- Validation croisée
- MAE
- R²
- séparation train/test
- optimisation des hyperparamètres avec GridSearchCV

### Modèle retenu

Un modèle RandomForestRegressor optimisé offrant les meilleures performances globales.

## 📌 Interprétation du modèle

Analyse des variables les plus importantes influençant la consommation énergétique :

- surface totale du bâtiment ;
- nombre d’étages ;
- âge du bâtiment ;
- surface de parking ;
- diversité des usages.

Cette analyse permet d’apporter une lecture métier des résultats du modèle.

## 🚀 Industrialisation du modèle
### API REST avec BentoML

Création d’une API permettant à un utilisateur d’obtenir une prédiction énergétique en temps réel à partir des informations d’un bâtiment.

#### Endpoint principal :

`/predict`

#### Fonctionnalités :
- chargement du modèle sauvegardé ;
- inférence en temps réel ;
- documentation Swagger automatique ;
- validation des entrées utilisateur.

## ✅ Validation des données avec Pydantic

Implémentation de règles de validation afin d’empêcher l’envoi de données incohérentes :

#### Exemples :
- surfaces strictement positives ;
- nombre d’étages valide ;
- âge réaliste du bâtiment ;
- surface parking ≤ surface totale.

## 🐳 Conteneurisation Docker

Création d’une image Docker complète contenant :

- le modèle ML ;
- l’API BentoML ;
- les dépendances Python ;
- les fichiers nécessaires au serving.

Résultat :

- environnement portable ;
- reproductibilité ;
- déploiement simplifié.

## ☁️ Déploiement Cloud sur GCP

Déploiement du modèle sur :

- Google Cloud Run ;
- Artifact Registry.

### Travaux réalisés
- création d’un projet GCP ;
- configuration du SDK ;
- création d’un registre Docker ;
- push des images ;
- déploiement du service REST ;
- tests du endpoint cloud.

Le modèle devient ainsi accessible via une URL publique.

## 📈 Résultats obtenus

✅ Modèle ML fonctionnel pour la prédiction énergétique des bâtiments
✅ API REST opérationnelle avec Swagger
✅ Validation des données utilisateur
✅ Déploiement Cloud fonctionnel sur GCP
✅ Architecture portable et industrialisable via Docker

## 🧠 Compétences démontrées
### Data Engineering
- préparation et nettoyage de données ;
- feature engineering ;
- gestion de pipelines ML.

### Machine Learning
- modélisation supervisée ;
- validation croisée ;
- optimisation d’hyperparamètres ;
- interprétation de modèles.

### API & MLOps
- BentoML ;
- création d’API ML ;
- validation Pydantic ;
- serving de modèles.

### Cloud & DevOps
- Docker ;
- Google Cloud Platform ;
- Cloud Run ;
- Artifact Registry ;
- déploiement de services conteneurisés.

## 💡 Valeur ajoutée du projet

Ce projet montre la capacité à :

- transformer un modèle ML en service exploitable ;
- industrialiser une solution Data Science ;
- déployer une API scalable dans le cloud ;
- combiner Data Engineering, Machine Learning et MLOps (Machine Learning Operations) ;
- produire une solution prête pour un usage métier réel.

Il met également en avant des compétences de mise en production, essentielles dans les environnements Data modernes.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet6_data