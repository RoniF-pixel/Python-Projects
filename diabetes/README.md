# Pima Indians Diabetes Classification
This project presents a classification model built using Logistic Regression to predict the likelihood of diabetes in female patients of Pima Indian heritage, aged 21 and above. The dataset used is the well-known Pima Indians Diabetes Database, provided by the National Institute of Diabetes and Digestive and Kidney Diseases (NIDDK).

## 📊 Dataset Overview
- Source: National Institute of Diabetes and Digestive and Kidney Diseases

- Observations: 768

- Features:

    - Pregnancies
    - Glucose
    - BloodPressure
    - SkinThickness
    - Insulin
    - BMI
    - DiabetesPedigreeFunction
    - Age
    - Outcome (1: Diabetes, 0: No Diabetes)

## 🔍 Objectives
- Perform exploratory data analysis (EDA) to identify inconsistencies and relationships.
- Clean and preprocess the data to improve model quality.
- Develop a Logistic Regression classifier using scikit-learn.
- Evaluate the model using confusion matrix and classification report.

## ⚙️ Technologies Used
Python, pandas, numpy, seaborn, matplotlib, scikit-learn

## 🧹 Data Cleaning
Several features contained invalid zero values that represent missing data:

- Replaced or removed zeros from Glucose, BloodPressure, and BMI.
- Imputed SkinThickness zeros with column mean.
- Created a new binary feature InsulinKnown to indicate if Insulin level is known (non-zero).

## 📈 Exploratory Data Analysis
- Visualized missing data using heatmaps.
- Identified positive correlations:
     - Glucose vs. Insulin
     - SkinThickness vs. BMI
- Observed:
     - Right-skewed age distribution (most participants in their 20s).
     - Higher Glucose and BMI in diabetic cases.

## 🤖 Model Training
- Train-Test Split: 70% training, 30% testing.
- Algorithm: Logistic Regression (sklearn.linear_model)
- Max Iterations: 300

logmodel = LogisticRegression(max_iter=300)
logmodel.fit(X_train, y_train)
predictions = logmodel.predict(X_test)

## 🧪 Evaluation
#### Confusion Matrix
[[130  16]
 [ 25  47]]

 #### Classification Report
 - Accuracy: 81%
- Precision (Diabetes): 75%
- Recall (Diabetes): 65%

##  Conclusion
This project demonstrates the development of a logistic regression model with solid classification performance on a medical dataset. The model shows potential for real-world screening tools, though further improvements could be made through advanced techniques like feature engineering or ensemble models.

## 📌 Future Work
- Address multicollinearity and feature scaling.
- Try advanced models (e.g., Random Forest, XGBoost).
- Apply cross-validation and hyperparameter tuning.
- Perform ROC analysis and AUC scoring.



