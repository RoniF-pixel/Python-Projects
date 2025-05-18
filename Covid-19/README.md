

#  COVID-19 Risk Classification & Analysis

This project aims to classify patient risk levels (specifically mortality) during the COVID-19 pandemic using clinical and demographic variables. We implemented various machine learning models to predict patient outcomes and performed exploratory data analysis to uncover meaningful relationships between comorbidities, symptoms, and COVID-19 severity.

##  📌Project Overview

- **Objective**: Predict mortality risk among COVID-19 patients based on symptoms, comorbidities, and demographic data.
- **Tools**: Python, Scikit-learn, Statsmodels, Pandas, Matplotlib, Seaborn, Tableau
- **Data Source**: Mexican government health data via Kaggle
- **Techniques**:
     - Logistic Regression, Decision Trees, Random Forests, Naive Bayes
     - Class imbalance handling via oversampling
     - Confusion matrix analysis and recall prioritization


##  ⚙️Key Models & Performance

| Model               | Accuracy | Recall ("Dead") | Recall ("Not Dead") | Comments                                                                 |
|--------------------|----------|------------------|----------------------|--------------------------------------------------------------------------|
| Logistic Regression | 90%      | **91%**          | 90%                  | Best balance of recall and interpretability                              |
| Naive Bayes         | 88%      | 88%              | 88%                  | Simple model, decent performance                                         |
| Decision Tree       | 92%      | 68%              | 96%                  | High accuracy, **poor recall** on "Dead" class                           |
| Random Forest       | 92%      | 70%              | 95%                  | Similar to Decision Tree; suffers from Type II errors on minority class  |

 **Conclusion**: While tree-based models achieved the highest accuracy, their recall for the "Dead" class was insufficient, risking dangerous false negatives. Logistic regression offered the best balance between sensitivity and specificity for high-risk classification.

##  🔍Key Findings

- **Mortality**: 7.3% of all patients died. Of those, 70.5% were confirmed COVID-19 carriers.
- **Infection Rate**: 37.5% of patients were COVID-19 positive. Among them, ~14% died.
- **Age Effect**: Older individuals had a significantly higher risk of infection and death.
- **Obesity**: Strongly correlated with increased likelihood of being a COVID-19 carrier.
- **Comorbidities**: Patients with pneumonia, hypertension, and diabetes had a higher probability of infection and severe outcomes.
- **Hospitalization**:
  - 19% of all patients were hospitalized.
  - Of those, 35% died.
  - 91% of deceased patients had been hospitalized.
  - 9% were admitted to the ICU, nearly half of whom died.
- **Temporal Trends**: Peak death rate occurred from April to August 2020.

##  ⚠️Data Considerations
- Class Imbalance: Addressed using oversampling; future iterations may benefit from SMOTE or ensemble methods to reduce noise and improve minority-class prediction.

- Multicollinearity: Checked using correlation matrices; predictors with high variance inflation were monitored.

- Feature Engineering: Dummy variables and recoding applied where appropriate.

## ✅ Conclusions & Recommendations
- Prioritize Recall for High-Risk Outcomes: In healthcare applications, especially mortality risk classification, high recall for the minority (deceased) class is more critical than overall accuracy.

- Logistic Regression Remains Valuable: Simple models like logistic regression can outperform complex classifiers when interpretability and balanced recall are prioritized.

- Improve Imbalanced Learning Approaches: Future improvements could include cost-sensitive learning, SMOTE, or ensemble methods like XGBoost with class weighting.

- Support Policy with Data: Age, comorbidity presence, and obesity emerged as strong indicators of risk—these findings can help guide triage, vaccination prioritization, or public health resource allocation.

- Extend Beyond Mortality: Similar approaches could be adapted to model hospitalization, ICU admission, or long-COVID outcomes using richer longitudinal datasets.


##  Repository

[GitHub Link to Project](https://github.com/RoniF-pixel/Python-Projects/tree/main/Covid-19)

## References

The dataset is obtained from Kaggle at the following link: [kaggle](https://www.kaggle.com/datasets/meirnizri/covid19-dataset), 
and was provided by the Mexican government, which can be found at this link: 
[Mexican government data](https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico)

## Visuals

![1 covid](https://github.com/user-attachments/assets/b7f58070-49e7-4a12-ba26-cb6956d80d33)

![2 covid](https://github.com/user-attachments/assets/c6ceb83e-feb1-477e-a8ad-25e490ad38cb)




Hope this repo will help you to assess my coding, data analytics skills or will be just fun for you to look through.


