# 📊 Projet 2 — Analyse exploratoire de données éducatives (EdTech)

## 📌 Contexte

Dans le cadre d’une startup EdTech fictive (Academy), une analyse exploratoire a été réalisée afin de soutenir une stratégie d’expansion internationale.

L’objectif métier était d’évaluer si les données éducatives de la Banque mondiale permettent d’identifier des pays à fort potentiel pour des services de formation en ligne.

---

## 🎯 Objectifs du projet

- Explorer et comprendre plusieurs jeux de données hétérogènes
- Évaluer la qualité et la complétude des données
- Nettoyer et fiabiliser les datasets
- Identifier et sélectionner des indicateurs pertinents
- Réduire le périmètre des données pour analyse métier
- Proposer une première approche de sélection de pays cibles

---

## 🛠️ Technologies utilisées

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 🔎 Démarche analytique

### 1. Exploration des données
- Chargement des différents fichiers de la Banque mondiale
- Analyse de la structure des datasets (shape, info, head)
- Identification des types de variables
- Analyse des valeurs manquantes et des doublons

---

### 2. Nettoyage et fiabilisation des données
- Suppression des doublons
- Analyse des valeurs manquantes par colonne
- Suppression des colonnes non exploitables
- Identification et suppression des “faux pays” (agrégats régionaux et globaux)
- Fiabilisation des relations entre datasets via filtrage et jointures

---

### 3. Réduction du périmètre des données
- Analyse des catégories métier des indicateurs
- Sélection des indicateurs pertinents pour le domaine de l’éducation
- Suppression des indicateurs hors périmètre
- Analyse de la cohérence temporelle des données (années futures)

---

### 4. Analyse de la complétude des données
- Calcul du taux de remplissage par année
- Calcul du taux de remplissage par indicateur
- Identification des indicateurs les plus riches en données
- Construction d’un ranking de qualité des variables

---

### 5. Transformation et structuration
- Passage du format large au format long (melt)
- Filtrage des années pertinentes
- Agrégation des données par pays et indicateur
- Construction d’un dataset analytique exploitable

---

### 6. Analyse statistique et corrélations
- Calcul des matrices de corrélation (Pearson et Spearman)
- Visualisation via heatmaps
- Identification et suppression des variables redondantes
- Analyse de la distribution des indicateurs

---

### 7. Sélection des indicateurs et pays
- Sélection d’environ 15 indicateurs pertinents
- Agrégation des données par pays
- Mise en place d’une logique de comparaison multi-indicateurs
- Première approche de scoring des pays cibles

---

## 📈 Résultats

- Mise en évidence de fortes disparités de qualité des données
- Identification des indicateurs les plus exploitables pour l’analyse métier
- Réduction significative du périmètre d’étude
- Construction d’un dataset final exploitable pour analyse stratégique
- Premiers éléments d’aide à la décision pour une expansion internationale

---

## 🧠 Compétences développées

- Data cleaning avancé sur datasets multi-sources
- Analyse exploratoire de données (EDA)
- Gestion de la qualité des données
- Feature selection (réduction de dimension métier)
- Analyse statistique et corrélations
- Structuration d’un raisonnement data orienté business

---

## 🔗 Lien vers le projet :

https://github.com/ZackKa/Projet_2_data