# credit-risk-classification

## Overview of the Analysis

The purpose of this challenge was to use various techniques to train and evaluate a model based on loan risk. This was used to build a model that can identify the creditworthiness of borrowers. 

The data used is made up of historical lending activity from a peer-to-peer lending services company.

The target for this analysis was 'loan_status'.

Features considered in the analysis included data on:
<ul><li>Loan amount
<li>Interest rate
<li>Borrower income
<li>Ratio of debt to income
<li>Number of accounts owned by the borrower
<li>Whether the borrower has any 'derogatory marks'
<li>Total debt</ul>

I split the data into testing and training sets, then used the training set to build a model based on logistic linear regression.

I then applied this model to the testing data to establish its performance and effectiveness as a model.

Next, I resampled the data with the RandomOverSampler module from the imbalanced-learn library and used this to fit the model and make predictions. I again looked at the performance and effectiveness of this model fit with the oversampled data.

## Results

* Machine Learning Model 1:
  <ul><li>Accuracy: 99%
  <li>Precision: 94% (100% for 0 or 'healthy loans'; 87% for 1 or 'high risk loans')
  <li>Recall: 94% (100% for 0 or 'healthy loans'; 89% for 1 or 'high risk loans')</ul>

* Machine Learning Model 2:
  <ul><li>Accuracy: 100%
  <li>Precision: 94% (100% for 0 or 'healthy loans'; 87% for 1 or 'high risk loans')
  <li>Recall: 100% (100% for 0 or 'healthy loans'; 100% for 1 or 'high risk loans')</ul>

## Summary

Model 2 seems to perform slightly better than model 1, with an overall accuracy score of 100%, compared to 99%. This is a very slight difference though. 

In terms of false positives - or predicting a safe loan that is actually high risk - the chance of these is not a concern as both models have 100% accuracy in predicting healthy loans.

However, both models have an accuracy for high risk loans below 90%. 87-89% may seem like a good precision score, but given the seriousness of these decisions, and the potential for this to prejudice people's ability to access finances they need, I believe accuracy in this area is more important than in the healthy loans. Therefore, I would want to see a higher score for this.

## Requirements
<ul><li>Split the Data into Training and Testing Sets (30 points)
<li>Create a Logistic Regression Model (30 points)
<li>Write a Credit Risk Analysis Report (20 points)
<li>Coding Conventions and Formatting (10 points)
<li>Code Comments (10 points)</ul>
