# POC RAG – Chatbot de recommandation d’événements
## 📌 Contexte

Dans le cadre d’une mission pour Puls-Events, ce projet consiste à développer un **Proof of Concept (POC)** d’un chatbot intelligent capable de recommander des événements culturels personnalisés.

L’objectif est de tester une architecture **RAG (Retrieval-Augmented Generation)** combinant recherche sémantique et génération de texte.

## 🎯 Objectifs
- Exploiter des données d’événements (OpenAgenda)
- Construire une base vectorielle performante
- Développer un chatbot intelligent basé sur le contexte
- Fournir des réponses pertinentes et explicables

## ⚙️ Stack technique
- Python
- LangChain
- FAISS
- Mistral
- API OpenAgenda

## 🏗️ Architecture du pipeline
```text
OpenAgenda API
   ↓
Nettoyage & structuration
   ↓
Chunking des textes
   ↓
Génération d’embeddings (Mistral)
   ↓
Indexation vectorielle (FAISS)
   ↓
Retriever (LangChain)
   ↓
LLM → Génération de réponse
```

## 🚀 Fonctionnalités clés
- 🔎 Recherche sémantique d’événements
- 🤖 Chatbot interactif (questions en langage naturel)
- 📍 Filtrage géographique (Paris)
- 📅 Données récentes (< 1 an)
- 📚 Réponses enrichies avec sources

## 📊 Résultats
- Base vectorielle performante et exploitable
- Recommandations pertinentes basées sur le contexte
- Pipeline entièrement reproductible
- Système extensible (autres villes, datasets, modèles)
- Réponses contextualisées avec réduction des hallucinations du modèle
- ~X événements récupérés depuis OpenAgenda (change en fonction des événements récupérés)
- ~X chunks générés (change en fonction des événements récupérés)
- Temps moyen de réponse du chatbot : ~3s
- Recommandations cohérentes sur requêtes tests

## 💡 Apports du projet

Ce projet démontre :

- La maîtrise des architectures RAG modernes
- L’intégration de LLM + base vectorielle
- La construction d’un pipeline NLP complet
- Une approche orientée cas d’usage métier (recommandation)

## 🔮 Perspectives
- Ajout d’historique conversationnel
- Amélioration du ranking des résultats
- Déploiement en API ou application web
- Extension multi-villes / multi-langues

## ✅ Conclusion

Ce POC valide la faisabilité d’un système de recommandation intelligent basé sur le NLP et les bases vectorielles, ouvrant la voie à une intégration produit à plus grande échelle.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_11_data