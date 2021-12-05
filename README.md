# Overview
The purpose of this study was to develop a statistical model that would be able to accurately predict credit risk for loan application. The models determine if an applicats will be able to afford/repay the loan due to many criteria listed on their loan application. 

# Results
1) The first model uses RandomOverSampling for the sample set on a logistic regression model.
 - The balanced accuracy score for this model gave 0.643 which isn't that great of an accuracy but it's over 50%.
 - The precision of the model gave 0.63 and 0.66 for high risk and low risk respectively. This is fairly good precision, but not enough to be comfortable using in a lending situation.
 - The recall of the model gave 0.59 and 0.70 for high risk and low risk respectively. This is fairly good precision, but not enough to be comfortable using in a lending situation.

2) The second model uses SMOTE Oversampling for the sample set on a logistic regression model.
 - The balanced accuracy score for this model gave 0.632 which is slightly lower than model 1.
 - The precision of the model gave 0.64 and 0.63 for high risk and low risk respectively. This was slightly less precision for both risks than model 1.
 - The recall of the model gave 0.66 and 0.61 for high risk and low risk respectively. This brought the recall closer than in model 1.

3) The third model uses ClusterCentroids Undersampling for the sample set on a logistic regression model.
 - The balanced accuracy score for this model gave 0.695 which is slightly higher than both model 1 & 2.
 - The precision of the model gave 0.72 and 0.67 for high risk and low risk respectively. This was again slightly higher than models 1 & 2.
 - The recall of the model gave 0.63 and 0.76 for high risk and low risk respectively. This was again slightly higher than models 1 & 2.

4) The forth model uses SMOTEENN Combination Sampling for the sample set on a logistic regression model.
 - The balanced accuracy score for this model gave 0.67 which is slightly higher than both model 1 & 2 but not as high as model 3.
 - The precision of the model gave 0.66 and 0.68 for high risk and low risk respectively. This was again slightly higher than both model 1 & 2 but not as high as model 3.
 - The recall of the model gave 0.91 and 1.00 for high risk and low risk respectively. This was a wider difference than all other 3 models.

5) The fifth model used a BalancedRandomForestClassifier on the original sample set.
 - The balanced accuracy score for this model gave 0.52 which is lower than all other 4 models and only slightly above 50%.
 - The precision of the model gave 0.05 and 1.00 for high risk and low risk respectively. This precision is good since it can accurately predict low risk loans and the high risk loans can then be done without a model.
 - The recall of the model gave 1.00 and 0.91 for high risk and low risk respectively. This recall is good since it can accurately predict high risk applicants by 100% so these applications can be flagged to be done without a model.

6) The sixth model used a Easy Ensemble AdaBoost Classifier on the original sample set.
 - The balanced accuracy score for this model gave 0.53 which is relative to model 5.
 - The precision of the model gave 0.05 and 1.00 for high risk and low risk respectively. This precision is equal to model 5.
 - The recall of the model gave 1.00 and 0.91 for high risk and low risk respectively. This recall is equal to model 5.

# Summary
In summary, I would not recommend any of these models, at least with the provided dataset. Each model had issues and none of them had above a 70% accuracy. For a model to be used in a business settings with as much risk as lending out loans creates, it would need to be much more accurate for myself to begin using it.
