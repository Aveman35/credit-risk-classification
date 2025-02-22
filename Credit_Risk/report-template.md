# Module 12 Report

## Overview of the Analysis

The purpose of this analysis was to create a machine learning model that could identify the creditworthiness of borrowers for a peer-to-peer lending services company.

The data used to train the model had 77,536 unique rows of data, each containing a loan and corresponding details. Each row contained information about the loan itself and the borrower, including loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and loan status.

The 'loan_status' column contained values 0 or 1, indicating a healthy loan (0) or a high risk of defaulting (1). This data was crucial in training the model to learn the relationship between the other columns of data, and the loan_status.

The first steps to create the model was to load the lending_data.csv file from the 'Resources' folder into a Pandas DataFrame. From there the 'loan_status' column was seperated to be the y variable for testing and training, then the remaining columns were used to create the X variable for testing and training. The X and y variables were then split into training and testing datasets using the 'train_test_split' module.
Using the 'LogisticRegression' module, a model was created and fit with the training data. Predictions were made using the X_test variable on the model, then a 'confusion_matrix' was introduced using the predictions and y_test variables. Finally a 'classification_report' was generated to display the results of the testing model.


## Results
Machine Learning Model 1:

    Precision scores
    * Healthy loan 1.00
    * High risk 0.87

    Recall scores
    * Healthy loan 1.00
    * High risk 0.95

    Accuracy of 0.99
   

## Summary


This machine learning module performed well, with high accuracy for determining healthy loans and high risk loans.

Room for improvement would be increasing the precision values for determining High risk loans, ideally improving it until it is over 0.90. It could be said this would be a good model to implement for ensuring if a loan will stay healthy, and could use improvement before fully being utilized to predict High risk loans.
