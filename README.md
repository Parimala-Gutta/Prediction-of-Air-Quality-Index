#  Air Quality Index (AQI) Prediction

##  Project Overview

This project focuses on predicting Air Quality Index (AQI) using real-world environmental data obtained via API calls. The pipeline involves data collection, preprocessing, exploratory data analysis, feature engineering, and supervised machine learning model development to classify air quality into different categories based on pollutant concentrations.

The model is designed to help monitor and predict air quality levels, which are critical for public health, environmental monitoring, and regulatory compliance.

---

## Project Pipeline

1️ **Data Collection**  
- API calls to retrieve pollutant data over multiple days.  
- Data retrieved included various air pollutant concentrations (CO, Benzene, NOx, O3, NO2, etc.).

2️ **Data Cleaning & Preprocessing**  
- Handled missing values (replaced -200 and applied interpolation).
- Cleaned numeric columns (replaced commas, type conversions).
- Merged date and time into unified datetime column.
- Dropped redundant columns for focused modeling.
- Converted target AQI variable into categorical classes.

3️ **Feature Engineering**  
- Developed custom AQI calculation functions based on EPA breakpoint standards.
- Created AQI scores for multiple pollutants.
- Applied IQR methods for outlier handling.

4️ **Exploratory Data Analysis (EDA)**  
- Time-series visualization for pollutants.
- 3D scatter plot visualizing pollutant combinations.
- Analyzed pollutant correlations.

5️ **Model Development**  
- Used **XGBoost Classifier** to train on categorized AQI levels.
- Applied train-test split (70%-30%).
- Applied standard scaling to normalize feature distributions.

6️ **Model Evaluation**  
- Evaluated model accuracy and feature importance (notebook contains further plots and metrics).

---

##  Technologies Used

| Category | Tools/Libraries |
| -------- | --------------- |
| Programming Language | Python |
| Data Manipulation | pandas, numpy |
| Visualization | matplotlib, seaborn, plotly |
| API Handling | requests, json, datetime |
| Machine Learning | scikit-learn, xgboost |
| 3D Visualization | mpl_toolkits |
| Cloud APIs | External AQI data API |

---

## Sample Visualizations

- Time-series pollutant plots
- Pollutant-wise category distributions
- 3D scatterplots to visualize multi-pollutant interaction
- Model performance evaluation (accuracy, confusion matrix, feature importance)

---

