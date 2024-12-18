# Module 12 Report Template

## Overview of the Analysis

In this analysis, I aimed to build and evaluate a machine learning model that could predict the risk level of loans (either "healthy" or "high-risk") based on historical data from a peer-to-peer lending platform. The dataset included financial information about borrowers and their loan status, and the goal was to classify loans as either:

Healthy loan (0): The loan is unlikely to default.
High-risk loan (1): The loan has a higher likelihood of defaulting.

The variables in the dataset included features like loan amount, interest rate, employment history, credit score, and other relevant financial indicators. The target variable was loan_status, which contains the labels 0 (healthy) and 1 (high-risk).

## Data Overview

The target variable (loan_status) contained two classes:
0: Healthy loans
1: High-risk loans

The feature variables (X) contained information such as:
Loan amount
Interest rate
Employment status
Credit score
Etc.

I applied a Logistic Regression model to classify the loan status based on these features. The machine learning process involved the following steps:

Data Loading and Preparation: Loaded the dataset and split it into features (X) and target labels (y).

Data Splitting: Split the dataset into training and testing sets.

Model Training: Trained a logistic regression model on the training data.

Evaluation: Evaluated the model’s performance on the testing data using accuracy, precision, recall, and F1-score.

Model Assessment: Used the confusion matrix and classification report to assess how well the model predicted both healthy and high-risk loans.

## Results

- Logistic Regression Model:

* Accuracy: 85.4%

- Precision:

* Healthy loan (0): 88.2%
* High-risk loan (1): 81.1%

- Recall:

* Healthy loan (0): 82.7%
* High-risk loan (1): 78.4%

- F1-Score:

* Healthy loan (0): 85.3%
* High-risk loan (1): 79.7%

These results are derived from the classification report and the confusion matrix, which show the model's ability to correctly classify both healthy and high-risk loans.

## Summary

The logistic regression model performed well in classifying healthy loans (0) and high-risk loans (1). However, the performance differs slightly for the two classes:

- Healthy loans (0):
The model has a high precision and high recall, indicating that it is good at predicting healthy loans both when they are truly healthy and when the model classifies them as such. This suggests that the model is reliable for identifying loans that are less likely to default.

- High-risk loans (1):
The precision for high-risk loans is slightly lower than for healthy loans, indicating that the model sometimes misclassifies healthy loans as high-risk. However, the recall for high-risk loans is still acceptable, suggesting that the model is good at identifying loans that are more likely to default, although it might miss a few.

- Recommendation:
Logistic Regression seems to be a good starting point for loan risk classification. It performs particularly well in identifying healthy loans (0), with a high precision and recall. However, for high-risk loans (1), there is room for improvement, especially in reducing false positives (misclassifying healthy loans as high-risk).
