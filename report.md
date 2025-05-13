# Module 20

# Credit Risk Classification

## Overview of the Analysis

The purpose of this analysis is to build a machine learning model that can predict the credit risk of loan applicants based on historical financial data. This is crucial for financial institutions, such as peer-to-peer lending platforms, to minimize risk and make informed lending decisions.

The dataset used in this analysis includes various financial metrics for loan applicants, such as their income, debt-to-income ratio, loan size, and number of accounts. The primary goal was to predict whether a loan would be "healthy" (safe) or "high-risk" (likely to default), based on the `loan_status` column:

* `0` – Healthy loan  
* `1` – High-risk loan

The machine learning process included the following stages:
- Reading and exploring the dataset.
- Splitting the data into features (`X`) and labels (`y`).
- Splitting the dataset into training and testing sets using `train_test_split`.
- Creating and fitting a Logistic Regression model (`LogisticRegression`) using the training data.
- Generating predictions and evaluating model performance with a confusion matrix and classification report.

## Results

* **Machine Learning Model 1: Logistic Regression**
  * **Accuracy Score:** 0.99
  * **Precision Score:**
    * Class 0 (Healthy Loans): 1.00
    * Class 1 (High-Risk Loans): 0.84
  * **Recall Score:**
    * Class 0 (Healthy Loans): 0.99
    * Class 1 (High-Risk Loans): 0.94


## Summary

The logistic regression model demonstrated strong overall performance, with an accuracy of 99%. It is highly precise in identifying healthy loans and performs moderately well when detecting high-risk loans. However, there is still room for improvement in predicting high-risk loans, as missing them could result in financial losses.

Whether the model is suitable for deployment depends on the business priorities. If the goal is to minimize defaults, the recall for class `1` (high-risk loans) becomes crucial. Since the recall for high-risk loans isn't perfect, we recommend further improvements such as:
- Using more advanced models (e.g., Random Forest, XGBoost)
- Performing feature engineering or resampling (e.g., SMOTE)

At this stage, the model may be used with caution to help identify safe loans, but it should not be relied upon solely to detect high-risk applicants without enhancements.

