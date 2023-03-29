# Credit_risk_18

## Overview of the analysis:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Different techniques were employed to train and evaluate models with unbalanced classes. I usee imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

The data set analysed is from LendingClub. the data was oversampled using the Random Oversampler and smote algorithms. the undersampling of the datea used the cluster centroids algorithm. A combined approach of over and under sampling approach used the smoteenn algorith. The next step was to compare the machine learning models that reduce bias, balancedRandomForestClassifier and Easey EnsembleClassifier to predict credit risk. Then the over all performance of the models was evaluated to determine the effectiveness of the models at predicting credit risk. 

## Results

•	Naive Random Oversampling results: Our balanced accuracy test it 65%, the precision for the high_risk has a very low positivity at 1% and the recall is 71%

                pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.71      0.60      0.02      0.65      0.43       101
   low_risk       1.00      0.60      0.71      0.75      0.65      0.42     17104

avg / total       0.99      0.60      0.71      0.75      0.65      0.42     17205


•	SMOTE oversampling results: the accuracy score is 66%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.63      0.69      0.02      0.66      0.44       101
   low_risk       1.00      0.69      0.63      0.82      0.66      0.44     17104

avg / total       0.99      0.69      0.63      0.81      0.66      0.44     17205

•	Undersampling results: balanced accuracy score is 52% overall, the precision is at 99% and the recall is 40%
                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.69      0.40      0.01      0.52      0.28       101
   low_risk       1.00      0.40      0.69      0.57      0.52      0.27     17104

avg / total       0.99      0.40      0.69      0.56      0.52      0.27     17205

•	Combination(over and undersampling) results: balanced accuracy score is 64% the precision is 99% and the recall is 57% overall

                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.72      0.57      0.02      0.64      0.42       101
   low_risk       1.00      0.57      0.72      0.72      0.64      0.40     17104

avg / total       0.99      0.57      0.72      0.72      0.64      0.40     17205

•	Balanced Random Forest Classifier results: the accuracy score is 79% the precision is 99% and the recall is 88%
                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.04      0.71      0.88      0.07      0.79      0.62       104
   low_risk       1.00      0.88      0.71      0.94      0.79      0.64     17101

avg / total       0.99      0.88      0.71      0.93      0.79      0.64     17205

•	Easy Ensemble AdaBoost Classifier results: the accuracy score is 92% the precision is 99% and the recall is 94%

                 pre       rec       spe        f1       geo       iba       sup

  high_risk       0.09      0.89      0.94      0.16      0.92      0.84       104
   low_risk       1.00      0.94      0.89      0.97      0.92      0.85     17101

avg / total       0.99      0.94      0.89      0.96      0.92      0.85     17205


## Summary:

The first two models were oversamples. The Third model was undersampled, and the fourth model used a combination of over and undersampling. Using the combination of these methods to determing which model was best at predicting which loans are the highest risk. 

The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In the first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically you want a good balance of recall and precision in the models.  I recommend the ensemble classifiers over the first four models. The easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.

