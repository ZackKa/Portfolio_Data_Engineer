# 🚀 POC – Pipeline temps réel avec Redpanda & PySpark
## 📌 Contexte

Dans le cadre de la modernisation du SI de InduTechData, ce projet consiste à concevoir un **pipeline de données en temps réel** pour traiter des tickets clients issus de flux IoT et applicatifs.

L’objectif est de démontrer la capacité à manipuler des architectures modernes orientées **streaming data**, en s’appuyant sur un écosystème cloud-compatible.

### Le projet est structuré en deux volets :

Partie 1 : Conception d’une architecture hybride cloud / on-premise
Partie 2 : POC d’un pipeline temps réel de gestion de tickets clients

# 🏗️ 1. Architecture hybride (AWS + SI on-premise)
## 🎯 Objectif

Concevoir une architecture cloud hybride capable de :

- traiter des flux IoT en temps réel
- centraliser les données analytiques
- garantir la compatibilité avec le SI existant
- assurer sécurité, scalabilité et maîtrise des coûts

## ☁️ Composants cloud retenus
- Stockage objet : Amazon S3
    - stockage des logs et données IoT
    - haute scalabilité et faible coût
    - intégration directe avec Redpanda et AWS analytics
- Entrepôt de données : Amazon Redshift
    - analyse SQL avancée
    - centralisation des données métiers
- Streaming : Redpanda
    - compatible Kafka
    - ingestion temps réel des flux IoT et applicatifs
    - faible latence et forte performance
- Gestion des identités : AWS AD Connector
    - extension de l’Active Directory on-premise vers le cloud
    - authentification unifiée
- Connectivité : VPN Site-to-Site (IPsec)
    - sécurisation des échanges entre SI et cloud

## 🔁 Flux de données
- IoT / applications → Redpanda (streaming temps réel)
- SQL Server → Redshift (batch via AWS DMS / CDC)
- Logs et fichiers → S3 (stockage data lake)
- Authentification → AD on-premise via AWS AD Connector

## 🔐 Sécurité & conformité
- Chiffrement TLS sur les flux Redpanda
- VPN IPsec pour les échanges hybrides
- Chiffrement au repos (S3 / Redshift)
- Gestion centralisée des identités via AD existant

## 📈 Scalabilité & coûts
- Architecture horizontale avec Redpanda et S3
- Redshift scalable selon la charge analytique
- Surveillance via AWS CloudWatch et AWS Budgets
- Coût estimé : infrastructure cloud évolutive (~1000$/mois selon charge)

## ⚖️ Synthèse

Avantages :

modernisation du SI sans rupture
forte scalabilité (IoT, logs)
intégration fluide on-premise + cloud

Limites :

dépendance réseau hybride
complexité opérationnelle Redpanda self-hosted

# ⚡ 2. POC – Pipeline temps réel de tickets clients

## 🎯 Objectifs
- Simuler la génération de tickets clients en temps réel
- Mettre en place un pipeline de streaming avec Redpanda (Kafka-compatible)
- Traiter et analyser les données avec PySpark
- Produire des indicateurs exploitables automatiquement
- Conteneuriser l’ensemble avec Docker

## 🏗️ Architecture du projet

```mermaid
flowchart LR
    A[Producer Python] --> B[Redpanda - Topic client_tickets]
    B --> C[PySpark Streaming]
    C --> D[Transformation & Enrichissement]
    D --> E[Agrégation]
    E --> F[Export JSON]
```

## ⚙️ Stack technique
- Streaming : Redpanda (alternative performante à Kafka)
- Traitement : PySpark (Structured Streaming)
- Langage : Python
- Conteneurisation : Docker & Docker Compose

## 🔍 Fonctionnalités clés
- Génération de données temps réel (tickets clients simulés)
- Ingestion via un broker Kafka-compatible
- Traitement distribué en streaming
- Enrichissement automatique des données (ex : assignation équipe support)
- Agrégation en continu (ex : nombre de tickets par type)
- Export automatisé des résultats

## 📊 Résultats

Exemple de sortie :
```text
{"type":"ACCOUNT","ticket_count":52}
{"type":"BILLING","ticket_count":50}
{"type":"GENERAL","ticket_count":53}
{"type":"TECHNICAL","ticket_count":45}
```
✔ 200 tickets traités
✔ pipeline temps réel fonctionnel
✔ traitement sans perte de données
✔ architecture reproductible via Docker

- Pipeline temps réel entièrement fonctionnel
- Traitement fiable sans perte de données
- Architecture reproductible et scalable
- Production d’indicateurs exploitables pour le support client

## 💡 Compétences démontrées
- Data Engineering temps réel (streaming)
- Manipulation de systèmes distribués (Kafka / Spark)
- Conception de pipelines ETL
- Conteneurisation et orchestration
- Structuration d’une architecture data moderne

## 🔗 Démonstration

👉 https://www.youtube.com/watch?v=6ZpCe8LNemo

## 📎 Conclusion

Ce projet illustre la mise en place d’un pipeline de données temps réel complet, depuis la génération jusqu’à l’analyse, en utilisant des technologies modernes adaptées aux environnements cloud hybrides.

## 🔗 Lien vers le projet :

https://github.com/ZackKa/Projet_9_data