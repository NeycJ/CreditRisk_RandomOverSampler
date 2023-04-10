## CreditRisk_RandomOverSampler
Supervised Learning_model train

* Purpose of the analysis.
This analysis is to identify the creditworthiness of borrowers.  Healthy Loans usually outweigh high-risk loans I need to create a model to be sure the data is near balanced.

* Financial information the data was on, and what you needed to predict.
The loan size, interest rate, borrower income, debt to income, number of account, derogatory marks, and total debt as a financial picture for each borrower.  I needed to predict which loans are risky. 

* Basic information about the variables you were trying to predict (e.g., `value_counts`).
Healthy loans(0) = 75036 
High Risk loans(1) = 2500

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
The stages of my Machine Learning analysis process:
Trained, test, split.
Instantiated Logistic Regression Model to train and test the data.
Created a new dataframe to split the data.
Balanced accuracy to check if my data is highly imbalanced.
Created a Confusion Matrix to identify positive, false positive, negative, and false negatives.
Printed Classification report to see how well the Logistic Regression model predicted both healthy and high-risk loans.

I repeated the above steps for the second model which used Logistic Regression with a Random Over Sampler model to train the data.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
                pre       rec       spe        f1       geo       iba       sup

  0_Healthy       1.00      0.99      0.91      1.00      0.95      0.91     18765
1_High-Risk       0.85      0.91      0.99      0.88      0.95      0.90       619

avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
                 pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?  
The Random Over Sampler with Log regression performed best with a .99, an almost perfect result in all scores in Classification Report.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )  
It's worth trying to predict the number of high-risk loans.

If you do not recommend any of the models, please justify your reasoning.

