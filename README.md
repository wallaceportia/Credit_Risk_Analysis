# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

Fast Lending a peer to peer lending company has decided to use 'Machine Learning' to predict credit risk.  They would like to use Machine Learning as they believe it will accomplish a more reliable lending experience, by miminimizing high risk loans.  The idea is that it would lead to choosing good candidates for loans and in turn lower default rates. In conjunction with the lead Data Scientist, Jill, we will build several machine learning algorithms to predict credit risk. The resampling techinques which be used are: Oversampling, Undersampling, Combinatorial and Ensemble Classifiers. The 6 techniques that will be used are:

*A.Oversampling*

   1.Naive Random Oversampling

   2.Smote

*B.Undersampling*

   3. ClusterCentroids

*C. Combinatorial*

   4.Smoteenn

*D.Ensemble Classifiers*

   5.RandomForest
  
   6.AdaBoosting
  
 Based on the following results we will choose which of these models may be the most viable to implement  
	
## Results:

###### 1. Naive Random Oversampling

a.Accuracy Score
        
![Naive_Oversampling](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/naive%20random%20accuracy.PNG)
	
The accuracy score compares the actual outcome(y-values) fromn the test against the nodels' predicted values.  The acuracy score is the percentage of predictions that are correct. The accuracy score for this model is 0.655 or 66%. This model is not demonstrative of a highly accurate model. It is still useful as it is the easiest classification metric to understand however it does not reveal the underlying disribution of respone values. For a deeper understanding we will examine the metrics produced by the classification report
	
![Naive Precision](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/naive%20random%20classification.PNG)

b.Precision Score: The precision score indicate to us how acurate the model is at predicting positive values.  The classification report shows us that the "Pecision score for __low risk loans is 1.00 or 100%__.  Althought initially this may not seem to be bad at predicicting 100% percent may be indicative of overfitting for low risk loans. This type of overfitting will make this a poor model for predicting future data sets.  The precision for predicting high risk loans however is the stark opposite with an accuracy of __0.01 or 1%__ this might indicate a high amount of false positives for low risk loans.  This can be cooberated by the confusion matrix see below,out of 6,421 loans low risk only 69 were actually correctly predicted.

![Naive CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/naive_random_cm.PNG)


	
The precision score for this model high risk loans is .01 or 1% and the precision for low risk loans is 1.00



c.Recall Score

The recall score for high risk loan is .68 or 68% and the sensitivity for low risk loans is .63 or 63% 
	

###### 2. Smote

![Smote Accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_accuracy.PNG)
a.Accuracy Score

![Smote Accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_accuracy.PNG)

b.	Precision Score

![Smote Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_classification.PNG)

![Smote CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_cm.PNG)

c.	Recall Score


###### 3.ClusterCentroids

![ClusterCentroid accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_accuracy.PNG)

a.Accuracy Score

![ClusterCentroid Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_classificatio.PNG)

b.Precision Score

![](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_cm.PNG)

c.	Recall Score

###### 4.Smotteen

![]()

a.Accuracy Score

![]()
b.Precision Score


![]()
c.Recall Score



###### 5.Randomforest

![]()

a.Accuracy Score

![]()

b.Precision Score

![]()]

c.Recall Score

###### 6.AdaBoosting

![]()

a.Accuracy Score

![]()

b.Precision Score

![]()

c.Recall Score

	
## Summary:

A pronounced implance between the sensitivity and precision will yield a low F1 score
o	There is a summary of the results (2 pt)
o	There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
