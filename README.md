# Online News Popularity Analysis

This repository contains a machine learning project that analyzes the **Online News Popularity Dataset** to identify factors influencing whether an online news article becomes popular. The study combines **supervised**, **unsupervised**, and **ensemble learning** methods.

The project was developed as a group assignment at the **University of Amsterdam – Economics and Business School**.

---

## 📌 Project Objectives

- Classify news articles as **popular** or **unpopular** based on a share threshold
- Identify key determinants of article popularity
- Explore latent patterns in the data using clustering techniques
- Compare supervised models and improve performance using ensemble learning

---

## 📊 Dataset

- **Source:** Fernandes, K., Vinagre, P., & Cortez, P. (2015)
- **Observations:** 39,644 online news articles
- **Features:** 61 numerical features covering:
  - Word usage
  - Links and self-references
  - Digital media (images, videos)
  - Publication time
  - Keywords
  - NLP features (sentiment, subjectivity)
- **Target variable:** Number of shares  
- **Popularity threshold:**  
  Articles with **≥ 1400 shares** are labeled as *popular*

Dataset files are located in the `data/` folder.

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Dropped irrelevant columns (e.g., URL)
- Outlier detection using **Isolation Forest**
- Standardization of features
- Train–test split (80/20)

### 2. Supervised Learning Models
- Logistic Regression
- XGBoost
- Support Vector Machines (SVM)
- Gaussian Naive Bayes

Hyperparameter tuning was performed using **Grid Search with cross-validation**.

### 3. Unsupervised Learning
- K-Means Clustering
- Gaussian Mixture Models (GMM)
- Agglomerative Clustering
- PCA for visualization

Clustering was applied to different feature subsets (words, NLP, links, digital content, etc.).

### 4. Ensemble Learning
- Weighted Majority Voting
- Combined predictions from:
  - Logistic Regression
  - XGBoost
  - Naive Bayes
  - SVM

---

## 📈 Key Results

- **Best individual model:** XGBoost (~69% accuracy)
- **Ensemble model:** Balanced performance (~66% accuracy)
- NLP-related features and word usage showed strong clustering patterns
- Temporal features had limited predictive power

---

## 📂 Repository Structure

