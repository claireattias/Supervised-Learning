# Module 12 Report

## Analysis

The purpose of this analysis is to evaluate the quality of the logistic regression models and determine how the model can ultimately affect how the bank distributes loans based on risk. The data given identified if individuals have a healthy loan status or a high risk loan status based on loan size, interest rate, borrower income, and debt. The logistic regression model will predict the loan status for individuals in binary outcomes. A value of 0 means the loan is healthy and a value of 1 means the loan has a high risk of defaulting. The data provided identifies 75,036 records of healthy loan status and 2,500 records of high risk loans. Since the data is continuous, a logistic regression model was generated using machine learning. After separating the data into labels and features, the data was split into training and testing datasets. A logistic regression model was then created and fit using training data, then used to make predictions. The quality of these predictions were assessed using a confusion matrix and a classification report. The data was resampled to ensure an equal number of healthy loans and high risk loans. 


## Results

Accuracy: how often the model is correct - the ratio of correctly predicted observations to the total number of observations 
Precision: the ratio of correctly predicted positive observations to the total predicted positive observations 
Recall: the ratio of correctly predicted positive observations to all predicted observations for that class

* Machine Learning Model 1:
  - 99% accuracy 
  - healthy loans: 1.00 precision, high risk loans: 0.85 precision 
  - health loans: 0.99 recall, high risk loans: 0.91 recall (56 false negative, 102 false positives)

* Machine Learning Model 2:
  - 99% accuracy 
  - healthy loans: 1.00 precision, high risk loans: 0.84 precision 
  - healthy loans: 0.99 recall, high risk loans: 0.99 recall (4 false negatives, 116 false positives)

## Summary

The accuracy of both models was 99%, but the recall improved significantly in the second model with resampled data. The first model did an excellent job predicting a healthy loan status, but a poor job predicting a high risk status. The second model did a much better job predicting high risk loans. The improvement is apparent in the decrease in false negatives (56 to 4). This means the first model incorrectly identified 56 high risk loans as healthy. There was an increase in false positives (102 to 116), meaning the second model incorrectly identified 116 health loans as high risk. While this is not ideal, it is more important to correctly identify the high risk loans because these are the ones that can potentially be more costly to the bank. Therefore, I would recommend the second model. 
