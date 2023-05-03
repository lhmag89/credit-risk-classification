# credit-risk-classification

## Analysis

The purpose of this analysis is to develop a classification model that uses lending data to label loans as healthy or high-risk. The lending data includes loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt and the loan status (healthy or high-risk). The data contained 75036 "healthy loans" and 2500 "high-risk loans" that were split into training and testing sets. The training sets were used to fit a logistic regression model. Predictions were made with the model and checked against the actual values to generate a balanced accuracy score, confusion matrix and classification report. A second logistic regression model was developed. This time, RandomOverSampler was used to try to address the imbalance in loan status. The logistic regression model was fitted with the new resampling data. Predictions were made with the new model and the same steps were taken to generate a balanced accuracy score, confusion matrix and classification report.

## Results

* Logistic Regression Model 1:
  * Balanced Accuracy Score: 0.952
  * Healthy Loans - Precision: 1.00, Recall: 0.99, F1-Score: 1.00
  * High-Risk Loans - Precision: 0.85, Recall: 0.91, F1-Score: 0.88

* Logistic Regression Model 2 (with RandomOverSampler):
  * Balanced Accuracy Score: 0.994
  * Healthy Loans - Precision: 1.00, Recall: 0.99, F1-Score: 1.00
  * High-Risk Loans - Precision: 0.84, Recall: 0.99, F1-Score: 0.91

## Summary

#### Model 1

The model has a good balanced accuracy score of 0.95. The f1-scores suggest the model is very good for healthy loans and good for high-risk loans. Of the loans that the model predicted would be healthy, >99% were healthy loans. Of the loans that were actually healthy, the model predicted 99% of them correctly. Of the loans that the model predicted would be high risk, 85% were high-risk. Of the loans that were actually high-risk, 91% were correctly predicted. The model like does a better job of classifying healthy loans due to the sample imbalance. The recommendation would be to improve the model since 9% misclassification of high-risk loans seems a bit high.

#### Model 2

The model has a very good balanced accuracy score of 0.99. The f1-scores suggest the model is very good for both healthy and high-risk loans. Of the loans that the model predicted would be healthy, >99% were healthy loans. Of the loans that were actually healthy, the model predicted 99% of them correctly. Of the loans that the model predicted would be high risk, 84% were high-risk. Of the loans that were actually high-risk, 99% were correctly predicted. This model likely does a better job than the previous model of classifying loans as a result of oversampling to improve the sample imbalance. In particular, there is now only a 1% misclassfication of high-risk loans as healthy loans. 

#### Recommendation

For this classification problem, the worst case would be to label a high-risk loan as healthy. The performance metric needed here is the recall value for predicting high-risk loans. Since the second model has a recall value of 0.99, that model was able to label 99% of the actual high-risk loans as high-risk. 
The recommendation would be to use this new model since 1% misclassification of high-risk loans seems reasonable.

## Technologies
Python, Jupyter, Pandas, numpy, pathlib, sklearn, imblearn, RandomOverSampler, collections, Counter

## Contributors
Developed by Luis Hernandez Email: lhernandez.mag.89@gmail.com

## License
UC Berkeley Extension Data Analytics Program
