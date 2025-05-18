# 🚗 Waze App Churn Prediction — Google Advanced Data Analytics Capstone
## Project: Predicting Monthly User Churn to Improve Retention Strategies

As part of the Google Advanced Data Analytics Certificate program, I analyzed user activity data from Waze, a global navigation app, to develop a model that predicts monthly user churn—defined as users uninstalling or ceasing to use the app.

Understanding user churn is vital for retention and growth. Identifying users at high risk of churning enables proactive engagement strategies such as targeted promotions or product interventions.

## 🔍 Project Objectives
- Predict whether a user will churn or be retained based on app usage patterns.
- Understand the drivers of churn through data exploration and feature engineering.
- Compare performance across logistic regression, random forest, and XGBoost models.

## 📊 Dataset Overview
- ~15,000 user records with 13 initial features.
- Key variables included:
   - label (churned or retained),
   - session (app opens),
   - n_days_after_onboarding,
   - driven_km_drives, duration_minutes_drives, activity_days, driving_days,
   - Device type (iOS or Android),
   - Favorite place navigations (total_navigations_fav1, fav2).

![image](https://github.com/RoniF-pixel/Projects/assets/121540731/10090c6f-a260-470a-8885-4b2ec158c967)

## 🔧 Feature Engineering
To enhance predictive power, several new features were engineered:
- km_per_drive: total km divided by number of drives.
- km_per_hour: proxy for driving speed or route type.
- percent_sessions_in_last_month: recency of use.
- total_sessions_per_day: user engagement level.
- percent_of_sessions_to_favorite: user loyalty to specific destinations.
- professional_driver: binary indicator separating frequent/high-volume users.

Notably, professional drivers had a churn rate of just 7.6%, compared to 19.9% among other users.

## 🤖 Modeling & Evaluation
Three models were built and compared:

#### 1. Logistic Regression
- Baseline model.
- Lower recall and AUC, limited non-linear pattern detection.

#### 2. Random Forest
- Improved accuracy and feature importance interpretability.
- Recall remained relatively low.

#### 3. XGBoost (Final Model)
- Accuracy: 81%
- Precision: 42%
- Recall: 17%
- Outperformed both logistic regression and random forest on recall—nearly double the recall of logistic regression, and 50% better than the forest model.
- Model Limitations:
     - Predicted 3x more false negatives than false positives.
     - Only correctly identified ~16.6% of actual churners.

![image](https://github.com/RoniF-pixel/Projects/assets/121540731/3f0eefab-39f9-402a-a48a-f6631df6f38e)

## 🧠 Key Takeaways
- Churners used the app less frequently but drove farther and longer per session than retained users.
- Engineered features dominated the model’s top predictors, reinforcing the value of domain-informed feature engineering.
- Despite solid accuracy and precision, low recall limits the model's effectiveness for high-stakes business decisions.
- The model still holds value for guiding exploratory analysis and identifying patterns in user behavior.

## 📂 Repository
[Code notebooks include](https://github.com/RoniF-pixel/Python-Projects/blob/main/Waze/Waze.ipynb):
EDA, Feature engineering logic, Model training and evaluation, Visualizations of feature importance and churn patterns

##  Next Steps
- Explore ensemble stacking or SMOTE to address class imbalance.
- Improve recall via alternative thresholds or cost-sensitive learning.
- Collaborate with product teams to validate new features using domain insights.

In this project I used several data science techniques—from wrangling and exploration to modeling and critical evaluation—applied to a **realistic**, **business-relevant challenge** in user engagement analytics.
