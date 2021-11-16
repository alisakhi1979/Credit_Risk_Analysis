# Credit_Risk_Analysis

## A) Overview:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, there is need to employ different techniques to train and evaluate models with unbalanced classes. This analysis uses the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data is oversampled using the RandomOverSampler and SMOTE algorithms, and undersample using the ClusterCentroids algorithm. Further, combinatorial approach of over- and undersampling using the SMOTEENN algorithm is applied and two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier is applied to predict credit risk. 

A comparison analysis of the performance of afore-mentioned models and a written recommendation on whether they should be used to predict credit risk is presented.

## B) Resources:
- Data Source: LoanStats_2019Q1.csv
- Software: Python (mbalanced-learn and scikit-learn libraries)

## C) Results:

1. Naive Random Oversampling:
    * Balanced Accuracy Score: 64%
    * high_risk 
        * Percision: 1%
        * Recall score (f1): 2%
    * low_risk
        * Percision: 100 %
        * Recall score (f1): 79%

2. SMOTE Oversampling:
    * Balanced Accuracy Score: 66%
    * high_risk
        * Percision: 1%
        * Recall score (f1): 2%
    * low_risk:
        * Percision: 100%
        * Recall score (f1): 82%

3. Cluster Centroids Undersampling:
    * Balanced Accuracy Score: 54%
    * high_risk 
        * Percision: 1%
        * Recall score (f1): 1%
    * low_risk
        * Percision: 100 %
        * Recall score (f1): 57%

4. Combination (Over and Under) Sampling:
    * Balanced Accuracy Score: 64%
    * high_risk
        * Percision: 1%
        * Recall score (f1): 2%
    * low_risk
        * Percision: 100%
        * Recall score (f1): 72%

5. Balanced Random Forest Classifier:
    * Balanced Accuracy Score: 78%
    * high_risk
        * Percision: 4%
        * Recall score (f1): 7%
    * low_risk:
        * Percision: 100%
        * Recall score (f1): 95%

6. Easy Ensemble AdaBoost Classifier:
    * Balanced Accuracy Score: 92%
    * high_risk
        * Percision: 7%
        * Recall score (f1): 14%
    * low_risk
        * Percision: 100%
        * Recall score (f1): 97%

## D) Summary:

In all models, except for Easy Ensemble AdaBoost Classifier, the balanced accuracy score is relatively low for performing credit analysis and segregating the risk of the prospect clients. Easy Ensemble AdaBoost Classifier model, however, has achieved 92 % balanced accuracy score which is remarkable for a predictive model. This model has slightly improved the Percision and Recall for the high_risk applicants and achieved score of 7% for percision and 14% recall. However, the level of percision is still very low and can not be accepted as a predictive model to be utilized in the business context. There is a risk of labeling many low risk applicants as high risk which will result in loosing customers who could be potentially a good loan taker.