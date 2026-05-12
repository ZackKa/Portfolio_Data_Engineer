# Projet 5 — Migration de données médicales vers MongoDB & Conteneurisation Docker
## 📌 Contexte du projet

Dans le cadre de mon parcours Data Engineer, j’ai réalisé une mission pour l’entreprise DataSoluTech.

L’objectif était d’accompagner un client confronté à des problèmes de scalabilité sur ses traitements de données médicales en migrant un dataset CSV vers une architecture NoSQL MongoDB, automatisée et conteneurisée avec Docker.

Le projet incluait également une réflexion autour d’un futur déploiement cloud sur AWS.

## 🎯 Objectifs du projet

Le projet avait plusieurs objectifs :

- Migrer un dataset médical vers MongoDB
- Automatiser la migration avec Python
- Conteneuriser l’infrastructure avec Docker
- Mettre en place un système d’authentification sécurisé
- Optimiser les performances avec des index MongoDB
- Tester la qualité et l’intégrité des données
- Étudier des solutions de déploiement cloud AWS

## 🏗️ Architecture du projet
```text
CSV → Python (ETL) → MongoDB → Docker → Tests
```

## 🛠️ Outils & Technologies utilisés

| Catégorie                | Technologies                           |
|--------------------------|----------------------------------------|
| Langage                  | Python                                 |
| Base NoSQL               | MongoDB                                |
| Conteneurisation         | Docker / Docker Compose                |
| Librairies Python        | pandas, pymongo, pytest                |
| Tests                    | pytest                                 |
| Gestion des dépendances  | requirements.txt                       |
| Versionning              | Git / GitHub                           |
| Cloud étudié             | AWS (DocumentDB, ECS, S3)              |

## 📂 Travaux réalisés
### 1️⃣ Migration des données vers MongoDB
#### Actions réalisées
- Analyse du dataset médical CSV
- Contrôle qualité des données :
    - doublons
    - valeurs manquantes
    - typage
    - cohérence des colonnes
- Création d’un script Python de migration
- Insertion des données dans MongoDB

#### Résultat
- 55 500 documents médicaux importés avec succès
- Migration entièrement automatisée

### 2️⃣ Modélisation MongoDB
#### Structure mise en place

```text
medical_db
└── patients
```

Chaque ligne du CSV a été transformée en document BSON MongoDB.

#### Champs principaux
- Name
- Age
- Gender
- Blood Type
- Medical Condition
- Doctor
- Hospital
- Billing Amount
- Admission Type
- Medication

### 3️⃣ Implémentation des opérations CRUD

Des scripts Python ont été développés pour :

- CREATE → ajout de patients
- READ → lecture et filtrage
- UPDATE → modification de documents
- DELETE → suppression de documents

### 4️⃣ Optimisation des performances
#### Création d’index MongoDB

Indexes créés sur :

- Name
- Medical Condition
- Doctor
- Date of Admission

#### Objectif

Améliorer :

- les temps de recherche
- les filtres analytiques
- les requêtes métier

### 5️⃣ Conteneurisation avec Docker
#### Infrastructure Docker mise en place

Le projet a été entièrement conteneurisé avec :

- MongoDB
- scripts Python de migration
- volumes persistants
- réseau Docker dédié

#### Éléments créés
- docker-compose.yml
- Dockerfile
- volumes persistants
- scripts d’initialisation MongoDB

#### Résultat

Infrastructure :

- portable
- reproductible
- scalable
- facilement déployable

### 6️⃣ Sécurisation MongoDB
#### Système d’authentification mis en place

Création de plusieurs rôles utilisateurs :

| Utilisateur | Rôle                    |
|--------------|--------------------------|
| admin_user   | administration complète |
| rw_user      | lecture / écriture      |
| read_user    | lecture seule           |

#### Objectif

Appliquer :

- séparation des privilèges
- sécurité des accès
- bonnes pratiques DevOps

### 7️⃣ Tests automatisés
#### Tests unitaires développés avec pytest

Vérifications automatiques :

- validation du dataset
- absence de doublons
- bon fonctionnement des index
- connexion MongoDB
- intégrité des insertions

Résultat

Pipeline plus fiable et reproductible.

## ☁️ Recherches AWS réalisées

Une étude technique a été menée sur plusieurs services AWS :

| Service AWS       | Utilité                                |
|-------------------|----------------------------------------|
| Amazon DocumentDB | MongoDB managé                         |
| Amazon ECS        | orchestration Docker                   |
| Amazon S3         | stockage et sauvegardes                |
| Amazon RDS        | comparaison architecture relationnelle |

## 📈 Résultats obtenus

#### ✔ Migration réussie
- 55 500 documents importés
- Données validées avant insertion
- Infrastructure automatisée et reproductible
- pipeline automatisé
- base scalable
- requêtes optimisées

#### ✔ Amélioration de la scalabilité

MongoDB permet :

- une meilleure gestion des gros volumes
- une architecture flexible
- une scalabilité horizontale

#### ✔ Projet totalement reproductible

Grâce à Docker :

- déploiement simplifié
- environnement identique partout
- isolation des services

#### ✔ Sécurisation des accès
- authentification activée
- rôles utilisateurs séparés
- limitation des privilèges

## 🧠 Compétences démontrées
#### Data Engineering
Migration de données
Validation & qualité des données
Automatisation de pipelines
Gestion de bases NoSQL

#### MongoDB
Collections & documents
CRUD
Indexation
Authentification
Gestion des rôles

#### Docker & DevOps
Docker Compose
Conteneurisation
Volumes persistants
Isolation des services

#### Qualité & Tests
Tests automatisés
Validation de données
Contrôle d’intégrité

#### Cloud & Architecture
Architecture scalable
Réflexion cloud AWS
Étude d’industrialisation

## 🚀 Valeur ajoutée du projet

Ce projet démontre ma capacité à :

- concevoir une architecture NoSQL moderne ;
- automatiser des traitements de données ;
- sécuriser une infrastructure MongoDB ;
- utiliser Docker dans un contexte Data Engineering ;
- préparer une solution scalable pour le cloud ;
- documenter et industrialiser un pipeline de migration.

Il illustre également une approche complète :

`compréhension métier → migration → automatisation → sécurisation → scalabilité → préparation cloud`

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_5_data