# churn-score-modeling-telecom
Projet de modélisation du churn client en télécommunications : stratification des données, encodage des variables catégorielles et comparaison GLM vs Random Forest pour construire un score prédictif robuste et interprétable.
# Prédiction du Churn Télécom et Prétraitement des Données

## Aperçu du projet
Ce projet présente une **chaîne complète de prétraitement des données et de prédiction du churn** dans le secteur des télécommunications.  
L’objectif est de construire un score de churn robuste et interprétable afin d’identifier les clients à risque et d’améliorer les stratégies de rétention.

---

## Fonctionnalités principales

### Prétraitement des données
- Conversion et traitement des variables de dates
- Gestion des valeurs manquantes (imputation statistique et stratifiée)
- Nettoyage et transformation des données
- Création de variables métier :
  - Âge du client
  - Ancienneté
  - Durée d’engagement restante
  - Historique de réengagement

### Stratification des clients
- Clustering K-means sur la durée d’engagement
- Validation des clusters :
  - Score de silhouette
  - Indice de Dunn
  - ANOVA
  - BIC (modèles de mélange gaussien)
- Définition de strates exploitables :
  - Court terme
  - Moyen terme
  - Long terme

### Méthodes d’encodage comparées
- Sans encodage (baseline)
- One-hot encoding
- Encodage par fréquence
- Encodage basé sur la cible (target encoding)

### Modèles utilisés
- **GLM (Régression logistique)** — modèle interprétable
- **Random Forest** — modèle performant pour relations non linéaires

### Métriques d’évaluation
- ROC-AUC par strate
- Score de propension
- Comparaison des méthodes d’encodage
- Interprétabilité via valeurs de Shapley

---

## Résultats clés

- La stratification améliore la performance de prédiction
- La durée d’engagement restante est un prédicteur majeur du churn
- Random Forest surpasse GLM pour les relations complexes
- Les encodages cible et fréquence offrent un bon compromis performance/dimension  

---

## Technologies utilisées

### Langage
- R
- R Markdown

### Bibliothèques principales
- `dplyr`, `tidyr`, `caret`
- `glmnet`, `randomForest`
- `pROC`, `cluster`, `mclust`
- `DALEX`, `ggplot2`

---

## Structure du projet

telecom-churn-prediction/
│
├── data/
│   ├── raw/                      # Données brutes (non modifiées)
│   └── processed/                # Données nettoyées et transformées
│
├── notebooks/
│   └── 01_preprocessing_modeling.Rmd   # Notebook principal reproductible
│
├── src/                          # Scripts d’analyse et de modélisation
│   ├── Pretraitement_donnees_telecom.Rmd
│
├── models/                       # Modèles sauvegardés
│   └── rf_model.rds
│
├── reports/
│   └── final_report.pdf          # Rapport / mémoire
│
├── results/
│   ├── auc_scores.csv
│   ├── propensity_scores.csv
│   └── model_comparison.csv
│
├── requirements.txt              # Dépendances (packages R utilisés)
├── README.md                     # Présentation du projet
└── .gitignore

### Description des dossiers

- **data/** : contient les données sources utilisées pour l’analyse.  
- **scripts/** : regroupe les scripts R Markdown pour le prétraitement, la stratification et la modélisation.  
- **outputs/** : stocke les résultats générés (scores, graphiques, tableaux).  
- **docs/** : documentation du projet (mémoire, rapports, présentations).

## 👤 Auteur

**Said Ouzzine**  
Data Scientist | Machine Learning | Risk Modeling  

Contact :  
- LinkedIn : https://www.linkedin.com/in/said-ouzzine/  
- Email : sadouzzine@email.com


