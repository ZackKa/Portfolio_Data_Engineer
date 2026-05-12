# Projet 8 — GreenAndCoop Forecast 2.0

## Présentation

Dans ce projet réalisé en tant que **Data Engineer**, j’ai conçu un pipeline de données permettant de collecter, transformer, stocker et superviser des données météorologiques utilisées pour améliorer les modèles de prévision électrique de GreenAndCoop.

L’objectif était d’intégrer des données issues de plusieurs sources météo hétérogènes (InfoClimat et Weather Underground) afin de fournir des données fiables et exploitables aux équipes Data Science.

---

# Objectifs du projet

* Centraliser des données météo multi-sources
* Harmoniser les formats JSON et Excel
* Contrôler la qualité des données
* Stocker les données dans MongoDB
* Déployer une architecture cloud sur AWS
* Mettre en place supervision, réplication et sauvegardes


# Stack technique

## Data Engineering

* Python
* Airbyte
* MongoDB
* Amazon S3

## Cloud & DevOps

* Docker
* Docker Compose
* AWS ECS
* AWS EC2
* AWS CloudWatch
* IAM

---

# Architecture du pipeline

```text
Sources météo
        ↓
Airbyte
        ↓
Amazon S3 (RAW)
        ↓
Transformation Python
        ↓
Amazon S3 (PROCESSED)
        ↓
MongoDB
        ↓
Monitoring & Backups AWS
```


# Réalisations principales

## Ingestion des données

* Collecte automatisée via Airbyte
* Stockage des données brutes dans Amazon S3
* Gestion de formats hétérogènes (JSON / Excel)

## Transformation des données

* Standardisation des schémas
* Harmonisation des champs météo
* Reconstruction de timestamps manquants
* Intégration des métadonnées des stations météo

## Contrôle qualité

Mise en place de scripts automatisés permettant de vérifier :

* les doublons ;
* les valeurs manquantes ;
* les champs critiques ;
* la cohérence des données.

Résultat obtenu :

```text
4950 documents
0 doublon
0 % d’erreur
```

## Migration MongoDB

* Import automatisé depuis S3 vers MongoDB
* Création d’une architecture Replica Set
* Vérification de l’intégrité post-import

## Conteneurisation

* Déploiement avec Docker Compose
* Isolation des services
* Persistance des données via volumes Docker

## Déploiement AWS

* Déploiement MongoDB sur AWS ECS puis EC2
* Monitoring centralisé avec CloudWatch
* Sauvegardes automatisées vers Amazon S3
* Mesure du temps d’accessibilité aux données


# Résultats

Le projet a permis de construire une architecture Data Engineering complète et industrialisée :

* pipeline automatisé ;
* ingestion multi-sources ;
* qualité des données contrôlée ;
* réplication MongoDB ;
* déploiement cloud AWS ;
* monitoring et sauvegardes.


# Compétences mobilisées

* Data Engineering
* ETL / ELT
* MongoDB
* AWS
* Docker
* Python
* Monitoring & supervision
* Qualité des données


# Conclusion

Ce projet m’a permis de mettre en œuvre une chaîne complète de traitement de données, depuis l’ingestion jusqu’au déploiement cloud, en appliquant des pratiques proches d’un environnement de production Data Engineering.

Ce projet m’a permis de concevoir une chaîne complète de Data Engineering allant de l’ingestion de données météo jusqu’au déploiement cloud sur AWS.

J’ai pu mettre en pratique :

* l’ingestion de données multi-sources ;
* la transformation et standardisation de données ;
* la qualité des données ;
* MongoDB et la réplication ;
* Docker ;
* les services cloud AWS ;
* le monitoring et les sauvegardes.

Le pipeline obtenu est fiable, reproductible, industrialisable et répond aux besoins des équipes Data Science de GreenAndCoop.

## 🔗 Lien vers le projet :

https://github.com/ZackKa/Projet_8_data