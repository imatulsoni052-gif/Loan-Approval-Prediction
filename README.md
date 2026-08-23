# Loan Approval Prediction using Machine Learning

A machine learning project that predicts loan approval outcomes with 92.7% accuracy, aimed at helping lenders make faster and more consistent credit decisions.
## Overview

Financial institutions process a large volume of loan applications every day, and manual evaluation is often slow, inconsistent, and expensive. This project uses machine learning to automate the loan approval decision by analyzing an applicant's financial, credit, and asset details. The goal is to identify creditworthy applicants while reducing lending risk and speeding up the approval process.
## Business Problem

Lenders need a way to:
- Evaluate applicants quickly and consistently
- Reduce the risk of loan defaults
- Cut down on manual screening effort
- Make approval decisions that are backed by data rather than guesswork

This project addresses these needs using a Logistic Regression-based predictive model.
## Dataset Features

The model is trained on applicant information including:
- Number of dependents
- Education level
- Self-employment status
- Annual income
- Loan amount and loan term
- CIBIL score
- Residential, commercial, and luxury asset values
- Bank asset value

Target variable: Loan Status (Approved / Rejected)
## Project Workflow

1. Data collection
2. Data cleaning and preprocessing
3. Exploratory Data Analysis (EDA)
4. Feature engineering
5. Train-test split (80:20)
6. Feature scaling
7. Logistic Regression modeling
8. Model evaluation
## Exploratory Data Analysis - Key Insights

- Around 62% of applications in the dataset were approved
- Most loan requests were below ₹2 crore
- CIBIL scores ranged from 300 to 900
- Income alone did not turn out to be a strong predictor of approval - it needed to be considered alongside other factors
## Feature Engineering

Two additional features were engineered to improve the model's ability to assess risk:

- Debt-to-Income Ratio - captures how much of an applicant's income is already committed to existing debt
- Total Assets - combines residential, commercial, luxury, and bank asset values into a single measure of financial strength

Adding these made the model both more interpretable and better at distinguishing risk levels.
## Model

Algorithm: Logistic Regression

Configuration:
- 80:20 train-test split
- Feature normalization using StandardScaler
- Balanced class handling
- Binary classification output (Approved / Rejected)

## Results

Metric      Score
Accuracy    92.7%
ROC-AUC     96.6%
Precision   High
F1 Score    Strong

The model performs well at separating approved applications from rejected ones, with credit score, income, and debt-to-income ratio emerging as the strongest predictors.

## Business Impact

- Speeds up loan eligibility screening
- Helps flag high-risk applicants earlier in the process
- Supports more consistent, data-backed lending decisions
- Reduces the manual workload involved in initial screening

## What I'd Explore Next

- Bringing in employment history and past repayment behavior as additional features
- Testing tree-based models like Random Forest and XGBoost for comparison
- Deploying the model as a simple web application for real-time predictions
- Setting up a process to monitor and retrain the model over time

## Tech Stack

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook

## Repository Structure

loan-approval-prediction/
│
├── loan_approval_dataset.csv       # Dataset used for training/testing
├── loan_approval_prediction.py     # Main project script
├── loan_approval_model.pkl         # Saved trained model
├── scaler.pkl                      # Saved feature scaler
├── README.md                       # Project documentation
└── images/
    ├── loan_status_distribution.png
    ├── cibil_score_distribution.png
    ├── correlation_heatmap.png
    ├── confusion_matrix.png
    └── roc_curve.png

## How to Run

git clone https://github.com/imatulsoni052-gif/loan-approval-prediction.git
cd loan-approval-prediction
pip install -r requirements.txt
python loan_approval_prediction.py

## About

Built by Atul Soni as part of a data analytics portfolio project.

Portfolio: https://www.wscubetech.com/portfolio/data/atul-soni-8nrpnp1
GitHub: https://github.com/imatulsoni052-gif
LinkedIn: https://www.linkedin.com/in/atul-soni-ab4638393/

If you find this project useful, feel free to star the repository.
