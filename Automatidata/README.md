## NYC Taxi Tipping Behavior Prediction
**Automatidata** partners with clients to transform unused or stored data into actionable insights and practical tools—including performance dashboards, customer-facing applications, and strategic analytics. In this project, Automatidata is consulting for the New York City Taxi and Limousine Commission (TLC), the agency responsible for regulating NYC's yellow taxis and for-hire vehicles.

## Project Overview
TLC requested a machine learning model to predict whether a passenger is likely to leave a tip, with the goal of alerting taxi drivers in real-time through an app. Given that many drivers depend heavily on gratuities to make a living, identifying low- and high-tipping passengers could help drivers better manage their income potential.

The model was developed using NYC Yellow Taxi trip data from 2017, consisting of over 22,000 unique trips and 18 features. These include trip duration, distance, tolls, fare amounts, payment type, and vendor information.

## Motivation
According to Salary.com, the average annual salary for a New York City taxi driver is about $45,000, while median monthly rent exceeds $6,500. This economic imbalance emphasizes the need to better understand factors that influence tipping behavior, potentially empowering drivers to optimize income and improve service outcomes.

## Data Preparation
Key data processing steps included:

#### Feature Engineering:

  - Calculated tip percentage and flagged "generous tippers" (>20% tip).
  - Created a binary variable for rush hour trips.

#### Data Cleaning:

  - Removed redundant or irrelevant columns.
  - Converted data types as needed for model compatibility.

A bar chart was generated to visualize the ratio of generous to non-generous tippers 

![image](https://github.com/RoniF-pixel/Projects/assets/121540731/c348cb1e-8e1b-4d7d-92f1-f94a42b0d1c2)

## Modeling Approach
Two models were developed:

  1. Multiple Linear Regression – Provided a baseline and interpretability.
  2. Random Forest Classifier – A more robust, non-linear approach, comprising 300 decision trees.

The random forest model achieved:

  - 68% accuracy
  - 67% precision (in identifying generous tippers)

## Feature Importance
The most influential features identified by the random forest model were:

    - VendorID
    - predicted_fare
    - mean_duration
    - mean_distance

Interestingly, VendorID was the most predictive variable, suggesting that certain vendors may attract more generous passengers—a finding that warrants further investigation.

![auto-important](https://github.com/RoniF-pixel/Projects/assets/121540731/107ae1fd-16c1-4268-9b57-12332020a71a)


## Implications and Next Steps
This model provides a practical tool for NYC taxi drivers to anticipate tipping behavior and manage expectations. However:

   - A parametric model could help quantify the exact influence of each variable on tip size.
   - Adding rider history (e.g., previous tipping behavior) could significantly enhance model performance.
   - Further exploration is needed to understand why certain features (like VendorID) matter most.

## Conclusion
This project highlights how machine learning can support real-world decision-making in urban transport settings. By helping drivers anticipate tipping likelihood, the model contributes toward making taxi driving a more sustainable and data-informed profession.
