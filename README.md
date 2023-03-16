# Mod_18_Challenge
## Purpose
The goal of this analysis is to test 6 different models' ability to predict/identify good loans and risky loans. Several models oversample the high risk rows that are significantly less frequent than good loans in the data source. One model undersamples the dominant good loans. Other models use ensemble learning, which simultaneously combines multiple models into one model to determine good and risky loans. We are to determine if any model reliably determines good and risky loans. 

## Results
The RandomOverSampler and SMOTE algorithms conduct oversampling. The ClusterCentroids algorithm conducts undersampling. SMOTEEN combines over and undersampling. The BalancedRandomForestClassifier and EasyEnsembleClassifier models use ensemble learning to combine multiple models into one to determine good and risky loans.

 * Below is the balanced accuracy, precision, and recall scores from the RandomOverSampler model. Its balanced accuracy score is ~66%. Please note for all of these models that low_risk = 0 and high_risk = 1. According to the classification report, this model's precision in determining high risk loans is 1%. A total of 6913 loans were determined to be high risk, but only 73 were actually high risk loans. Therefore, only 1% of loans that were deemed to be risky were accurate in this determination. Of the 101 loans that were actually high risk, only 73 were predicted to be high risk (the other 28 high risk loans were determined by the model to be low risk). Therefore, the model's sensitivity/recall for high risk loans is 72%, meaning of the loans that are high risk the model will detect 72% of them as high risk. 
 ![RandomOverSampler_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/RandomOverSampler_Results.PNG)
 
 
 * Below are the results of the SMOTE oversampling model. Of loans the model determined were high risk, only 1% were actually high risk, which is the model's precision for determining risky loans. Of loans that were actually high risk, 62% were determined by the model to be high risk. This is the model's recall/sensitivity. The remaining high risk loans were incorrectly determined by the model to be low risk.
 ![SMOTE_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/SMOTE_Results.PNG)
 
 
 * Below are the results of the ClusterCentroid undersampling model. This model has roughly the same precision and recall for high risk loans as the previous two models. However, of the loans that were actually low risk, only 40% were determined by this model to be low risk, which is this model's sensitivity/recall for low risk loans. This model incorrectly determined 60% of low risk loans to be high risk. 
 ![Undersampling_ClusterCentroids_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/Undersampling_ClusterCentroids_Results.PNG)
 
 
 * SMOTEEN Model: This model is similar to the RandomOverSampler model. 
 ![SMOTEEN_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/SMOTEEN_Results.PNG)
 
 
 * BalancedRandomForest Model: Of the models we've viewed so far, this model has the best overall recall. Of loans that were actually low risk, the model correctly determined 89% of these loans as being low risk. Of loans that were actually high risk, the model correctly determined 64% of these high risk loans to be high risk loans. 
 ![BalancedRandomForest_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/BalancedRandomForest_Results.PNG)
 
 
 * EasyEnsemble Model: This model has the best overall recall and the highest precision of high risk loans. 
 ![EasyEnsemble_Results.png](https://github.com/tylerwe19/Mod_18_Challenge/blob/main/EasyEnsemble_Results.PNG)
 
 --- 
 
## Summary

