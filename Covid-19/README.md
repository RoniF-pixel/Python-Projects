Introduction:

Coronavirus disease (COVID-19) is an infectious disease caused by a newly discovered coronavirus. Most people infected with COVID-19 virus will experience mild to moderate respiratory illness and recover without requiring special treatment. Older people, and those with underlying medical problems like cardiovascular disease, diabetes, chronic respiratory disease, and cancer are more likely to develop serious illness. During the entire course of the pandemic, one of the main problems that healthcare providers have faced is the shortage of medical resources and a proper plan to efficiently distribute them. In these tough times, being able to predict what kind of resource an individual might require at the time of being tested positive or even before that will be of immense help to the authorities as they would be able to procure and arrange for the resources necessary to save the life of that patient. Machine learning models offer promising prospects in this regard.
The main goal of this project is to build a machine learning model that, given a Covid-19 patient's current symptom, status, and medical history, will predict whether the patient is at high risk or not.

Methodology:

This study employs five distinct machine learning models: Logistic Regression, Decision tree classifier, Random forest classifier, Naive Bayes, and XGBoost classifier. These models are applied to analyze medical data accurately. This dataset contains an enormous number of anonymized patient-related information including pre-conditions. The raw dataset consists of 21 unique features and 1,048,576 unique patients. In the Boolean features, 1 means "yes" and 2 means "no". values as 97 and 99 are missing data. The features can be explained as follows:

- sex: 1 for female and 2 for male.
- age: of the patient.
- classification: covid test findings. Values 1-3 mean that the patient was diagnosed with covid in different degrees. 4 or higher means that the patient is not a carrier of covid or that the test is inconclusive.
- patient type: type of care the patient received in the unit. 1 for returned home and 2 for hospitalization.
- pneumonia: whether the patient already have air sacs inflammation or not.
- pregnancy: whether the patient is pregnant or not.
- diabetes: whether the patient has diabetes or not.
- copd: Indicates whether the patient has Chronic obstructive pulmonary disease or not.
- asthma: whether the patient has asthma or not.
- inmsupr: whether the patient is immunosuppressed or not.
- hypertension: whether the patient has hypertension or not.
- cardiovascular: whether the patient has heart or blood vessels related disease.
- renal chronic: whether the patient has chronic renal disease or not.
- other disease: whether the patient has other disease or not.
- obesity: whether the patient is obese or not.
- tobacco: whether the patient is a tobacco user.
- usmr: Indicates whether the patient treated medical units of the first, second or third level.
- medical unit: type of institution of the National Health System that provided the care.
- intubed: whether the patient was connected to the ventilator.
- icu: Indicates whether the patient had been admitted to an Intensive Care Unit.
- date died: If the patient died indicate the date of death, and 9999-99-99 otherwise.

The dataset is obtained from Kaggle at the following link: https://www.kaggle.com/datasets/meirnizri/covid19-dataset, and was provided by the Mexican government, which can be found at this link: https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico

Findings:

- Unfortunately 7.3% of the total patients have died, with about 70.5% of them were Covid Carriers.
- As for the total carriers they were about 37.5% out of the total patients.
- About 14% of those carriers have died.
- We found that age has a significant impact; as it increases chances of getting the virus increases.
- We also found that people who are suffering from obesity are more likely to carry the virus.
- As for pregnancy, we couldn't find any impact on Covid classification.
- We noticed that patients with "Pneumonia", "Hypertension", "Diabetes" and tobacco users have a great chance of getting the virus with "Pneumonia" patients being the most.
- We also noticed that there's a positive correlation between having "Hypertension" and "Diabetes" diseases; as most patients with one of those two diseases are subjected to get the other.
- We saw that among all the patients of these diseases the patients classified with 3rd degree of Covid are the highest by far.
- About 19% of the total patients were hospitalized, with a death percentage of 35%.
- The "Pneumonia" disease has the greatest impact on that percentage (35%).
- About 91% of the dead patients were hospitalized.
- About 9% out of the hospitalized patients were admitted to the ICU, with about 56% of them being classified as Covid carriers, and with a great percentage of death of about 49%.
- The death was very trending during mid 2020 starting from April up till August.

![1 covid](https://github.com/user-attachments/assets/b7f58070-49e7-4a12-ba26-cb6956d80d33)

![2 covid](https://github.com/user-attachments/assets/c6ceb83e-feb1-477e-a8ad-25e490ad38cb)


Conclusion:

From the above results we can see that althogh we got the highest accuracy (about 92%) from both Decision Tree & Random Forrest algorithms, but the recall was very bad in the "Dead" class, and since we care the most about our "false negatives" (predicting a patient to be having no risks, while he/she is actually at high risk) which results in type 2 error; our judgement will be based on the recall and here's where those algorithms fail with their misleading accuracy.

So, from the point of view of both the accuracy and the recall togther, the best model was the "Logistic Regression" with about 90% accuracy and lowest recall ("Not dead" class), and even a bit higher recall in the "Dead" class (about 91%).

Comes next the "Naive Bayes" with an accuracy of 88% and with a lowest recall of 88% (both classes). We can also notice that we sacrificed both the precision and f1 score which came pretty low in every report. Probably, we could've achieved better results if we undersampled our train dataset instead of oversampling it (as it will reduce the great noise in our data), but this could have resulted in losing a great portion of our data, and thus losing it's integrity.




Hope this repo will help you to assess my coding, data analytics skills or will be just fun for you to look through.


