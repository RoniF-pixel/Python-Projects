# ⚡ Lightning Strike Data Analysis (NOAA - August 2018)
This project analyzes lightning strike data across the United States during August 2018. Using NOAA datasets, we merge, clean, and explore spatial and temporal patterns, perform hypothesis testing, and apply time series forecasting using a SARIMA model to understand short- and long-term dynamics in lightning activity.

---

## 📊 Project Overview
The analysis focuses on two datasets:

- **Dataset 1**: Includes geospatial data with columns: date, center_point_geom, longitude, latitude, number_of_strikes.
- **Dataset 2**: Includes region-based data with columns: date, zip_code, city, state, state_code, center_point_geom, number_of_strikes.

We aim to:

- Merge the datasets into a unified DataFrame.
- Explore and visualize strike patterns.
- Perform time series forecasting using SARIMAX.
- Evaluate model performance and residuals.

---

## 🔧 Data Preparation

- Merged datasets using pandas.merge().
- Used isnull() to identify missing metadata.
- Visualized missing data points on a latitude–longitude map using Plotly.

Finding: Most missing entries originated from offshore locations outside U.S. landmass.

---

## 🌍 Spatial Join

- Converted coordinates into Shapely Point objects.
- Loaded U.S. state polygons via GeoPandas.
- Spatial join confirmed missing-state entries were mostly offshore or outside U.S. boundaries.

---

## 🏷️ Feature Engineering

- Parsed timestamps, extracted day-of-week.
- Created binary indicators: is_weekend, is_usa.
- Tagged strikes missing state info as offshore.

---

## 📉 Descriptive Statistics

- U.S. strikes: ~324K
- Non-U.S. strikes (offshore): ~394K

---

## 🧪 Hypothesis Testing
**Weekday vs Weekend (Temporal)**
    - Two-sample t-test shows significantly fewer strikes on weekends than weekdays.
    - p < 0.001, t < 0

**Intensity by State (Spatial)**
    - Calculated average strike intensity per state.
    - Central U.S. (Arkansas, Kentucky, Oklahoma) had the highest values.
    - One-way ANOVA confirms variation:
          - F = 157.81, p < 0.001

---

## 📆 Temporal Patterns
- Lightning activity peaked:
      - August 17: ~1M strikes
      - August 28: ~1.05M strikes

- Midweek peaks; weekends showed reduced activity.

---

## ⏱️ Time Series Forecasting (SARIMA Model)
**Model Fit Summary**
      - Model Used: SARIMA
      - AIC: 750.25 → better than baseline ARIMA(0,1,0)
      - Log-Likelihood: Improved from ~-399 to higher values
**Coefficient Summary**
      | Parameter        | Estimate Summary                                     |
| ---------------- | ---------------------------------------------------- |
| `ar.L1`          | Significant (p = 0.045): captures persistence        |
| `ma.L1`          | Not significant                                      |
| `seasonal_ar.L7` | Significant (p = 0.012): confirms weekly seasonality |
| `seasonal_ma.L7` | Marginal (p ≈ 0.08)                                  |
| `sigma2`         | Reasonable, significant variance estimate            |

**Residual Diagnostics**
- Histogram: Right-skewed → residuals not normally distributed
- Time Series Plot: Large early spike; stable behavior afterward
- ACF of Residuals: No significant autocorrelation
- PACF of Residuals: Clean; all lags within bounds
- Conclusion: Residuals resemble white noise, though non-normality and early outliers exist

**Forecast (September 1–7)**
- Observed (Blue Line): Data from August 1–31, with peaks mid-month
- Forecast (Orange Line): SARIMA-predicted values for September 1–7
- Confidence Interval (Shaded): 95% prediction interval

**Interpretation**
- Central forecast is flat and modest (expected after late-August decline)
- Wide, asymmetric confidence intervals, ranging from near zero to 4M strikes
- Likely due to:
       - High volatility in observed data
       - Non-normal residuals
       - One or more extreme past events

- Upper bound spike: Model is cautious — covers rare but extreme lightning bursts

---

## Recommendations
- Improve model: Consider exogenous variables (e.g., weather, humidity)
- Stabilize variance: Use log-transformation (already applied in this case)
- Flag outliers: Early spike may skew model
- Communicate uncertainty: Forecasts have large confidence intervals

---

## 🧰 Tools & Libraries
- Data Handling: pandas, numpy
- Modeling & Stats: statsmodels, scipy
- Geospatial Analysis: geopandas, shapely
- Visualization: matplotlib, seaborn, plotly
- Forecasting: SARIMA via statsmodels.tsa.statespace.SARIMAX

---

## 📌 Key Takeaways
- Offshore strikes were the main source of missing metadata.
- Weekends had significantly fewer strikes than weekdays.
- Central U.S. exhibited the highest strike intensities.
- SARIMA successfully modeled short-term and weekly seasonal trends.
- However, the model’s forecast uncertainty is high, especially during volatile periods.

---

### 👩 Author
**Ronak Fathi**
Statistical analysis • Geospatial modeling • Forecasting • Data storytelling
