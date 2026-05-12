# 🏃‍♂️ POC Data – Avantages sportifs en entreprise
## 📌 Contexte

Dans le cadre d’une mission chez Sport Data Solution, ce projet vise à concevoir un pipeline data complet pour encourager la pratique sportive en entreprise.

L’objectif est de collecter et analyser les activités sportives des employés afin de déclencher automatiquement des avantages (prime, jours de bien-être).

## 🎯 Objectifs
- Collecter et centraliser les données RH et sportives
- Mettre en place un pipeline batch + streaming
- Calculer automatiquement les avantages salariés
- Assurer la qualité, la traçabilité et le monitoring
- Alimenter un dashboard décisionnel

## ⚙️ Stack technique
- Python (pandas, simulation, traitement)
- Kestra (orchestration)
- PostgreSQL (modélisation en couches RAW / STAGING / MART)
- Redpanda (streaming temps réel)
- Docker & Docker Compose
- Power BI (visualisation)
- Slack API (notifications)

## 🏗️ Architecture du pipeline
```text
Sources (RH + activités sportives)
        ↓
Ingestion batch (Kestra)
        ↓
Streaming activités (Redpanda / Kafka)
        ↓
Stockage PostgreSQL (RAW)
        ↓
Transformation & enrichissement (STAGING)
        ↓
Tests qualité (Pytest)
        ↓
Tables métiers (MART)
        ↓
Dashboard Power BI + Notifications Slack
```

## 🚀 Fonctionnalités clés
- 🔄 Pipeline end-to-end automatisé
- ⚡ Streaming temps réel des activités sportives
- 🧪 Tests qualité intégrés à chaque étape
- 📊 Calcul des KPI (primes, éligibilité, activité)
- 💬 Notifications automatiques sur Slack
- 📈 Dashboard Power BI pour pilotage métier

## 📊 Résultats
- Pipeline robuste et rejouable
- Données fiables grâce aux contrôles qualité
- Calcul automatisé des avantages salariés
- Vision claire de l’impact financier

Après exécution complète du pipeline sur 12 mois de données simulées :

- 👨‍💼 Employés analysés : 161
- 🏃 Activités sportives traitées : 1617 
- 💰 Montant total des primes générées : ~172k €
- 🧑‍🤝‍🧑 Employés éligibles prime : ~42 %
- 🌿 Employés éligibles prime de bien-être : ~33 %
- ⚡ Temps moyen d’exécution du pipeline : 20 min (pour une première exécution, incluant le calcul des distances et l’envoi de messages Slack)

#### 💡 Impact métier
- Réduction du temps de traitement manuel des données RH/sportives
- Automatisation complète du calcul des avantages
- Vision claire du coût financier des politiques de bien-être

## 💡 Apports du projet

Ce projet démontre :

- La maîtrise d’une architecture data moderne (batch + streaming)
- La mise en place d’un data pipeline industrialisé
- L’intégration de monitoring, alerting et qualité des données
- Une approche orientée cas d’usage métier concret

## 🔮 Perspectives
- Intégration avec des APIs sportives réelles (Strava, Garmin)
- Déploiement cloud (AWS / GCP)
- Personnalisation des règles métier
- Application web pour les collaborateurs

## ✅ Conclusion

Ce POC valide la faisabilité d’un système data complet permettant de valoriser la pratique sportive en entreprise, tout en fournissant des indicateurs fiables pour la prise de décision.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_12_data