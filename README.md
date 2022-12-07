# Credit_Risk_Analysis

## Overview

A lender is seeking a predictive model of credit risk, specifically with regard to credit cards. The company will use Machine Learning to create an initial model using creditworthiness data from the peer-to-peer lending service LendingClub.

In general, the number of low risk loans outnumber the number of high risk loans. Due to the unbalanced nature of this problem several models were trained and evaluated to assess suitability.

## Results
A brief overview of the results for each model is shown below. This includes the generated balanced accuracy score, the confusion matrix, and the classification report.

### Naive Random Oversampling
Balanced Accuracy Score:
![](/assets/nro_ba.png)

Confusion Matrix:
![](/assets/nro_cf.png)

Classification Report:
![](/assets/nro_report.png)

### SMOTE Oversampling
Balanced Accuracy Score:
![](/assets/smote_ba.png)

Confusion Matrix:
![](/assets/smote_cf.png)

Classification Report:
![](/assets/smote_report.png)

### Cluster Centroid Undersampling
Balanced Accuracy Score:
![](/assets/cc_ba.png)

Confusion Matrix:
![](/assets/cc_cf.png)

Classification Report:
![](/assets/cc_report.png)

### SMOTEEN Combination
Balanced Accuracy Score:
![](/assets/st_ba.png)

Confusion Matrix:
![](/assets/st_cf.png)

Classification Report:
![](/assets/st_report.png)

### Balanced Random Forest Classifier
Balanced Accuracy Score:
![](/assets/brf_ba.png)

Confusion Matrix:
![](/assets/brf_cf.png)

Classification Report:
![](/assets/brf_report.png)

### Easy Ensemble AdaBoost Classifier
Balanced Accuracy Score:
![](/assets/eec_ba.png)

Confusion Matrix:
![](/assets/eec_cf.png)

Classification Report:
![](/assets/eec_report.png)


## Summary

Key information from the results above:
- The Easy Ensemble AdaBoost Classifier yielded the highest balanced accuracy score ~ 0.93.
- Naive Random Oversampling produced the lowest balanced accuracy score ~ 0.65. 
- The model with the highest precision (relative to detecting high risk borrowers) was Easy Ensemble with a precision of ~0.09.
- The model with the highest recall (relative to detecting high risk borrowers) was Easy Ensemble with a recall of ~0.92.

Assuming that the primary goal is maximize detection of high risk borrowers and minimize rejection of low risk borrowers the Easy Ensemble AdaBoost Classifier is the most suitable out of the six models tested. The high scores reported for this model could be a result of overfitting. To verify that it is the right choice, it should be evaluated on additional test data.
