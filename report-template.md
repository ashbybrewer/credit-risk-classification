# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to use machine learning to to determine which loans are healthy (low-risk) or non-healthy (hihgh_risk) based on the loan status provided by the lending company. 
Using the dataset provided by the lending company, I created a Logistic Regression Model that generated an accuracy score of 95%. Although the model generated a high-accuracy, the models recall value (0.91) for non-healthy loans is lower than the recall value (0.99) for healthy loans. This indicates that the model will predict loan status's as healthy better than being able to predict loan status's as non-healthy. This is due to the dataset being imbalanced. You can see the impbalance in the python notbook around step 3, where we do a value count. 

Since there's an imbalance, we'll try to normalize it and imporove the model by balancing it. To do this we used the oversampler. 

We used a logistic regression model that's balanced and imbalanced, and compare accurancy to see if the model improved with balanacing. 

According to the confusion matrix in step 3 [Create a LRM w/ Resampled(oversampled) Data]:

Out of the 18,765 loan status's that are healthy, the model predicted 18,649 as healthy correctly and 116 as healthy incorrectly.

Out of the 619 loan status's that are non-healthy (high-risk), the model predicted 615 as non-healthy correctly and 4 as non-healthy incorrectly.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
The Logistic Regression model fitted with the Imbalanced DataSet predicted healthy loans 100% of the time and predicted non-healthy loans 85% of the time.

The model generated an accuracy score of 95% but could be improved due to the dataset being imbalanced.
According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 9% of mistakes when predicted non-healthy loans.

The model fitted with imbalanced data has a higher possibility of making these mistakes:

  -a healthy loan (low-risk) is classified as a non-healthy loan (high-risk).
  -a non-healthy loan (high-risk) is classified as a healthy loan (low-risk).



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

The model generated an accuracy score of 99% due to the dataset being balanced.
According to the models recall scores, the model made 1% of mistakes when predicting healthy loans and made 1% of mistakes when predicted non-healthy loans.

The model fitted with balanced (oversampled) data has a much lower possibility of making these mistakes:

a healthy loan (low-risk) is classified as a non-healthy loan (high-risk).
a non-healthy loan (high-risk) is classified as a healthy loan (low-risk).
## Summary
The regression model with the overfitted data perfomred much better than the imblanced data due to the data being balanced. This results in a higher accuracy score and a higher recall. This indicates fewer mistakes. 

Model fitted with Imbalanced Data:

56 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

102 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy


Model fitted with Balanced Data:

4 (FALSE POSITIVES) --> The actual value is healthy and the predicted value is non-healthy

116 (FALSE NEGATIVES) --> The actual value is non-healthy and the predicted value is healthy

According to the confusion matrices, the number of False Postives drastically decreases indicating the model will classify healthy & non-healthy loans correctly. Based off of this analysis, I would recommend using Model 2: "Logistic Regression Model fitted with Balanced (oversampled) data."