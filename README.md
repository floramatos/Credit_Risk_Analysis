# Credit Risk Analysis
Training and evaluating supervised machine learning models for the prediction of credit card risk.

## Overview of the analysis
The goal of the present project was to choose the best machine learning model to predict credit card risk. As low-risk loans are more frequent than high-risk loans, the models evaluated needed to account for the imbalance in the probability of the outcomes. Six different models were tested, 4 resampling methods and 2 ensemble methods.

Dataset source: LendingClub.

## Results
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### Resampling Models
resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

#### Oversample data using the RandomOverSampler and SMOTE algorithms
Naive Random OverSampling
Counter({'low_risk': 51366, 'high_risk': 51366})
balanced accuracy score = 0.6547385707934685
confusion matrix
array([[   73,    28],
       [ 7069, 10035]])

SMOTE OverSampling
Counter({'low_risk': 51366, 'high_risk': 51366})
balanced accuracy score = 0.66201409663885
confusion matrix
array([[   64,    37],
       [ 5296, 11808]])
       
**SMOTE slight better than Naive Random

#### Undersample data using the ClusterCentroids algorithm
UnderSampling
Counter({'high_risk': 246, 'low_risk': 246})
balanced accuracy score = 0.66201409663885
confusion matrix
array([[   70,    31],
       [10341,  6763]])
**althought the score is similar to SMOTE, the confusion matrix seems to indicate that undersampling is worse than oversampling as it has less true negatives and more false negatives than SMOTE

#### Oversample and undersample data using the SMOTEENN algorithm
determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms

SMOTEENN
Counter({'high_risk': 68460, 'low_risk': 62011})
balanced accuracy score = 0.5442369453268994
confusion matrix
array([[  73,   28],
       [7324, 9780]])
       
### Compare machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk
train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model

BalancedRandomForestClassifier 
balanced accuracy score = 0.7885466545953005
confusion matrix
array([[   71,    30],
       [ 2153, 14951]])
       
EasyEnsembleClassifier
balanced accuracy score = 0.9316600714093861
confusion matrix
array([[   93,     8],
       [  983, 16121]])
       
## Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
