# Credit_Risk_Analysis
## Overview of the Loan Prediction Risk Analysis
I've been asked to work with the lead Data Scientist at LendingClub to use machine learning to predict credit risk. I utilized 6 different machine learning models to determine the most accurate and precise model to predict credit risk. I ran oversampling models using RandomOverSampler and SMOTE algorithms, and an undersampling model using the ClusterCentroids algorithm. I, then, used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The following document details the results of the various models and determines which model is ideal for determining credit risk.

## Results
In the following results, I will break down the accuracy score and recall for all 6 models. The precision is the same for all 6 models (at 0.99), so it's the accuracy score and recall that will best determine the most effective model.

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

This model randomly under-samples each bootstrap sample to balance it.

# Easy Ensemble AdaBoost Classifier
![EasyEnsembleAdaBoostClassifier.png](https://github.com/liviblocker/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoostClassifier.png)
Accuracy score: 0.94

Precision: 0.99

Recall: 0.94


## Summary
With the Naive Oversampling Classifier, we simply oversample the instances of high-risk data points to account for the class imbalance. This is neither particularly accurate nor sensitive model. In the SMOTE model, we oversample high-risk data points again, but in this model we include data points close to the high-risk data point to create a larger minority class sample. This model is only slightly more sensitive than the Naive Oversampling Classifier. It seems that these oversampling models do not do enough to effectively determine high-risk individuals.

Similar to the SMOTE Oversampling model, the Cluster Centroids algorithm identifies clusters of the majority class, then generates synthetic data points. The majority class is then undersampled down to the size of the minority class. This is the least sensitive and least accurate of all 6 models. The SMOTEENN model both undersamples the majority class (low-risk data points) and oversamples the minority class (high-risk data points) by creating synthetic data points (in a similar way to the SMOTE and Cluster Centroid models). This, again, is not the most effective model.

The ensemble algorithms are the most effective models to determine high credit risk.

# Recommendation
This model has a high accuracy score, high precision, and high sensitivity. It has the highest F1 score, will most accurately determine who is at high credit risk.
