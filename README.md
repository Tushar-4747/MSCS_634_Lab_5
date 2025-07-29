# Lab 5: Clustering Techniques Using DBSCAN and Hierarchical Clustering

## Course: MSCS 634  

**Student Name**: Tushar Jitendrakumar Limbachiya 

**Lab Assignment**: Lab 5  

---

##  Purpose

The objective of this lab is to explore unsupervised machine learning techniques—specifically **Hierarchical Clustering** and **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**—using the **Wine dataset** from the `sklearn.datasets` library. The goal is to understand how these clustering techniques work, how to evaluate their performance, and how to visualize and interpret the results.

---

##  What This Lab Covers

- Loading and preparing the Wine dataset.
- Standardizing features to make them suitable for clustering.
- Applying **Agglomerative Hierarchical Clustering**.
- Generating and interpreting **dendrograms**.
- Applying **DBSCAN clustering** with multiple parameter settings.
- Visualizing clusters using **PCA projections**.
- Evaluating cluster quality using:
  - **Silhouette Score**
  - **Homogeneity Score**
  - **Completeness Score**
- Analyzing and comparing the results of the two clustering techniques.

---

##  Key Insights

- **Hierarchical Clustering** successfully grouped wine samples into clusters that closely resembled the actual wine classes when visualized via PCA.
- **DBSCAN** was able to identify dense regions and noise but required careful parameter tuning (`eps` and `min_samples`) to produce meaningful clusters.
- **Silhouette Score** was useful to assess how well-defined the clusters were internally.
- **Homogeneity and Completeness Scores** helped understand how well clustering labels matched the original target classes.

---

##  Comparison of Techniques

| Technique               | Strengths                                                                 | Weaknesses                                                        |
|------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------|
| Hierarchical Clustering| Interpretable dendrogram, no need to specify number of clusters initially | Less scalable with large datasets                                 |
| DBSCAN                 | Detects noise and arbitrary shaped clusters                               | Sensitive to parameter values, struggles with varying densities   |

---

##  Challenges Faced

- Selecting optimal `eps` and `min_samples` values for DBSCAN took multiple iterations.
- Visualizing high-dimensional data required dimensionality reduction (PCA).
- Some clusters formed by DBSCAN included outliers, impacting silhouette score.

---

##  Decisions Made

- Used `StandardScaler` for feature normalization prior to clustering.
- Applied **PCA** to reduce dimensionality to 2D for better visualization.
- Chose evaluation metrics based on both internal (silhouette) and external (homogeneity/completeness) validation.

---

## 📁 Files Included

- `lab5_clustering.ipynb` – Main Jupyter Notebook containing all code, plots, and analysis.
- `README.md` – This file providing an overview of the lab assignment.

---
