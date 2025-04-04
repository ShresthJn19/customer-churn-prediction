# 📉 Telco Customer Churn Analysis + Model Building

This notebook analyzes customer churn behavior in a telecom company using the IBM Telco Customer Churn dataset. The focus is on understanding key churn drivers and building a predictive model using Random Forest.

---

## 📊 Dataset Overview

- **Source:** IBM Sample Dataset
- **Rows:** 7,043 customer records
- **Target:** `Churn` (Yes/No)

### Key Features:
- Customer demographics (gender, senior citizen, dependents)
- Subscription services (internet, streaming, tech support, etc.)
- Account info (tenure, contract, billing)
- Charges (monthly & total)

---

## ✅ Project Workflow

### 1. Data Cleaning & Preprocessing
- Converted `TotalCharges` to numeric, handled coercion errors
- Removed rows with missing values (mostly new customers with no usage)
- Converted `SeniorCitizen` from 0/1 to Yes/No
- Binned `tenure` into labeled groups (`1-12`, `13-24`, etc.)
- Dropped non-informative columns (e.g., `customerID`)

### 2. Exploratory Data Analysis
- Distribution of churn vs non-churn customers
- Segment analysis: churn rates by tenure group, contract type, payment method
- Charge distribution and comparisons
- Correlation matrix for numerical features

### 3. Model Building – Random Forest
- Trained a `RandomForestClassifier` on cleaned data
- Used train-test split to evaluate model
- Visualized confusion matrix and computed F1-score
- Displayed feature importances to understand predictive power

---

## 🔍 Key Insights

- Month-to-month customers have the highest churn risk
- Short-tenure users (1–12 months) churn more often
- High monthly charges and manual payment methods are common among churners
- Services like tech support and online security influence retention

---

## ⚙️ Technologies & Libraries

- Python 3.12.9
- Jupyter Notebook
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- imbalanced-learn (SMOTE handling)

---

## 👤 Author

Shresth Jain
