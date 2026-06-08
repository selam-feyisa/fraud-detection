# Fraud Detection Project

## Overview
This project builds a machine learning system to detect fraudulent e-commerce transactions for Adey Innovations Inc.

## Dataset
- Fraud_Data.csv
- IpAddress_to_Country.csv
- creditcard.csv

## Work Completed (Task 1)

### Data Cleaning
- No missing values
- No duplicates
- Converted datetime columns

### Exploratory Data Analysis
- Fraud rate: 9.36%
- Dataset is highly imbalanced
- Purchase value, age, browser analysis performed

### Feature Engineering
- time_since_signup
- hour_of_day
- day_of_week

### Geolocation
- IP addresses mapped to countries
- 181 countries identified
- Fraud analysis by country completed

## Next Steps
- Train machine learning models
- Handle class imbalance using SMOTE
- Build Logistic Regression and XGBoost models
- Apply SHAP explainability

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook