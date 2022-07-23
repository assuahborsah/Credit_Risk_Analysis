# Credit_Risk_Analysis

# Overview of the analysis

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data would be oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. Then, apply a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, a comparison of two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once everything is done, evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# Resources

Python, Visual Studio Code, Anaconda, Jupyter Notebook and Pandas.

# Results/Deliverables

The results are presented between 0 and 1, where 0 means that the model does not perform well on the metric being measured, while 1 means that it does perform well.

## Random Oversampling

![image](https://user-images.githubusercontent.com/96086671/180618321-8da494c3-ce36-4233-ae00-061a2fe86a87.png)

 
 
## SMOTE Oversampling
 
 ![image](https://user-images.githubusercontent.com/96086671/180618324-e3dd55cf-6515-4a78-8a4c-4adb317bc8b1.png)

 
 
 
## Cluster Centroids Undersampling
 

![image](https://user-images.githubusercontent.com/96086671/180618331-d38ce283-c713-4536-b218-76ca402127e5.png)



## SMOTEENN Combination Under and Over Sampling

![image](https://user-images.githubusercontent.com/96086671/180618348-63e40aa0-e728-46b8-8113-39da13f8d11c.png)

 
 
 
## Balanced Random Forest Classifier
 
 
 ![image](https://user-images.githubusercontent.com/96086671/180618364-f16746de-3fd0-435f-82d4-d76726e88325.png)



 
## Easy Ensemble AdaBoost Classifier


![image](https://user-images.githubusercontent.com/96086671/180618377-61bf2262-c5d4-419d-93dc-786aad61c193.png)

 
 
 
## Precision

•	The precision of the bad loan applications (high_risk) is very close to 0%, indicating that none of the models predict well the number of true positives. On the other hand, all the models are 1 or 100% for the low_risk class which means they are great at predicting good loan applications.

## Recall/Sensitivity

•	The Easy Ensemble AdaBoost Classifier showed good recall results, where bad loan applications had 92% and good loans had 94%.

•	The balanced Random Forest Classifier had a decent recall of 87% on the good loans.

## Specificity

•	Balanced Random Forest Classifier had the specificity of 87% on the high_risk, which means it is good at avoiding false positive bad loans.

•	Easy Ensemble AdaBoost Classifier had the specificity of 94% on the high_risk and 92% on the low_risk, which means it is great at avoiding false positives for both.

## f1 metric

•	On the high_risk, none of the models had good results on the f1 metric applied to the bad loans.

•	On the low_risk, all the algorithms showed good f1 results except the under sampling ClusterCentroids. The highest two being the Balanced Random Forest Classifier with 93% and the Easy Ensemble AdaBoost Classifier with 97%. 


# Summary

For all models, utilizing the EasyEnsembleClassifier is the most effective as it provides the highest Score for all Risk loans. Even though the Easy Ensemble AdaBoost Classifier had great results on the recall, specificity, and accuracy. Its 0-precision result impacted negatively its f1 metric. Overall, the Easy Ensemble AdaBoost Classifier performed well on all metrics measured.

In General, above the 90% of the current analysis, utilizing EasyEnsembleClassifier will perform a High-Risk loan precision as a great value for the overall analysis.
