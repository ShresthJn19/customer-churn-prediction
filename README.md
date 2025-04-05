# 📉 Customer Churn Prediction – Telco Dataset

This project explores the IBM Telco Customer Churn dataset to identify key factors behind customer attrition and build a predictive machine learning model. The goal is to help telecom companies anticipate and reduce customer churn.

---

## 🎯 Objective

- Analyze customer behavior to uncover churn patterns
- Engineer features to improve model performance
- Train a classification model to predict churn risk
- Explain model behavior using SHAP values

---

## 🛠️ Tech Stack

- Python
- pandas, numpy
- seaborn, matplotlib
- scikit-learn
- imbalanced-learn (SMOTE)

---

## 📦 Dataset Overview

- **Total Records:** ~7,043
- **Source:** IBM Sample Dataset
- **Target Variable:** `Churn` (Yes/No)

Key features include:
- Demographics: gender, senior citizen, dependents
- Services: Internet, phone, security, streaming
- Contract & Billing: tenure, contract type, payment method
- Charges: monthly charges, total charges

---

## 🔍 Analysis Workflow

### 1️⃣ Data Cleaning & Preprocessing
- Converted `TotalCharges` from object to numeric
- Removed rows with missing values
- Mapped `SeniorCitizen` from 0/1 to `Yes`/`No`
- Created tenure groups (e.g., `1–12`, `13–24`, etc.)
- Dropped irrelevant column (`customerID`)

### 2️⃣ Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis of features vs churn
- Key insights:
  - Highest churn in month-to-month contracts
  - Fiber optic users churn more than DSL users
  - Electronic check payments show high churn
  - Low tenure = high churn risk

### 3️⃣ Modeling – Random Forest Classifier
- Applied SMOTE to balance churn class
- Train-test split (70-30)
- Trained `RandomForestClassifier`
- Achieved:
  - **Accuracy:** ~95.5%
  - **F1-score (churn):** 95%
  - **Confusion matrix & classification report**

## 📊 Key Results

| Metric         | Value   |
|----------------|---------|
| Accuracy       | 95.5%   |
| F1 Score       | 95%     |
| Top Features    | Contract type, tenure group, monthly charges |
| Insight         | Short-tenure users with monthly contracts and high bills are most likely to churn |
