# Projet 4 — Audit OLAP & Data Quality (SuperSmartMarket)
## 📊 Récapitulatif du projet

Ce projet s’inscrit dans un parcours Data Engineer et simule une mission en environnement décisionnel (BI / OLAP).

L’objectif était d’identifier et corriger une incohérence critique dans le calcul du chiffre d’affaires d’une entreprise de retail, liée à une mauvaise gestion de l’historisation des données dans un système OLAP utilisé avec Power BI.

Le projet couvre l’ensemble du cycle :

- compréhension d’une architecture BI existante
- modélisation d’un modèle en étoile
- audit de données et investigation SQL
- analyse de logs transactionnels
- correction des données avec une approche Data Engineering (SCD Type 2)

## 📌 Description du projet

SuperSmartMarket utilise une architecture décisionnelle basée sur un entrepôt de données OLAP alimenté par des flux transactionnels et exploité via Power BI.

Une anomalie critique a été détectée :
**le chiffre d’affaires historique variait dans le temps sans nouvelles transactions.**

L’analyse a permis de :

- reconstruire un modèle de données en local (Proof of Concept)
- recalculer les indicateurs directement depuis les données sources
- analyser les logs pour identifier les causes de l’incohérence
- détecter une absence d’historisation des prix produits
- comprendre que les mises à jour écrasaient l’historique des ventes

Une solution de correction a été proposée et implémentée via :

- historisation des prix (SCD Type 2)
- création d’une table de suivi des versions
- mise en place de triggers SQL
- création de vues pour garantir la stabilité des indicateurs

## 🛠️ Outils et technologies utilisés

- SQLite (prototype de base de données)
- SQL (requêtes analytiques et de diagnostic)
- Modélisation en étoile (Star Schema)
- Data Warehouse / OLAP concepts
- Power BI (analyse des incohérences)
- SCD Type 2 (historisation des dimensions)
- Triggers SQL
- Analyse de logs transactionnels

## 🏗️ Solution implémentée

- SCD Type 2 sur les prix produits
- Trigger d’historisation automatique
- Vue stable pour reporting BI

## 📈 Résultats obtenus
- Validation du chiffre d’affaires réel : 284 243,88 €
- 207 489 logs analysés
- 575 UPDATE critiques sur les prix produits
- Identification d’une absence d’historisation des dimensions
- Identification de la cause racine :
    **mises à jour non historisées des prix produits**
- Analyse de plus de 200 000 logs transactionnels
- Mise en évidence de 575 modifications critiques sur les prix
- Mise en place d’une solution garantissant :
    - la stabilité des indicateurs historiques
    - la traçabilité des modifications
    - la fiabilité du reporting BI

**Résultat final : un système analytique cohérent, reproductible et fiable dans le temps.**

## 💡 Impact métier

- Suppression des incohérences dans Power BI
- Fiabilisation du reporting financier
- Garantie de stabilité des KPI dans le temps

## 🧠 Compétences démontrées

- Data Engineering & Data Modeling
- Analyse et audit de bases OLAP
- SQL avancé (jointures, agrégations, CTE, vues)
- Investigation de données (data debugging)
- Analyse de logs et détection d’anomalies
- Implémentation de SCD Type 2
- Conception de triggers SQL
- Compréhension des flux BI (ETL → OLAP → reporting)
- Approche orientée qualité et fiabilité des données

## 🚀 Valeur ajoutée du projet

Ce projet met en évidence une compétence clé en Data Engineering :

**la capacité à identifier et corriger des problèmes de fiabilité dans des systèmes décisionnels réels.**

Il démontre que :

- un problème de reporting peut venir de la structuration des données
- la qualité des dimensions est critique pour les indicateurs métier
- l’historisation est indispensable pour garantir la cohérence des analyses dans le temps

Ce projet illustre également une approche professionnelle complète :
de l’audit des données jusqu’à la mise en place d’un correctif robuste de type industriel.

🔗 Lien vers le projet

https://github.com/ZackKa/Projet_4_data