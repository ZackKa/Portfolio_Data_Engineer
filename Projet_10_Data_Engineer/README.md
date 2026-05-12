# 🍷 Automatisation d’un pipeline data avec Kestra
## 📌 Contexte

Dans le cadre de l’industrialisation des traitements data de l’entreprise BottleNeck (marchand de vin), ce projet vise à automatiser un pipeline de transformation et d’analyse de données issues de plusieurs sources (ERP, CMS).

L’objectif est de rendre les analyses fiables, reproductibles et automatisées, afin de fournir des rapports mensuels aux équipes métier.

## 🎯 Objectifs
- Nettoyer et fiabiliser les données issues de plusieurs systèmes
- Réconcilier les données via un fichier de correspondance
- Calculer le chiffre d’affaires par produit et global
- Identifier automatiquement les vins premium (méthode statistique)
- Automatiser l’ensemble du pipeline avec orchestration
- Planifier l’exécution mensuelle

## 🏗️ Architecture du pipeline

```mermaid
flowchart LR
    A[Sources ERP / CMS / Liaison] --> B[Nettoyage des données]
    B --> C[Tests qualité]
    C --> D[Jointures]
    D --> E[Tests cohérence]
    E --> F[Calcul chiffre d’affaires]
    F --> G[Tests résultats]
    G --> H[Z-score - vins premium]
    H --> I[Exports Excel & CSV]
    I --> J[Planification mensuelle]
```

## ⚙️ Stack technique
- Orchestration : Kestra
- Traitement : Python & SQL (DuckDB)
- Analyse : Pandas (z-score)
- Conteneurisation : Docker
- Format de sortie : Excel & CSV

## 🔍 Fonctionnalités clés
- Pipeline automatisé de bout en bout (ETL + analyse)
- Intégration multi-sources (ERP, CMS, fichier de liaison)
- Tests de qualité des données à chaque étape
- Calcul automatisé du chiffre d’affaires
- Détection statistique des vins premium (z-score > 2)
- Génération de rapports prêts à l’usage métier
- Planification mensuelle via cron

## 🧪 Contrôles qualité des données

À chaque étape du pipeline, des tests automatiques sont intégrés afin de garantir la fiabilité des données :

### 🔍 Tests implémentés

- ✔ Absence de valeurs manquantes (NULL check)
- ✔ Suppression des doublons sur les clés primaires
- ✔ Vérification de la cohérence des jointures (ERP / CMS / liaison)
- ✔ Contrôle du chiffre d’affaires (validation des agrégations)
- ✔ Validation du calcul du z-score pour les vins premium

### 📌 Objectif des tests

Ces contrôles permettent de garantir :
- la qualité des données en entrée et sortie
- la reproductibilité du pipeline
- la fiabilité des résultats métiers

## 📊 Résultats
- Pipeline robuste avec contrôles qualité intégrés
- Données fiables et cohérentes après transformation
- Automatisation complète des rapports mensuels
- Réduction du travail manuel et des risques d’erreurs

Le pipeline automatisé permet de produire les résultats suivants après exécution complète :

- 💰 Chiffre d’affaires total : **70 568,60 €**
- 🍷 Nombre de vins premium détectés : **30**
- 🍷 Nombre de vins ordinaires : **684**
- 📦 Nombre total de lignes traitées après fusion : **714**

## 💡 Compétences démontrées
- Orchestration de workflows data (Kestra)
- Conception de pipelines ETL robustes
- Data quality & testing automatisé
- Manipulation SQL et Python pour la data
- Mise en production via conteneurs Docker

## 📎 Conclusion

Ce projet illustre la mise en place d’un pipeline data industrialisé, combinant automatisation, contrôle qualité et analyse statistique, au service des équipes métier.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_10_data