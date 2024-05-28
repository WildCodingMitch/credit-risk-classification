# Module 12 Report

## Analysis Overview

The purpose of this analysis is to train and evaluate a model based on loan risk that can identify the creditworthiness of borrowers. The data included	loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, loan_status. These features were the basis of our predictions as to whether or not a loan is healthy or not. During this analysis I read in the data and divided the data based on whether the column was a label or feature. The only label is loan_status, so the rest were used as features. I then split the data using sklearn's train_test_split, using the split data I created and trained a Logistic Regression Model. Finally, I used this model to make predictions on the data to see how well the model performs with test data.

## Results

* Confusion Matrix:
  -   [[18663   102]
  -   [   56   563]]

* Classification Report:
  -                         precision   recall   f1-score  support

  -        0                  1.00      0.99      1.00     18765
  -        1                  0.85      0.91      0.88       619

  -        accuracy           --        --       0.99     19384
  -        macro avg          0.92      0.95     0.94     19384
  -        weighted avg       0.99      0.99     0.99     19384

## Summary

Overall the model performs well, by looking at the confusion matrix we can see that the number of Healthy Loans that were actually Non-Healthy Loans was 56, and the number of Non-Healthy Loans that were actually Healthy Loans was 102. Getting these numbers down would be key for this model. Also, after viewing the classification report, we can see that the model predicted healthy loans(0) 100% of the time and predicted non-healthy loans(1) 85% of the time. Although the model is performing well it is concerning that it is making 158 wrong predictions. More training and seeing more Non-Healthy Loans may improve the quality of the model, since the Healthy Loans heavily outweigh the Non-Healthy Loans in the provided dataset.

