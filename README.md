# Credit Risk Analysis
Training and evaluating supervised machine learning models for the prediction of credit card risk.

## Overview of the analysis
The goal of the present project was to choose the best machine learning model to predict credit card risk. As low-risk loans are more frequent than high-risk loans, the models evaluated needed to account for the imbalance in the probability of the outcomes. Six different models were tested, 4 resampling methods (Naive Random OverSampling, SMOTE OverSampling, UnderSampling, SMOTEENN Over- and UnderSampling) and 2 ensemble methods (Balanced Random Forest Classifier, Easy Ensemble Classifier).

Dataset source: LendingClub.

## Results
To run the models, the dataset was first cleaned and splitted in train and test sets. The models were then trained and different measures were generated to evaluate them. The main measures used here were:
  - The balanced accuracy score, accounting for the variance explained by the overall model. Higher score means that the model is better at explaining the outcomes.
  - The sensitivity (or recall) of the model for the high-risk outcome. Higher sensisity means that the model is better at predicting true high-risk cases out of the total of actual high-risk cases.
  - The precision of the model for the high-risk outcome. Higher precision means that the model is better at predicting true high-risk cases out of the total of predicted high-risk cases.

### Resampling Models

#### Naive Random OverSampling
 - balanced accuracy score = 65%

![Screen Shot 2022-02-26 at 12 21 18 AM](https://user-images.githubusercontent.com/89421440/155835992-3e037ad6-cad5-49be-b9c2-dd1fd6e71772.png)

#### SMOTE OverSampling
- balanced accuracy score = 66%

![Screen Shot 2022-02-26 at 12 21 55 AM](https://user-images.githubusercontent.com/89421440/155836014-ab4ab3d7-c16f-4d15-90cc-ba5c204b2928.png)

#### UnderSampling
- balanced accuracy score = 66%

![Screen Shot 2022-02-26 at 12 22 44 AM](https://user-images.githubusercontent.com/89421440/155836037-be8cb173-76cf-4708-a043-b69ecf0161f7.png)

#### SMOTEENN Over- and UnderSampling
- balanced accuracy score = 54%

![Screen Shot 2022-02-26 at 12 23 10 AM](https://user-images.githubusercontent.com/89421440/155836057-c25b20bb-a5b1-4779-9b1a-a092cbb2cbe9.png)

### Ensemble Models

#### Balanced Random Forest Classifier
- balanced accuracy score = 79%

![Screen Shot 2022-02-26 at 12 23 46 AM](https://user-images.githubusercontent.com/89421440/155836072-b8a63d1f-d3c1-4a18-b900-98ef5b650238.png)

#### Easy Ensemble Classifier
- balanced accuracy score = 93%

![Screen Shot 2022-02-26 at 12 24 19 AM](https://user-images.githubusercontent.com/89421440/155836085-d0917341-0d9c-45bc-ae7f-1d8d3ae2b61b.png)

## Summary
Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
