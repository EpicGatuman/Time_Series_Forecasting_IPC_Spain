# Time Series Forecasting of Spain's Consumer Price Index (IPC)

This repository contains a time series forecasting project focused on modeling the monthly evolution of the **Consumer Price Index (IPC)** in Spain. The analysis was carried out using classical time series techniques including ARIMA, exponential smoothing models, and linear regression with external regressors.

The project was developed by Matías Mora and Marc Cascant as part of an academic course on time series analysis.

## Objective

The goal is to understand and model the evolution of the IPC in Spain and build a forecasting model capable of predicting its future values with high accuracy. The project focuses both on statistical rigor and interpretability.

## Dataset

- Source: **INE (Instituto Nacional de Estadística)**  
- Monthly IPC data from January 2002 to December 2023
- External variables considered: Energy price index, Food price index, and underlying inflation

## Methodology

The project follows these main steps:

### 1. Data Preparation
- Cleaning and formatting of raw data
- Creation of training and test partitions
- Generation of relevant external regressors

### 2. Exploratory Analysis
- Trend, seasonality, and stationarity analysis
- ACF and PACF plots to determine potential model structures
- Decomposition into trend, seasonal, and residual components

### 3. Model Building

- **ARIMA and SARIMA models**
  - Grid search for optimal (p,d,q) and (P,D,Q)s parameters
  - Residual diagnostics and Ljung-Box tests

- **ETS (Exponential Smoothing) models**
  - Model selection via information criteria (AIC, BIC)
  - Additive and multiplicative seasonal components tested

- **Dynamic regression models**
  - Incorporation of external variables (energy, food prices)
  - Pre-whitening and cross-correlation analysis

### 4. Model Evaluation

- Forecast accuracy metrics: RMSE, MAE, MAPE
- Evaluation on hold-out test set (last 24 months)
- Comparison of forecasting performance across models

## Results

- The final model selected was a **dynamic regression model with external variables**, achieving the best performance on the test set.
- Residuals were uncorrelated and homoscedastic.
- The model produced reliable forecasts consistent with recent inflationary trends in Spain.

## Technologies Used

- R (main language)
- `forecast`, `tseries`, `ggplot2`, `lmtest`, `zoo`, `urca`
- RMarkdown and LaTeX for report generation

## Files

- `IPC_TimeSeries_Analysis.Rmd`: Main code (RMarkdown)
- `IPC_Forecast_Report.pdf`: Final academic report (in Catalan)
- `data/`: Folder containing the preprocessed IPC data and regressors

## License

This repository is shared for academic and educational purposes. All rights reserved by the authors.

---

Developed by Matías Mora and Marc Cascant, 2025
