# CEI Internship Program 2026 – Week 2 Assignment

## End-to-End Machine Learning Pipeline on Tesla Sales and Pricing Data

### Author
Sankalp Tamboli

---

## Project Overview

This project implements a complete end-to-end Machine Learning workflow on Tesla sales and pricing data. The objective is to predict Tesla vehicle deliveries using historical production, pricing, and vehicle-related information while also forecasting future delivery trends using time series analysis.

The project covers the entire machine learning lifecycle, including:

- Data preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Machine learning pipelines
- Regression modeling
- Hyperparameter tuning
- Time series forecasting

---

## Dataset Features

The dataset contains Tesla-related information across multiple regions and models, including:

- Year
- Month
- Region
- Model
- Estimated_Deliveries
- Production_Units
- Avg_Price_USD
- Battery_Capacity_kWh
- Range_km
- CO2_Saved_Tons
- Source_Type
- Charging_Stations

---

## Data Preprocessing

The following preprocessing steps were performed:

- Dataset inspection using `.info()`, `.describe()`, and `.head()`
- Missing value analysis
- Duplicate record detection
- Datetime feature creation using Year and Month
- Chronological sorting for time-series analysis
- Data quality verification

---

## Exploratory Data Analysis (EDA)

Several analyses were performed to understand data characteristics:

### Distribution Analysis
- Histograms of numerical variables
- Distribution of delivery volumes

### Outlier Analysis
- Boxplots for detecting extreme observations
- Evaluation of whether outliers represent genuine business variation

### Correlation Analysis
- Correlation heatmap
- Relationship between production and deliveries

### Business Analysis
- Regional performance comparison
- Tesla model performance comparison
- Source type comparison
- Yearly delivery and production trends

---

## Feature Engineering

New features were created to improve predictive performance:

### Engineered Features

#### Prev_Deliveries
Captures previous delivery trends using lag information.

#### Delivery_Efficiency
Measures production-to-delivery conversion efficiency.

#### Price_per_km
Represents vehicle pricing efficiency relative to driving range.

---

## Machine Learning Pipeline

A unified preprocessing pipeline was implemented using:

### Numerical Features
- StandardScaler

### Categorical Features
- OneHotEncoder

### Pipeline Components
- ColumnTransformer
- Pipeline API

This approach prevents data leakage and ensures reproducible preprocessing.

---

## Regression Models

Three regression models were evaluated:

### 1. Linear Regression
Baseline model used to establish predictive performance.

### 2. Ridge Regression
Applies L2 regularization to improve coefficient stability and handle correlated features.

### 3. Lasso Regression
Applies L1 regularization and performs implicit feature selection through coefficient shrinkage.

---

## Model Evaluation Metrics

Models were evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## Model Comparison

All three models achieved exceptionally strong predictive performance.

### Best Performing Model
**Ridge Regression**

Reasons:
- Highest R² score
- Lowest MAE
- Lowest RMSE
- Better handling of correlated features through regularization

---

## Hyperparameter Tuning

GridSearchCV was used to optimize Ridge Regression.

### Objective
Identify the optimal alpha value using 5-fold cross-validation.

### Benefits
- Improved model stability
- Better generalization performance
- Reduced risk of overfitting

---

## Time Series Forecasting

Future Tesla deliveries were forecast using:

### ARIMA(1,1,1)

The forecasting workflow included:

- Monthly delivery aggregation
- Stationarity testing using ADF Test
- Differencing for trend removal
- ARIMA model fitting
- 12-month delivery forecasting

---

## Key Findings

- Production_Units exhibited the strongest relationship with Estimated_Deliveries.
- Feature engineering improved model performance by incorporating temporal and business-oriented information.
- Ridge Regression achieved the best overall predictive performance.
- Hyperparameter tuning produced only marginal improvements because the baseline model was already highly effective.
- ARIMA forecasting projected future deliveries to remain relatively stable around recent historical levels.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Statsmodels

---

## Conclusion

This project successfully developed a complete end-to-end machine learning pipeline on Tesla sales and pricing data.

The workflow included preprocessing, EDA, feature engineering, regression modeling, hyperparameter tuning, and time series forecasting. Ridge Regression emerged as the best-performing model, while ARIMA forecasting demonstrated the application of time series methods for predicting future delivery trends.

The project highlights how machine learning and forecasting techniques can be used together to support data-driven business decision making.
