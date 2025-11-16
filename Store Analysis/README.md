#  Time Series Forecasting of Office Supplies Sales
## Project Overview
This project applies rigorous time series analysis techniques to forecast monthly sales of Office Supplies using transactional retail data spanning January 2011 to December 2014. The goal is to build robust ARIMA and SARIMAX models to provide actionable forecasts that capture both trend and seasonal patterns.

##  Data Description
The dataset originates from a comprehensive retail transaction record from a Superstore spanning 2015 to 2018. For this analysis, data was filtered to include only the Office Supplies category and aggregated to obtain total monthly sales figures.

| **Order Date** | **Sales (USD)** |
| -------------- | --------------- |
| 2011-01        | 4,260           |
| 2011-02        | 4,740           |
| ...            | ...             |


##  Methodology
1.  Data Preparation & Exploration

- Extracted Office Supplies data subset.
- Aggregated sales monthly using pandas resample().
- Conducted exploratory data analysis (EDA) to understand trends, outliers, and seasonality.
- Performed Augmented Dickey-Fuller (ADF) test confirming the need for differencing to achieve stationarity.

2.  ARIMA Modeling

- Identified optimal (p, d, q) parameters via AIC/BIC criteria.
- Trained ARIMA models using statsmodels.tsa.ARIMA.
- Validated on a hold-out test set, evaluating with RMSE and residual diagnostics.

3.  SARIMAX Modeling

- Incorporated monthly seasonality by specifying seasonal order (P, D, Q, S) with season length S=12.
- Compared SARIMAX performance against ARIMA to capture recurring seasonal effects.

##  Results & Evaluation

| **Model** | **RMSE**  |
| --------- | --------- |
| ARIMA     | 2,621 USD |
| SARIMAX   | 1,557 USD |


-  SARIMAX outperforms ARIMA by effectively modeling seasonal fluctuations.

-  Forecasts closely track observed data, enhancing reliability for business decision-making.

##  Forecast Visualization

![sarimax-store](https://github.com/user-attachments/assets/846aa184-bd26-4224-b900-b360f01637e2)


##  Conclusions & Future Work
- SARIMAX models successfully capture seasonal and trend components, producing superior forecasts.

- Potential improvements include integrating exogenous variables such as marketing campaigns, economic indicators, or holidays to enhance predictive power.

- Exploring advanced forecasting frameworks like Facebook Prophet or LSTM networks is recommended for further accuracy gains.

##  Technical Stack
- Languages: Python 3

- Libraries: pandas, numpy, matplotlib, seaborn, statsmodels, scikit-learn

- Tools: Jupyter Notebook


##  Author
**Ronak Fathi**

Statistical Consultant & Data Analyst


