# 🚀 Puls-Events – Design & Pilotage d’un MVP IA (RAG Chatbot)
## 📌 Contexte

Dans le cadre de mon alternance chez Puls-Events, j’ai participé à la transformation d’un Proof of Concept (POC) en un MVP industrialisable.

Le POC validait déjà un chatbot basé sur une architecture RAG (Retrieval-Augmented Generation) capable de recommander des événements culturels à partir de données OpenAgenda.

### 👉 L’objectif de ce projet :
concevoir une solution scalable, robuste et prête pour la production, en intégrant des enjeux réels de Data Engineering, Cloud et FinOps.

## 🎯 Objectifs du projet
- Transformer un POC technique en MVP industrialisable
- Concevoir une architecture cloud scalable
- Structurer un produit IA complet (technique + métier)
- Définir une roadmap de développement
- Estimer les coûts (build & run)
- Intégrer une approche FinOps dès la conception

## 🛠️ Stack technique

- Frontend : Streamlit
- Backend API : FastAPI
- IA / RAG : LangChain
- Base vectorielle : Qdrant
- Mémoire conversationnelle : Redis
- Pipeline data : Airflow
- Stockage : AWS S3
- Monitoring : CloudWatch, Sentry
- Cloud : AWS

## ⚠️ Limites du POC initial

Le POC présentait plusieurs freins à une mise en production :

- ❌ Architecture locale non scalable
- ❌ Absence d’API robuste
- ❌ Pas de gestion multi-utilisateurs
- ❌ Aucun monitoring
- ❌ Coûts non maîtrisés

👉 Il était donc nécessaire de repenser entièrement l’architecture sans repartir de zéro.

## 🏗️ Architecture cible (MVP)
### 🔹 Stack technique
- Frontend : Streamlit
- Backend API : FastAPI
- Orchestration IA : LangChain (RAG)
- Base vectorielle : Qdrant
- Mémoire conversationnelle : Redis
- Pipeline data : Airflow
- Stockage : S3
- Monitoring : CloudWatch + Sentry
- Cloud : AWS
### 🔹 Fonctionnement global
- L’utilisateur envoie une requête
- Transformation en embedding
- Recherche dans la base vectorielle
- Injection du contexte pertinent
- Génération de la réponse via LLM

👉 Résultat : un chatbot capable de fournir des réponses contextualisées et personnalisées.

## ☁️ Choix du Cloud

Une analyse comparative a été menée entre :

- AWS
- GCP
- Azure

✅ AWS a été retenu pour :

- sa maturité en production
- son écosystème riche
- sa scalabilité
- sa compatibilité avec les outils open-source

## 🧠 Fonctionnalités du MVP

✅ Must-have
- API backend robuste
- Système RAG scalable
- Base vectorielle performante
- Mémoire conversationnelle
- Géolocalisation des réponses
- Pipeline data automatisé
- Monitoring & observabilité
- Déploiement cloud

⭐ Nice-to-have
- Authentification utilisateur
- Optimisation des performances
- Personnalisation avancée

## 📋 Gestion de projet
🧩 Méthodologie
- Approche Agile
- Priorisation des fonctionnalités
- Développement itératif

## 📅 Planification
- Définition des jalons
- Organisation en phases projet
- Structuration des livrables

## 💰 Estimation des coûts
### 🔹 Build (développement)
💸 22k – 26k €
Ressources principales :
- Data Engineer
- Développeur Fullstack
### 🔹 OPEX (exploitation)
Environnement	Coût mensuel
MVP	50 – 100 €
Production	300 – 800 €
### 🔹 Approche FinOps
- Optimisation des appels LLM
- Gestion du stockage (S3 lifecycle)
- Réduction des logs
- Extinction des ressources inutilisées

## 🚀 Stratégie de déploiement
### 🔹 Phase MVP
Déploiement sur instance EC2 unique
Services centralisés :
- API
- RAG
- Qdrant
- Redis
- Airflow

🎯 Objectif : livrer rapidement à coût réduit

### 🔹 Évolution future
- Architecture microservices
- Conteneurisation (Docker / Kubernetes)
- Scalabilité horizontale
- Séparation des services

## ⚠️ Défis rencontrés
### 🔸 Techniques
- Scalabilité du RAG
- Latence des réponses
- Gestion de la mémoire conversationnelle
### 🔸 Data
- Qualité des données OpenAgenda
- Mise à jour des embeddings
### 🔸 Coûts
- Appels aux modèles LLM
- Stockage et logs

## ✅ Solutions apportées
- Architecture modulaire et évolutive
- Limitation intelligente du contexte
- Monitoring des performances
- Intégration d’une logique FinOps

## 📈 Résultats

Ce projet m’a permis de :

- Concevoir une architecture IA prête pour la production
- Structurer un projet Data/IA de bout en bout
- Intégrer des enjeux réels :
    - performance
    - scalabilité
    - coûts
    - monitoring
- Passer d’une logique technique (POC) à une logique produit (MVP)

## 🔮 Perspectives
- Passage à une architecture microservices
- Amélioration de la personnalisation
- Ajout de nouvelles sources de données
- Optimisation des performances du RAG

##🧠 Conclusion

Ce projet démontre ma capacité à :

- Transformer un POC en solution industrialisable
- Concevoir une architecture cloud moderne
- Piloter un projet Data/IA avec une vision technique + produit + business

👉 Il constitue une étape clé vers la mise en production d’un système IA scalable dans un contexte réel.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_13_data