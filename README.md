![R](https://img.shields.io/badge/R-276DC3?logo=r&logoColor=white&style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Random%20Forest%20%7C%20GLM-brightgreen?style=for-the-badge)
![Telecom Churn](https://img.shields.io/badge/Telecom%20Churn-Modeling-blueviolet?style=for-the-badge)

# 1. Projet : churn-score-modeling-telecom
Projet de modélisation du churn client en télécommunications : stratification des données, encodage des variables catégorielles et comparaison GLM vs Random Forest pour construire un score prédictif robuste et interprétable.

# 2. Prédiction du Churn Télécom et Prétraitement des Données

## Aperçu du projet
Ce projet présente une chaîne complète de prétraitement des données et de prédiction du churn dans le secteur des télécommunications.  
L’objectif est de construire un score de churn robuste et interprétable afin d’identifier les clients à risque et d’améliorer les stratégies de rétention.

---

# 3. Fonctionnalités principales

## 3.1 Prétraitement des données
- Conversion et traitement des variables de dates  
- Gestion des valeurs manquantes (imputation statistique et stratifiée)  
- Nettoyage et transformation des données  
- Création de variables métier :  
  - Âge du client  
  - Ancienneté  
  - Durée d’engagement restante  
  - Historique de réengagement  

## 3.2 Stratification des clients
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

## 3.3 Méthodes d’encodage comparées
- Sans encodage (baseline)  
- One-hot encoding  
- Encodage par fréquence  
- Encodage basé sur la cible (target encoding)  

## 3.4 Modèles utilisés
- GLM (Régression logistique) — modèle interprétable  
- Random Forest — modèle performant pour relations non linéaires  

## 3.5 Métriques d’évaluation
- ROC-AUC par strate  
- Score de propension  
- Comparaison des méthodes d’encodage  
- Interprétabilité via valeurs de Shapley  

---

# 4. Résultats clés

## 4.1 Synthèse des performances
- La stratification améliore la performance de prédiction  
- La durée d’engagement restante est un prédicteur majeur du churn  
- Random Forest surpasse GLM pour les relations complexes  
- Les encodages cible et fréquence offrent un bon compromis performance/dimension  

---

# 5. Technologies utilisées

## 5.1 Langage
- R  
- R Markdown  

## 5.2 Bibliothèques principales
- dplyr, tidyr, caret  
- glmnet, randomForest  
- pROC, cluster, mclust  
- DALEX, ggplot2  

---

# 6. Structure du projet


```
telecom-churn-prediction
│
├── data
│   ├── raw -- confidentiel
│   └── processed
│
├── src
│   └── Pretraitement_donnees_telecom.Rmd
│
├── reports
│   └── final_report.pdf
│
├── requirements.txt
├── README.md
└── .gitignore
```


## 6.1 Description des dossiers
- **data/** : contient les données sources utilisées pour l’analyse.  
- **scripts/** : regroupe les scripts R Markdown pour le prétraitement, la stratification et la modélisation.  
- **outputs/** : stocke les résultats générés (scores, graphiques, tableaux).  
- **docs/** : documentation du projet (mémoire, rapports, présentations).  

---

# 7. Auteur

**Said Ouzzine**  
Data Scientist | Machine Learning | Risk Modeling  

Contact :  
- LinkedIn : https://www.linkedin.com/in/said-ouzzine/  
- Email : sadouzzine@email.com
 

