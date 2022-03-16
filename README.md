# Zillow-Housing-Prices-Time-Series-Analysis
Forecasting the Median Sold Prices for Zillow Housing Data using historical prices and exogenous variables

# Introduction
House price has a great impact on everyone’s life. The goal of this report is to research how we can predict the median future sold price for housing in California based on time series models. Here, we are using the Zillow dataset recorded Feb 2008- Dec 2015 monthly as our training set, including median sold price for housing in California, median mortgage rate, and unemployment rate, and trying to predict the Jan- Dec 2016 median sold price for housing in California.

# About the Data

The dataset consists of 95 observations with 4 columns:
  - Date gives information about the date of each record.
  - MedianSoldPrice gives information on the median sold price of houses in California.
  - MedianMortageRate is the median mortgage rate of the houses.
  - UnemploymentRate is the unemployment rate for that month.

# Overview of Methodology

- Step 1: Initial Data Exploration
  - Testing for stationarity
  - Differencing and Decomposition
- Modelling
  - ARIMA Family
    - ARIMA Models
    - SARIMA Models  
    - SARIMAX Models
  - Exponential Smoothening Methods
  - Prophet model
- Cross Validation and Fine Tuning Models 
- Best Model
- Predictions
- Final Error Calculation
- Results  

# Conclusion
We attempt to predict the Median Housing Prices for the near future using the history data and exogenous variables. From our initial exploratory analysis, we find that the time series data shows an obvious trend. Some seasonality can be seen towards the later half of the data.
For our analysis, we used a variety of candidate time series forecasting models ranging from ARIMA family to prophet. For initial univariate analysis, we start with low complexity models by just considering simple ARIMA models with only trend components and no seasonality. We selected the
best candidate models with and without seasonality using different information criteria. Comparing the one-step cross validation RMSE of each of these candidate models, we found that ARIMA(3,1,0)(1,0,1)[12] is our best model for the univariate ARIMA family. Next, we performed a similar procedure for Exponential Smoothing models. We considered all the possible combinations for trend and seasonality and we found that the Exponential Smoothing model with Multiplicative trend and no seasonality gives the best cross validation RMSE. We did not get good cross-validation results for the Prophet model. This is expected since the Prophet model is not ideal for time series data with monthly frequency.
Next, we analysed SARIMA models with different combinations of exogenous variables. On comparing the cross-validation RMSE, we found that SARIMAX(2,0,0),(0,1,2)[12] with Unemployment rate as the exogenous variable gives the best results. Comparing the cross-validation RMSE values for our best models from different cases, we find that SARIMAX(2,0,0),(0,1,2)[12] has the lowest RMSE and hence we chose it as our best model. On the test data, we get a prediction RMSE value of 9596.31for our best model.
