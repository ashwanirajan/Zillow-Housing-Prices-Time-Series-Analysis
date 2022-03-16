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
