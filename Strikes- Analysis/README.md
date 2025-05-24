# ⚡ Lightning Strike Data Analysis (NOAA - August 2018)
This project explores and forecasts lightning strike data collected by the National Oceanic and Atmospheric Administration (NOAA) for August 2018. The notebook performs data cleaning, integration, visualization, time series modeling (using SARIMAX), and forecasting.

## 📊 Project Overview
The analysis focuses on two datasets:

**Dataset 1**: Includes geospatial data with columns: date, center_point_geom, longitude, latitude, number_of_strikes.
**Dataset 2**: Includes region-based data with columns: date, zip_code, city, state, state_code, center_point_geom, number_of_strikes.

We aim to:

- Merge the datasets into a unified DataFrame.
- Explore and visualize strike patterns.
- Perform time series forecasting using SARIMAX.
- Evaluate model performance and residuals.

## 🛠️ Technologies Used

- Python
- Pandas, NumPy – Data manipulation
- Matplotlib, Seaborn – Visualization
- statsmodels – SARIMAX modeling
- SciPy – Statistical tools
- Jupyter Notebook – Interactive analysis




