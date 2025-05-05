

#  COVID-19 Risk Classification & Analysis (Python)

This project aims to classify patient risk levels (specifically mortality) during the COVID-19 pandemic using clinical and demographic variables. We implemented various machine learning models to predict patient outcomes and performed exploratory data analysis to uncover meaningful relationships between comorbidities, symptoms, and COVID-19 severity.

##  Repository Structure

- `data/`: Raw dataset (de-identified for privacy)
- `notebooks/`: EDA and model development notebooks
- `models/`: Trained model outputs and performance evaluations
- `tables_figures/`: Key summary tables and diagnostic plots
- `results/`: Final reports and interpretive summaries

##  Project Overview

- **Objective**: Predict mortality risk among COVID-19 patients based on symptoms, comorbidities, and demographic data.
- **Tools**: Python, Scikit-learn, Statsmodels, Pandas, Matplotlib, Seaborn, Tableau
- **Techniques**: Logistic Regression, Decision Trees, Random Forests, Naive Bayes, Oversampling, Confusion Matrix Analysis

##  Key Models & Performance

| Model               | Accuracy | Recall ("Dead") | Recall ("Not Dead") | Comments                                                                 |
|--------------------|----------|------------------|----------------------|--------------------------------------------------------------------------|
| Logistic Regression | 90%      | **91%**          | 90%                  | Best balance of recall and interpretability                              |
| Naive Bayes         | 88%      | 88%              | 88%                  | Simple model, decent performance                                         |
| Decision Tree       | 92%      | 68%              | 96%                  | High accuracy, **poor recall** on "Dead" class                           |
| Random Forest       | 92%      | 70%              | 95%                  | Similar to Decision Tree; suffers from Type II errors on minority class  |

 **Conclusion**: While tree-based models achieved the highest accuracy, their recall for the "Dead" class was insufficient, risking dangerous false negatives. Logistic regression offered the best balance between sensitivity and specificity for high-risk classification.

##  Key Findings

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

##  Data Considerations

- Oversampling was used to address class imbalance, which may have introduced noise.
- Future improvements could include undersampling or synthetic sampling (e.g., SMOTE).
- Feature selection and multicollinearity assessment were considered using Statsmodels and correlation plots.

##  Lessons Learned

- High accuracy does not imply reliability, especially with imbalanced data.
- Prioritizing recall on minority/high-risk classes (like "Dead") is critical in health-related classification problems.
- Logistic regression, though simple, can be robust and interpretable when used thoughtfully.

##  Repository

[GitHub Link to Project](https://github.com/RoniF-pixel/Python-Projects/tree/main/Covid-19)


The dataset is obtained from Kaggle at the following link: [kaggle](https://www.kaggle.com/datasets/meirnizri/covid19-dataset), 
and was provided by the Mexican government, which can be found at this link: 
[Mexican government data](https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico)


![1 covid](https://github.com/user-attachments/assets/b7f58070-49e7-4a12-ba26-cb6956d80d33)

![2 covid](https://github.com/user-attachments/assets/c6ceb83e-feb1-477e-a8ad-25e490ad38cb)




Hope this repo will help you to assess my coding, data analytics skills or will be just fun for you to look through.


