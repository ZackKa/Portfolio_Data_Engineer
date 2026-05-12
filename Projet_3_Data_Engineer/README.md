# 🏠 Projet 3 — Data Engineering & Analyse immobilière (Laplace Immo)

## 📌 Contexte métier

Dans le cadre d’un projet pour Laplace Immo, réseau national d’agences immobilières, une mission de Data Engineering a été réalisée afin de structurer et exploiter des données immobilières françaises.

L’objectif était de construire un **Proof of Concept (PoC)** permettant de transformer des données brutes en un système analytique exploitable pour le suivi du marché immobilier.

---

## 🎯 Objectifs du projet

- Concevoir une base de données relationnelle normalisée (3NF)
- Structurer des données immobilières multi-sources
- Garantir la qualité et l’intégrité des données
- Construire un pipeline de préparation et de chargement des données
- Exploiter la base via des requêtes SQL analytiques
- Fournir des insights métier sur le marché immobilier français

---

## 🛠️ Stack technique

- SQLite (base de données relationnelle)
- SQL (modélisation + analyse)
- Excel / CSV (préparation des données)
- SQL Power Architect (modélisation)
- Concepts de Data Modeling (3NF)

---

## 📦 Livrables

- Dictionnaire des données (Excel)
- Schéma relationnel normalisé (3NF)
- Base de données SQLite opérationnelle
- Requêtes SQL analytiques

---

## 🧱 Architecture & modélisation des données

### 🔹 Modélisation relationnelle (3NF)

Le modèle a été conçu pour garantir :
- suppression des redondances
- intégrité des données
- normalisation complète

### 🔗 Structure de la base :

- Region
  - Departement
    - Commune
      - Bien
        - Vente

---

### 🔑 Concepts clés utilisés

- Clés primaires et étrangères
- Intégrité référentielle
- Normalisation (1NF → 3NF)
- Décomposition logique des entités métier

---

## 🔄 Pipeline de préparation des données

- Analyse des fichiers sources (Valeurs Foncières, Référentiel géographique, Données communes)
- Nettoyage et transformation des datasets
- Création de fichiers conformes au schéma relationnel
- Gestion des clés (auto-increment, concaténation, mapping géographique)
- Vérification de l’unicité des clés primaires
- Contrôle de cohérence entre fichiers et base de données

---

## 🗄️ Construction de la base de données

- Création des tables SQL
- Chargement des données nettoyées
- Vérification de l’intégrité référentielle
- Validation de la conformité avec le schéma relationnel

---

## 📊 Analyse SQL & exploitation des données

### 🔹 Requêtes réalisées

- Analyse du volume de transactions immobilières
- Répartition des ventes par région et département
- Calcul des prix moyens au m²
- Analyse de la typologie des biens (pièces, surface)
- Étude des biens haut de gamme
- Analyse des dynamiques de marché

---

### 🔹 Exemples d’insights

- Forte concentration des ventes en Île-de-France
- Prix au m² les plus élevés : Paris et Hauts-de-Seine
- Les biens 2–3 pièces représentent la majorité du marché
- Croissance modérée du marché immobilier (+3,68%)

---

## 📈 Résultats & impact métier

- Mise en place d’une base de données structurée et exploitable
- Fiabilisation des données immobilières multi-sources
- Identification des zones à forte valeur immobilière
- Analyse des dynamiques de marché pour orienter les agences
- Support à la prise de décision stratégique pour Laplace Immo

## 📊 Résultats clés

- Île-de-France : région avec le plus grand volume de transactions
- Prix moyen le plus élevé : Paris (~12 000 €/m²)
- Marché dominé par les biens 2–3 pièces (>60%)
- Croissance globale du marché : +3,68 %

---

## 🧠 Compétences développées

### Data Engineering
- Modélisation de données relationnelles
- Conception de bases de données (3NF)
- Construction de pipeline de données
- Data cleaning et transformation

### SQL & Data Analysis
- Requêtes complexes (JOIN, GROUP BY, CTE)
- Analyse statistique de données immobilières
- Extraction d’insights métier

### Architecture & qualité des données
- Intégrité référentielle
- Normalisation avancée
- Gestion des clés primaires/étrangères

---

## 🚀 Valeur ajoutée du projet

Ce projet démontre une capacité complète de Data Engineering :

👉 passer de données brutes à une base analytique structurée  
👉 concevoir une architecture de données robuste  
👉 exploiter les données via SQL pour répondre à des besoins métiers réels  
👉 produire des insights exploitables pour la prise de décision

---

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_3_data