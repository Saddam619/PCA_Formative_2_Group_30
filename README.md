# PCA_Formative_2_Group_30

# PCA-Based African Nations Health Analysis

A comparative health outcomes analysis across African nations using Principal Component Analysis (PCA) implemented from scratch in Python.

---

## 👥 Authors & Team Members

* **Saddam Adam** 
* **Sylvie Tumukunde**

---

## 📌 Project Overview

This project applies unsupervised machine learning and linear algebra techniques to analyze population health indicators across 50 African nations. Using a 14-variable WHO global health outcomes dataset, we implement Principal Component Analysis (PCA) **from scratch using only `NumPy` and `Matplotlib`** (without `scikit-learn`).

The objective is to reduce dimensionality, reveal latent structural variance across health profiles, and isolate critical separating health drivers (such as HIV prevalence, immunization coverage, and child mortality).

---

## 📂 Dataset Details

* **Source File:** `health-outcomes-csv-1.csv` ([Global Health Outcomes Data on Kaggle](https://www.kaggle.com/datasets/thedevastator/global-health-outcomes-data))
* **Scope:** Filtered from 196 global entries to 50 African countries.
* **Feature Set:** 14 numerical indicators including:
  * Infant and under-five mortality rates
  * Immunization coverage (DTP, Measles)
  * Infant malnutrition and exclusive breastfeeding rates
  * Adult disease prevalence (HIV, TB, Malaria)

---

## 🔬 Methodology & Implementation Steps

1. **Data Cleaning & Standardization:**
   * Handled categorical name encoding and string-to-float conversions.
   * Imputed missing values using column-wise means.
   * Standardized features to zero mean ($\mu = 0$) and unit variance ($\sigma = 1$).

2. **Covariance Matrix Construction:**
   * Calculated the $14 \times 14$ feature covariance matrix to quantify pairwise linear relationships.

3. **Eigen-Decomposition & Component Ranking:**
   * Derived eigenvalues and eigenvectors using `np.linalg.eig`.
   * Ranked principal components in descending order of explained variance.

4. **Dimensionality Reduction & Projection:**
   * Selected components meeting the 95% cumulative explained variance threshold.
   * Projected data points onto the top 2 Principal Components (PC1 & PC2).

5. **Comparative Visualization:**
   * Plotted raw feature space versus PC space using `Matplotlib` to isolate key regional health clusters.

---

## 📁 Repository Structure
