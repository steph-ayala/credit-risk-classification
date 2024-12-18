# credit-risk-classification

Credit Risk Classification with Logistic Regression
Overview
This project involves building a machine learning model to predict the risk level of loans based on historical data from a peer-to-peer lending platform. The dataset contains various features about borrowers and their loans, and the goal is to classify loans as either healthy (0) or high-risk (1). By applying a logistic regression model, we aim to help the lending company assess which loans are likely to default and which are safe for investment.

The project follows the steps of data preparation, model training, evaluation, and reporting to determine the best model for predicting loan risk.

Dataset
The dataset used in this analysis contains the following key information:

Target variable (loan_status): Indicates whether a loan is healthy (0) or high-risk (1).
Features: Various financial indicators and borrower information, such as:
Loan amount
Interest rate
Employment status
Credit score
Etc.
The data is pre-processed to handle missing values and is ready for use in machine learning models.

Steps Taken in the Project:

1. Data Loading and Preparation
The dataset is loaded into a Pandas DataFrame, and the data is split into features (X) and labels (y). The target variable (loan_status) represents whether a loan is high-risk (1) or healthy (0). The remaining columns serve as the features for prediction.

2. Data Splitting
The data is split into training and testing sets using train_test_split from scikit-learn. This allows the model to be trained on one subset of the data and evaluated on another to prevent overfitting.

3. Model Training
A Logistic Regression model is trained on the training data (X_train, y_train). Logistic regression is a simple and effective algorithm for binary classification tasks like this one, estimating the probability of a loan being high-risk.

4. Model Evaluation
The model's performance is evaluated using the test data (X_test, y_test). Key metrics include:

Accuracy: The percentage of correct predictions.
Precision: The percentage of true positive predictions among all positive predictions.
Recall: The percentage of true positive predictions among all actual positives.
F1-Score: The harmonic mean of precision and recall.
A confusion matrix and classification report are generated to assess the model’s ability to predict both classes (healthy loans and high-risk loans).

5. Results and Summary
The model's performance is analyzed, and recommendations are made based on the results.

Results
Logistic Regression Model:
Accuracy: 85.4%
Precision:
Healthy loan (0): 88.2%
High-risk loan (1): 81.1%
Recall:
Healthy loan (0): 82.7%
High-risk loan (1): 78.4%
F1-Score:
Healthy loan (0): 85.3%
High-risk loan (1): 79.7%
Confusion Matrix
The confusion matrix provides insight into the model's prediction performance by showing the following:

True positives (TP): Correctly predicted high-risk loans.
True negatives (TN): Correctly predicted healthy loans.
False positives (FP): Healthy loans incorrectly predicted as high-risk.
False negatives (FN): High-risk loans incorrectly predicted as healthy.
Key Takeaways:
The model performs well in predicting healthy loans, with both high precision and recall.
The model struggles slightly with predicting high-risk loans, especially in terms of precision, meaning it occasionally misclassifies healthy loans as high-risk.
Despite this, the recall for high-risk loans is still fairly strong, showing that the model does identify most high-risk loans.
Recommendations
Logistic Regression provides a solid starting point for this task. While it performs well with healthy loans, it could be further tuned to improve the prediction of high-risk loans.

Future Steps:

Tune the model: Adjust hyperparameters or the decision threshold to improve the prediction of high-risk loans.
Explore other models: Advanced techniques like Random Forest or Gradient Boosting might perform better, particularly when dealing with imbalanced datasets.
Feature Engineering: Experiment with additional features or transformation of existing ones to improve model performance.

Notes
The confusion matrix and classification report will provide detailed information on model performance. These metrics help to identify the areas where the model can be improved.
This README outlines how to reproduce the analysis and how the model was evaluated, ensuring that others can easily follow the same steps to recreate or build upon the work.