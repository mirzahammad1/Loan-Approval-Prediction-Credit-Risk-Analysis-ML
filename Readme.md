# Loan Approval Prediction & Credit Risk Analysis

## Business Problem
Banks receive thousands of loan applications every month and must balance growth with risk.
This project aims to analyze historical loan application data to understand approval drivers
and build a predictive model that estimates the probability of loan approval.

The solution is designed to support underwriting decisions while remaining transparent and explainable.

---

## Dataset Overview
The dataset contains historical personal loan applications with a binary target variable:

- **LoanApproved**
  - 1 → Approved
  - 0 → Declined

Features include:
- Applicant demographics
- Income and debt metrics
- Credit score and default history
- Loan request characteristics

---

## Approach & Methodology

### Data Cleaning
- Validated data types and ranges
- Removed duplicate records
- Handled missing values using median/mode imputation
- Ensured logical constraints on financial variables

### Exploratory Data Analysis (EDA)
- Analyzed overall loan approval rates
- Studied approval trends by employment status, education, home ownership, and loan purpose
- Evaluated risk factors such as credit score, debt-to-income ratio, and previous defaults
- Identified high-risk applicant segments

### Modeling
Three machine learning models were trained and compared:
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest

Techniques used:
- Train/test split
- Cross-validation
- Hyperparameter tuning with GridSearchCV

---

## Model Evaluation
Models were evaluated using:
- ROC-AUC
- Precision-Recall AUC
- Confusion Matrix
- Classification Report

Random Forest achieved the best overall performance and was selected as the final model.

---

## Interpretability & Insights
- Credit score is the strongest predictor of loan approval.
- High debt-to-income ratios significantly reduce approval probability.
- Previous defaults are a major risk indicator.
- Partial dependence plots confirm intuitive and policy-aligned model behavior.

---

## Final Model Performance
| Model | ROC-AUC | PR-AUC |
|------|--------|--------|
| KNN | Moderate | Moderate |
| Decision Tree | Good | Good |
| **Random Forest** | **Best** | **Best** |

---

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
