# Credit Risk Classification

## Overview of the Analysis

The goal of this project is to build a machine learning model that can predict the credit risk of loan applicants using historical financial data. This analysis is essential for lenders and peer-to-peer lending companies that want to assess the likelihood that a borrower will repay a loan.

The dataset includes information such as:
- Borrower income
- Debt-to-income ratio
- Loan amount
- Number of financial accounts

The target variable is `loan_status`, which has two classes:
- `0` indicates a **healthy loan**
- `1` indicates a **high-risk loan**

The stages of the machine learning process in this analysis were:
1. Reading and exploring the dataset (`lending_data.csv`)
2. Splitting the data into features (`X`) and labels (`y`)
3. Splitting the dataset into training and testing sets
4. Training a **Logistic Regression** model
5. Making predictions and evaluating model performance using a **confusion matrix** and **classification report**

## Results

### Machine Learning Model 1: Logistic Regression

- **Accuracy Score:** 0.99  
- **Precision Score:**
  - Class 0 (Healthy Loans): 1.00
  - Class 1 (High-Risk Loans): 0.84
- **Recall Score:**
  - Class 0 (Healthy Loans): 0.99
  - Class 1 (High-Risk Loans): 0.94


## Summary

The Logistic Regression model performed well in predicting healthy loans, achieving perfect precision for class `0` and a high recall. This means the model is highly reliable in identifying loans that are unlikely to default.

However, while the model is reasonably good at identifying high-risk loans (class `1`), it is not perfect. It still misclassifies some risky loans as healthy, which could lead to poor lending decisions.

### Recommendation:
- **Use with caution.** The model is acceptable for identifying low-risk loans but may need improvement for detecting high-risk ones.


