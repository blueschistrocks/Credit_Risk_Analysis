## Overview
This analysis was conducted to understand how to utilize Machine Learning statistical algorithms for making predictions based on patterns in the dataset provided from LendingClub, a lending service company. 

To complete this analysis, we use different Supervised Machine Learning procedures to train and evaluate the data with unbalanced classes. The dataset has an unbalanced classification problem due to many good loans over the lower amount of risky loans. To balance out the classifications, allow for more insightful predictions and increase the accuracy score, various Machine Learning algorithms to resample the data were employed. The following algorithms were used:

- RandomOverSampler
- SMOT
- ClusterCentroids
- SMOTEENN
- BalancedRandomForestClassifier
- EasyEnsembleClassifier.

## Results
The LendingClub dataset contained 115,675 loan applications in the first quarter 2019 (1Q19). Loan Status was to determine if the application was considered a low or high risk. Applications that had current as the loan status were classified as low risk and the remaining applications as high risk. The dataset was condensed to to 68,817 applications with 99% of the applications classified low risk.


The data was split using the 75/25% method for training vs. testing.  51,366 applications were listed as low risk and 246 were categorized as high risk in to the training set.

![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/65252712f949bf3523f7bacf0f80a67000612adc/Images/Screen%20Shot%202022-06-04%20at%207.10.28%20PM.png)<br>

## Deliverable 1: Use Resampling Models to Predict Credit Risk
### Oversampling
The RandomOverSampler Model results classified 51,366 records each as High Risk and Low Risk.

![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/65252712f949bf3523f7bacf0f80a67000612adc/Images/Screen%20Shot%202022-06-04%20at%207.10.55%20PM.png)<br>

![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/65252712f949bf3523f7bacf0f80a67000612adc/Images/Screen%20Shot%202022-06-04%20at%207.11.21%20PM.png)<br>
- Calculated balanced accuracy score: 79%.

- The precision rate for High Risk was 1% with a recall of 70% giving this model an F1 score of 2%.
- The precision rate for Low Risk was of 100% and recall of 61%.

![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/65252712f949bf3523f7bacf0f80a67000612adc/Images/Screen%20Shot%202022-06-04%20at%207.12.31%20PM.png)<br>
## Synthetic Minority Oversampling Technique (SMOTE)

- Calculated balanced accuracy score: 66% only slightly higher.
![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/5b25dff920e7bc0779aa056a4578fa6d76734464/Images/Screen%20Shot%202022-06-04%20at%207.14.09%20PM.png)<br>

The precision rates were only slightly different than the first model.
- The precision rate for High Risk was 1% with a recall of 63% giving this model an F1 score of 2%.
- The precision rate for Low Risk was of 100% and recall of 69%.
![image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/5b25dff920e7bc0779aa056a4578fa6d76734464/Images/Screen%20Shot%202022-06-04%20at%207.14.50%20PM.png)<br>
### Undersampling
The undersampling model classified High Risk and Low Risk records as 246 each.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.15.17%20PM.png)<br>

- Calculated balanced accuracy score: 54.5% lower than the above models.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.15.31%20PM.png)<br>

- The precision rate for High Risk was 1% with a recall of 69% giving this model an F1 score of 1%.
- The precision rate for Low Risk was of 100% and recall of 40%.
![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.16.19%20PM.png)<br> 

## Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk
### Combination (Over and Under) Sampling
The SMOTEENN model classified 68,460 records as High Risk and 62,011 as Low Risk.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.16.36%20PM.png)<br>

- Calculated balanced accuracy score: 65%.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.16.47%20PM.png)<br>

- The precision rate for High Risk was 1% with a recall of 72% giving this model an F1 score of 2%.
- The precision rate for Low Risk was of 100% and recall of 57%.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.16.56%20PM.png)<br>

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
#### BalancedRandomForestClassifier Model

The BalancedRandomForestClassifier classified 51,366 as High Risk and 246 as Low Risk.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.17.44%20PM.png)<br>

- The calculated balanced accuracy score: 79%, which is higher than the above models. 
![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.17.52%20PM.png)<br>

- The precision rate for High Risk was 3% with a recall of 70% giving this model an F1 score of 6%.
- The precision rate for Low Risk was of 100% and recall of 87%.
- The total_rec_prncp feature was at 7.9% of the total.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.18.20%20PM.png)<br>

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/b3c1816d1233b25ad574b54d4fae7c69bcfe70ec/Images/Screen%20Shot%202022-06-04%20at%207.18.45%20PM.png)<br>

#### EasyEnsembleClassifier Model

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/5ab108f66920136cda5a408a30662d25f733e0be/Images/Screen%20Shot%202022-06-04%20at%207.19.41%20PM.png)<br>

- The calculated balanced accuracy score: 93%, which is higher than all the models. 

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/5ab108f66920136cda5a408a30662d25f733e0be/Images/Screen%20Shot%202022-06-04%20at%207.19.51%20PM.png)<br>

- The precision rate for High Risk was 9% with a recall of 92% giving this model an F1 score of 16%.
- The precision rate for Low Risk was of 100% and recall of 94%.

![Image](https://github.com/blueschistrocks/Credit_Risk_Analysis/blob/5ab108f66920136cda5a408a30662d25f733e0be/Images/Screen%20Shot%202022-06-04%20at%207.20.01%20PM.png)<br>

### Summary
Of the six models, the EasyEnsembleClassifer model provided the highest accuracy rate of 93% with a rate of precision of predicting high risk and low risk candidates at 9% and 100%, respectively.  The high risk and low risk recall or sensitivity rate was 92 and 94 respectively. These were also the highest rated of all of the six models. 

Based on the results I would recommend the EasyEnsembleClassifer model to perform these types of analysis.

For future analysis would be use a different data set. The LendingClub dataset had 99% of the applications classified as low risk with only 1% of the data classified in the high risk category. Machine Learning algorithms using a dataset like this one may cause a skew in the results by creating groups from a dataset that is has a very small number of High Risk applications. 


