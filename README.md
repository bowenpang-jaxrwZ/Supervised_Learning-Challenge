# Week20 Supervised Learning Challenge

## Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions
The instructions for this Challenge are divided into the following subsections:
* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Predict a Logistic Regression Model with Resampled Training Data
* Write a Credit Risk Analysis Report

## Split the Data into Training and Testing Sets
1. Read the ```lending_data.csv``` data from the Resources folder into a Pandas DataFrame.
2. Create the labels set (```y```) from the “loan_status” column, and then create the features (```X```) DataFrame from the remaining columns.
3. Note: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

##  Create a Logistic Regression Model with the Original Data
1. Fit a logistic regression model by using the training data (X_train and y_train).
2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
3. Evaluate the model’s performance by doing the following:
    * Calculate the accuracy score of the model.
    * Generate a confusion matrix.
    * Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Credit Risk Analysis Report
#### An overview of the analysis:
* The purpose of this analysis is to evaluate, evaluate and predict the creditworthiness of borrowers, which means the risk/healthy level of loans.
* The input of this model included the amount of the loan, interest rate, the income of the borrower, a debt to income ratio, number of accounts, derogatory marks, and the borrower's total debt.
* The model is built to predict if loans would be "healthy"(0) or "high-risk"(1) based on historical data we have on hand.
* The data was split into training and test sets(by default, ```train/test ratio``` is 75%:25%) and fit to a ```LogisticRegression model``` for analysis.
* We used the ```LogisticRegression model``` for analysis. On top of that, also increased the ```recall``` rate by implementing ```Resampling``` method to improve the imbalanced original dataset.

#### Results
* Machine Learning Model 1:
<br>

             precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619
<br>

* Machine Learning Model 2:
<br>

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619
<br>
With regard to Model 1 and 2: The logistic regression model using the original data does a amazing job of predicting the values for the healthy loans(0). The precision for the 1 class is 1.00 , meaning the model correctly made the positive prediction every time. The recall, which is the number of times the model correctly predicted a healthy transaction, is also great with 0.99 on predicting healthy loans. However, the model did not perform well on predicting the values for the high-risk loans(1). The precision rate was only 0.85 and 0.84 for model 1 and 2. The recall was only 0.91 in model 1, but improved largely in model 2. Overall, the logistic regression model generated pretty impressive numbers for the model predictions.

#### Summary
To summarize, the second model would be ideal when it comes to recommending the model usage by any company. For any business, it would be equally important to identify low AND high risk loans, which the second model did with 99% recall for both.


