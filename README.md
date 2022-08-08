# Module 12 Credit Risk Resampling

## Overview of the Analysis

The purpose of this analysis is to buid a model that can identify the credit worthiness of borrowers.

We were provided with a lending_data.csv which has financial information of borrower. 
* Loan amount, 
* Borrower’s income, 
* Debt to Income, 
* Total debt,
* No. Of accounts
* Loan_status = 0 ,1 

y feature for the model is loan_status. With the provided data, we can observe that there is class imbalance where records with loan_status =0 are 30 times more than the records with loan_status = 1

## Stage 1
The original data is splitted into training & testing data. The train data is used to train a Regression Model. Then the loan_status predictions were made using the trained model. The effectiveness of the model was then evaluated comparing the predictions & the test _data by generating accuracy score, confusion matrix & classification report

## Stage 2

The label data imbalance was addressed using the RandomOverSampler ( oversampling technique). The sampled data was then splitted into training & testing data. The  train data is used to train a Regression Model. Then the loan_status predictions were made using the trained model. The effectiveness of the model was then evaluated comparing the predictions & the test _data by generating accuracy score, confusion matrix & classification report.

## Results


Machine Learning Model 1:
  * The logistic regression model performs very well predicting the healthy loans with 100% precision and 99% recall. It has an overall accuracy of 95%. However because of class imbalance with less high risk loan data, the precision of high risk loan is 85% & recall is 91%.




Machine Learning Model 2:
  * Post traing the model with the balanced class data, the overall accuracy has improved from 95% to 99%. Using the oversampled data has improved the recall for high-risk loans from 91% to 99% percent which is desired feature for such usecases.


## Summary

Comparing the results from 2 models, I would suggest using the second model which includes Random Oversampling. The overall accuracy is better for this model  with significant improvement in recall(false negatives) from 91% to 99%.

