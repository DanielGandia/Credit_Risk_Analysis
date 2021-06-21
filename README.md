# Credit_Risk_Analysis

## Overview of the Analysis:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we'll need to employ different techniques to train and evaluate models with unbalanced classes. I have been asked to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I'll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I'll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I'll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, I'll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.
## Resources:

- Data Sources: LoanStats_2019Q1.csv
- Software: Python 3.83, Jupyter Notebook 6.3.0, Visual Studio Code 1.57.1

## Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)

### Resampling Models to Predict Credit Risk
Naive Random Oversampling:
- Balance accuracy score: 62.4%
- Precision scores: high-risk 0.01 ; low-risk 1.00
- Recall scores: high-risk 0.68 ; low-risk 0.57
- Avg/Total: .99 for precision & .57 for recall 

![naive_oversampling.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/naive_oversampling.png)

### SMOTEENN Algorithm to Predict Credit Risk

SMOTE Oversampling:
- Balance accuracy score: 63.5%
- Precision scores: high-risk 0.01 ; low-risk 1.00
- Recall scores: high-risk 0.65 ; low-risk 0.61
- Avg/Total: .99 for precision & .65 for recall 

![smote_oversampling.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/smote_oversampling.png)

Undersampling:
- Balance accuracy score: 64.6%
- Precision scores: high-risk 0.01 ; low-risk 1.00
- Recall scores: high-risk 0.69 ; low-risk 0.44
- Avg/Total: .99 for precision & .44 for recall 

![undersampling.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/undersampling.png)

Combination (Over and Under) Sampling:
- Balance accuracy score: 64.6%
- Precision scores: high-risk 0.01 ; low-risk 1.00
- Recall scores: high-risk 0.74 ; low-risk 0.55
- Avg/Total: .99 for precision & .55 for recall 

![combined_over_undersampling.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/combined_over_undersampling.png)
### Ensemble Classifiers to Predict Credit Risk

Balanced Random Forest Classifier:
- Balance accuracy score: 66.1%
- Precision scores: high-risk 0.59 ; low-risk 1.00
- Recall scores: high-risk 0.32 ; low-risk 1.00
- Avg/Total: 1.00 for precision & 1.00 for recall

![random_classifier.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/random_classifier.png)

Easy Ensemble AdaBoost Classifier:
- Balance accuracy score: 92.6%
- Precision scores: high-risk 0.06 ; low-risk 1.00
- Recall scores: high-risk 0.92 ; low-risk .93
- Avg/Total: 1.00 for precision & .93 for recall

![adaboost_classifier.png](https://github.com/DanielGandia/Credit_Risk_Analysis/blob/main/Images/adaboost_classifier.png)

## Summary:

The above shown results indicate that the Easy AdaBoost Classifier is the most accurate model with a 92.6% balance accuracy score. All of the other models had accuracy scores in the mid 60s.  This model also had the one of the highest recall rate for high-risk loans. This is the model that I recommend to be used if a similar exercise is to be done for high-risk loan precision.





