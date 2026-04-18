# 📊 Projet Google Trends — Analyse de mots-clés IA / Tech

## 🧠 Description

Ce projet consiste à analyser l’évolution de la popularité de mots-clés liés à l’intelligence artificielle et à la technologie à partir des données Google Trends en France entre 2020 et 2025.

L’objectif est de construire une base de données propre, puis d’explorer les tendances, les corrélations et les comportements des mots-clés à travers des analyses statistiques et du clustering.

---

## 🎯 Objectifs

- Collecter des données Google Trends
- Nettoyer et structurer les données
- Réaliser des statistiques descriptives
- Analyser les corrélations entre mots-clés
- Appliquer un clustering (KMeans)
- Produire des visualisations

---

## 🗂️ Structure du projet
projet_google_trends/
                         project_root
                              │
        ┌───────────────┬─────┼─────┬───────────────┬───────────────┐
        │               │     │     │               │               │
      data           figures notebook           docs            src
        │                     │
   ┌────┴────┐               └── projet_google_trends.ipynb
   │         │
  raw    processed

                              │
                          README.md


---

## 🛠️ Technologies utilisées

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pytrends
- Jupyter Notebook

---

## ⚙️ Méthodologie

### 1. Collecte des données
Les données ont été récupérées via l’API Google Trends (`pytrends`) pour plusieurs mots-clés liés à l’IA et à la tech.

---

### 2. Nettoyage
- Conversion des dates
- Suppression des doublons
- Gestion des valeurs manquantes
- Uniformisation des mots-clés

---

### 3. Structuration
Deux formats ont été créés :

- **Format long** : une ligne par date et mot-clé  
- **Format large** : une ligne par date, une colonne par mot-clé  

---

### 4. Analyse descriptive
Calcul des indicateurs :
- moyenne
- médiane
- minimum / maximum
- écart-type
- amplitude
- variation dans le temps

---

### 5. Corrélation
Création d’une matrice de corrélation pour identifier les relations entre mots-clés.

---

### 6. Clustering
- Normalisation des données
- Application de KMeans
- Regroupement des mots-clés selon leurs tendances

---

## 📁 Données générées

- `trends_brut_long.csv`
- `trends_clean_long.csv`
- `trends_clean_wide.csv`
- `stats_par_motcle.csv`
- `matrice_correlation.csv`
- `X_scaled_clustering.csv`
- `elbow_data.csv`
- `clusters_motscles.csv`

---

## 📊 Visualisations

- Top 10 des mots-clés
- Courbes d’évolution
- Méthode du coude (KMeans)
- Graphiques exploratoires

---

## ⚠️ Limites

Les données Google Trends sont normalisées (0–100).  
Cela signifie que les valeurs ne représentent pas des volumes absolus, ce qui limite certaines comparaisons entre mots-clés.

---

## 🚀 Lancer le projet

### Installer les dépendances

```bash
pip install pandas numpy matplotlib seaborn scikit-learn pytrends jupyter

Ouvrir le notebook
jupyter notebook

Puis ouvrir :

notebook/projet_google_trends.ipynb

📌 Conclusion

Ce projet permet d’identifier :

les mots-clés les plus populaires
les tendances émergentes
les comportements similaires entre sujets
