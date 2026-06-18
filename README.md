# Fraud Detection - 10 Academy Week 5&6

## Project Overview
End-to-end fraud detection system for e-commerce and bank transactions.

## Task 1: Data Analysis and Preprocessing (Completed)

### Data Cleaning
- No missing values or duplicates in both datasets.
- Converted timestamps to datetime.

### Exploratory Data Analysis
- Fraud rate in e-commerce: ~9.36%
- Fraud rate in credit card: ~0.17% (highly imbalanced)
- Visualizations saved in notebooks/

### Geolocation Integration
- Converted IP addresses to integer.
- Used `pd.merge_asof` to map IPs to countries.

### Feature Engineering (Fraud_Data)
- `time_since_signup` (in hours)
- `hour_of_day`, `day_of_week`
- Country from IP range

### Data Transformation
- StandardScaler for numerical features
- One-hot encoding for categorical features (source, browser, sex, country)

### Class Imbalance Handling
- Used **SMOTE** on training set only (justified because dataset is highly imbalanced).
- Before SMOTE (Fraud): 109568 legitimate vs 11321 fraud
- After SMOTE: 109568 vs 109568

## Repository Structure
Follows the required structure.

## How to Reproduce
```bash
pip install -r requirements.txt
jupyter notebook notebooks/feature-engineering.ipynb
 ## Task 2: Model Building & Training (Completed)

- **Baseline**: Logistic Regression
- **Best Model**: XGBoost
- Primary Metrics: **AUC-PR** and **F1-Score** (suitable for imbalanced data)

## Task 3: Model Explainability

- Used SHAP for interpretability
- Top features: `time_since_signup`, `purchase_value`, `hour_of_day`, etc.
- Visualizations saved in notebooks/

## Business Recommendations
1. Flag transactions with very low `time_since_signup` (< 1 hour) for extra verification.
2. Monitor high `purchase_value` at unusual hours.
3. Add country-based risk scoring.

## Final Submission Files
- Comprehensive README
- Clean project structure
- modeling.ipynb + shap-explainability.ipynb