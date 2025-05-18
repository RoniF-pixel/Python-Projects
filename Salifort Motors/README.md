# 📊 Employee Retention Analysis — Google Advanced Data Analytics Capstone
## Project: Predicting Employee Attrition at Salifort Motors

As part of the Google Advanced Data Analytics Certificate, I completed a capstone project analyzing employee attrition data for a fictional alternative energy vehicle manufacturer, Salifort Motors. The company sought insights into employee retention and requested a predictive model to help identify at-risk employees and reduce turnover.

## 🧭 Objective
To identify key drivers of employee attrition and develop a predictive model to flag employees at risk of leaving, enabling targeted interventions to improve satisfaction and retention.

## 📌 Key Findings from Exploratory Data Analysis (EDA)
- Two main attrition profiles emerged:
   - Dissatisfied employees with shorter tenures
   - Highly satisfied employees with medium-length tenures

- Burnout indicators included:
    - High project count
    - Long average monthly hours
    - Lack of promotions or recognition

- Employees with 6+ years of tenure rarely left

- A subset of 4-year employees with unusually low satisfaction appeared at risk

- Data patterns suggested that poor management and workload imbalance were central to attrition

## 🧠 Modeling Approach
I developed three classification models to predict employee attrition:

1. Logistic Regression

  - Precision: 80%
  - Recall: 83%
  - F1-score: 80% (weighted)
  - Accuracy: 83%

2. Decision Tree Classifier

3. Random Forest Classifier

   - For both tree-based models, I performed two modeling rounds:

      - Full feature set
      - Engineered feature set, addressing potential data leakage

## 🔍 Addressing Data Leakage
- Certain features (e.g., satisfaction_level and average_monthly_hours) could contain leakage, possibly reflecting post-decision behavior (e.g., reduced hours after deciding to quit).

- I engineered a new binary feature called overworked, defined using project count and monthly hours thresholds, to better capture latent burnout without direct leakage.

## ✅ Final Results
- Improved Decision Tree Model (with engineered features):

   - AUC: 93.8%
   - Precision: 87.0%
   - Recall: 90.4%
   - F1-score: 88.7%
   - Accuracy: 96.2%

- Random Forest slightly outperformed the decision tree, confirming model robustness.
  
![decision-capstone](https://github.com/user-attachments/assets/c8df1041-cd54-4a3c-a629-49144d5c3d4a)

![downloadc7](https://github.com/user-attachments/assets/f3d14bfd-cefd-4d60-bbfd-83c49a276a85)

## 📂 Repository: decision-capstone
[File](https://github.com/RoniF-pixel/Python-Projects/blob/main/Salifort%20Motors/Salifort%20Motors.ipynb):  (includes code, data, and model artifacts)

This project demonstrates my end-to-end data science capabilities—from data cleaning and EDA to thoughtful feature engineering and model evaluation. It highlights my ability to recognize and address real-world challenges like data leakage and biased predictors while building models that support business decision-making.

**I hope you liked it!**
