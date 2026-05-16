# 🏠 NosCités — Analyse et Architecture MongoDB des locations courte durée
## 📌 Contexte
Dans ce projet, j’interviens en tant que Data Engineer pour l’association fictive NosCités, qui analyse les impacts des plateformes de location courte durée sur le marché immobilier français.

Suite à une perte de données concernant les annonces parisiennes à l’été 2024, l’objectif était de :
- restaurer une sauvegarde MongoDB ;
- vérifier la cohérence des données ;
- produire des indicateurs métier sur l’effet “JO Paris 2024” ;
- connecter les données à un outil de Business Intelligence ;
- concevoir une architecture MongoDB distribuée et résiliente pour éviter de futurs incidents.

Le projet couvre donc à la fois :
- l’administration MongoDB ;
- l’analyse de données NoSQL ;
- la Business Intelligence ;
- l’architecture distribuée (Replica Sets & Sharding).

## 🎯 Objectifs du projet
### Partie 1 — Restauration et exploration MongoDB
- Importer les données dans MongoDB ;
- Comprendre la structure des documents ;
- Réaliser les premières requêtes de validation.

### Partie 2 — Analyse de données
- Produire des indicateurs métier via MongoDB ;
- Réaliser des analyses avancées avec Python / Polars ;
- Connecter MongoDB à Power BI.

### Partie 3 — Architecture distribuée
- Fusionner les données Paris + Lyon ;
- Mettre en place un Replica Set ;
- Déployer un cluster shardé multi-sites.

## 🛠 Stack Technique
### Base de données
- MongoDB
- Mongosh
- MongoDB Compass

### Analyse de données
- Python
- PyMongo
- Polars

### Business Intelligence
- Power BI
- MongoDB BI Connector
- ODBC Driver

### Architecture distribuée
- MongoDB Replica Sets
- MongoDB Sharding
- Cluster distribué on-premise

## 📂 Dataset
### Source
Export de plateformes de locations courte durée (type Airbnb).

### Volumétrie
- Paris : 95 885 annonces
- Paris + Lyon : 105 858 annonces

### Format
- CSV (>100 Mo)
- Données semi-structurées


### Exemple de document MongoDB
```json
{
  "id": "...",
  "host_id": "...",
  "room_type": "Entire home/apt",
  "price": 120,
  "amenities": ["Wifi", "Kitchen", "Heating"],
  "availability_365": 180,
  "has_availability": true
}
```

## 📥 Partie 1 — Restauration et compréhension des données
### Import des données
Import réalisé via :

- MongoDB Compass
- MongoDB CLI (mongoimport)

### Base MongoDB
```bash
Database: noscites
Collection: listings_paris
```

### Premières vérifications
Nombre total d’annonces
**95 885 annonces**

Logements avec disponibilité déclarée
**90 173 annonces**

### Pourquoi MongoDB / NoSQL ?
Le choix de MongoDB est particulièrement adapté car les données :

- sont semi-structurées ;
- proviennent de scraping web ;
- contiennent des champs imbriqués (`amenities`) ;
- évoluent régulièrement ;
- nécessitent une forte flexibilité de schéma.
Le modèle document-oriented évite également la multiplication de jointures SQL complexes.

## 📊 Partie 2 — Analyse des données
### 🔎 Requêtes MongoDB
#### Répartition des annonces par type de logement

| Type             | Nombre |
|------------------|--------|
| Entire home/apt  | 85 733 |
| Private room     | 8 975  |
| Hotel room       | 776    |
| Shared room      | 401    |

#### Nombre total d’hôtes distincts
**71 979 hôtes**

#### Locations réservables instantanément
**22 094 annonces≈ 23% du total**

#### Hôtes avec plus de 100 annonces
**24 hôtes**
Cet indicateur met en évidence une professionnalisation importante de certains acteurs.

#### Nombre de super hôtes
**10 027 super hôtes≈ 13.9% des hôtes**

### 📈 Analyses avancées avec Python & Polars
#### Taux moyen de réservation mensuel

| Type de logement | Taux moyen |
|------------------|------------|
| Private room     | ~70%       |
| Entire home/apt  | ~66–71%    |
| Shared room      | ~61%       |
| Hotel room       | ~53%       |

#### Médiane du nombre d’avis
La **médiane de tous logements** est de **3 avis**

La **médiane par catégorie d’hôte**

| Catégorie        | Médiane |
|------------------|---------|
| Super hosts      | 24      |
| Non Super hosts  | 2       |

Les super hosts génèrent donc significativement plus d’activité.

#### Densité de logements par quartier
Quartiers les plus denses :
- Buttes-Montmartre
- Popincourt
- Vaugirard
- Batignolles-Monceau
- Entrepôt

#### Quartiers avec le plus fort taux de réservation
- Ménilmontant
- Buttes-Chaumont
- Popincourt
- Panthéon
Ces zones semblent particulièrement impactées par le tourisme intensif.

### 📊 Business Intelligence — Power BI
#### Architecture BI
```text
MongoDB
   ↓
BI Connector / ODBC
   ↓
Power BI
```

#### Dashboard réalisé
Le dashboard permet de visualiser :
- la densité des logements ;
- les taux de réservation ;
- la répartition des types de logements ;
- les indicateurs agrégés métier.

### Approche retenue
Pour améliorer les performances côté BI :
- exposition de collections agrégées ;
- limitation des requêtes complexes côté Power BI ;
- optimisation des temps de chargement.

## 🏗 Partie 3 — Architecture distribuée MongoDB
### 🌍 Intégration multi-sites
Fusion des données :
- Paris
- Lyon

Ajout d’un champ :
```bash
{  "city": "Paris"}
```
ou
```bash
{  "city": "Lyon"}
```

### 🔁 Replica Sets
Architecture mise en place
```text
Primary
├── Secondary
├── Secondary
└── Arbiter
```

Objectifs
- Haute disponibilité ;
- Tolérance aux pannes ;
- Réplication automatique ;
- Continuité de service.

### ⚡ Sharding MongoDB
#### Cluster shardé
```text
Shard Paris
Shard Lyon
```

#### Clé de sharding
```text
{ city: 1 }
```

#### Bénéfices
- distribution horizontale des données ;
- optimisation des requêtes locales ;
- réduction de la latence ;
- meilleure scalabilité.

### 🏛 Architecture globale
```text
MongoDB Sharded Cluster
├── ReplicaSet Paris
├── ReplicaSet Lyon
├── Config Servers
└── Mongos Router
        ↓
    Power BI
```

### Résultats du projet


- ✅ Base MongoDB restaurée
- ✅ Données validées et analysées
- ✅ Dashboard Power BI connecté
- ✅ Replica Sets opérationnels
- ✅ Architecture shardée mise en place

### 🧠 Compétences démontrées
#### Data Engineering
- ingestion et restauration de données ;
- administration MongoDB ;
- modélisation NoSQL.

#### Analyse de données
- requêtes MongoDB ;
- pipelines d’agrégation ;
- analyses statistiques avec Polars.

#### Architecture distribuée
- Replica Sets ;
- Sharding ;
- haute disponibilité ;
- distribution des données.

#### Business Intelligence
- connexion MongoDB ↔ Power BI ;
- création de dashboards analytiques.

## 🔗 Lien vers le projet

https://github.com/ZackKa/Projet_7_data