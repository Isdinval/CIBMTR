# 📌 CIBMTR - Equity in Post-HCT Survival Predictions

## 🏥 Project Overview

This project aims to **develop fair and accurate survival prediction models** for patients undergoing **allogeneic Hematopoietic Cell Transplantation (HCT)**. Traditional survival models often exhibit biases related to race, socioeconomic status, and geographic location. Our goal is **to improve the equitability of survival predictions using machine learning and survival analysis techniques.**

This work was conducted as part of a **Kaggle competition**, leveraging **synthetic data** generated from real-world CIBMTR datasets using the **SurvivalGAN** method.

## 🎯 Objectives

- Improve survival predictions for HCT patients.
- Reduce racial disparities in model performance.
- Optimize Stratified Concordance Index (C-index) for fair evaluation.
- Use a robust ensemble learning approach (LightGBM, XGBoost, Random Forest, Cox Models).
- Implement feature engineering to enhance predictive power.


## 📂 Dataset

The dataset consists of 59 features, covering:

- Demographics (age, sex, race, ethnicity).
- Medical characteristics (disease status, HLA matching, Karnofsky score).
- Socioeconomic factors (insurance type, distance to center).
- Outcome variables:
  - efs: Event-Free Survival (binary).
  - efs_time: Time to Event-Free Survival (censored survival time).
- 📌 Data Source: Synthetic dataset generated via SurvivalGAN, preserving real-world distributions.


## 🛠 Tech Stack & Libraries
- Python (pandas, NumPy, scikit-learn)
- Machine Learning: LightGBM, XGBoost, RandomForest, CatBoost
- Survival Analysis: lifelines (Cox Proportional Hazards, Kaplan-Meier, Nelson-Aalen)
- Optimization: StratifiedGroupKFold, hyperparameter tuning
- Data Processing: Feature Engineering, StandardScaler, Label Encoding

## 🔥 Model Pipeline
### 1️⃣ Data Preprocessing
- Handling missing values (race-specific imputation).
- Encoding categorical variables.
- Standardizing numerical features.
  
### 2️⃣ Feature Engineering
- Medical & demographic interactions.
- Socioeconomic indicators.
- Polynomial & log-transformed features.
  
### 3️⃣ Model Training
- Stratified K-Fold Cross-Validation (fair representation of race groups).
- LightGBM, XGBoost, RandomForest for regression targets.
- Cox Models (Proportional Hazards) for survival targets.
- Ensemble predictions via weighted averaging.
  
### 4️⃣ Evaluation
- Stratified Concordance Index (C-index).
- Per-group performance analysis (ensuring fairness).

  
## 📊 Results & Insights
- Higher prediction accuracy with ensemble models.
- Reduced racial disparities in prediction performance.
- Stratified C-index optimization ensured fairness across different demographic groups.

📌 Key Finding: Feature engineering and stratified evaluation significantly improved prediction fairness and robustness.
