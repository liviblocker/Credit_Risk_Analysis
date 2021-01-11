# Credit_Risk_Analysis
## Overview of the Loan Prediction Risk Analysis
I've been asked to work with the lead Data Scientist at LendingClub to use machine learning to predict credit risk. I utilized 6 different machine learning models to determine the most accurate and precise model to predict credit risk. I ran oversampling models using RandomOverSampler and SMOTE algorithms, and an undersampling model using the ClusterCentroids algorithm. I, then, used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The following document details the results of the various models and determines which model is ideal for determining credit risk.

## Results
In the following results, I will break down the accuracy score and recall for all 6 models. The precision (0.99) is the same for all 6 models, so it's the accuracy score and recall that will best determine the most effective model.

# Naive Random Oversampling
![NaiveRandomOversampling.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)
Accuracy score: 0.67
Precision: 0.99
Recall: 0.61

# SMOTE Oversampling
![SMOTEOversampling.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/SMOTEOversampling.png)
Accuracy score: 0.66
Precision: 0.99
Recall: 0.69

# Cluster Centroids
![ClusterCentroids.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids.png)
Accuracy score: 0.54
Precision: 0.99
Recall: 0.42

# SMOTEENN
![SMOTEENN.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier.png)
Accuracy score: 0.64
Precision: 0.99
Recall: 0.57

# Balanced Random Forest Classifier
![BalancedRandomForestClassifier.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier.png)
Accuracy score: 0.87
Precision: 0.99
Recall: 0.87

# Easy Ensemble AdaBoost Classifier
![EasyEnsembleAdaBoostClassifier.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoostClassifier.png)
Accuracy score: 0.94
Precision: 0.99
Recall: 0.94




## Summary
There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
