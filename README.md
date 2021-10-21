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
	
The accuracy score compares the actual outcome(y-values) from the test against the nodels' predicted values.  The acuracy score is the percentage of predictions that are correct. The accuracy score for this model is 0.655 or 66%. This model is not demonstrative of a highly accurate model. It is still useful as it is the easiest classification metric to understand however it does not reveal the underlying disribution of response values. For a deeper understanding we will examine the metrics produced by the classification report
	
![Naive Precision](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/naive%20random%20classification.PNG)

b.Precision Score: The precision score indicates to us how accurate the model is at predicting positive values.  The classification report shows us that the "Pecision score for __low risk loans is 1.00 or 100%__.  Althought initially this may not seem to be very good that the model is predicicting 100% percent of low risk loans it may be indicative of overfitting for low risk loans. This type of overfitting will make this a poor model for predicting future data sets.  The precision for predicting high risk loans however is the stark opposite with an accuracy of __0.01 or 1%__ this might indicate a high amount of false negatives for low risk loans.  This can be cooberated by the confusion matrix see below,out of 6,421 loans low risk only 69 were actually correctly predicted.

![Naive CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/naive_random_cm.PNG)

c.Recall Score: The recall score indicates the proportion of actual positives which were correctly classified. That is when the actual value is positive, how often is the prediction corrrect. The recall for __low risk loans is .68 or 68%__. The sensitivity for __hight risk loans is lower at .63 or 63%__ 
The recall score for high risk loan is .68 or 68% and the sensitivity for low risk loans is .63 or 63%.

It should be mentioned that the __F1 score__ which is the combination of precision and recall is very low for high risk loans at __0.02 or 2%__  
	
###### 2. Smote

![Smote Accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_accuracy.PNG)

a.Accuracy Score: The accuracy score for this model is __0.66 or 66%__ which is not highly accurate.  

![Smote Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_classification.PNG)

b.Precision Score The __precision score for low risk loans is 1.00 or 100%__; again this is very indicative or overfitting for low risk loans.  The __precision for high risk loans is .01 or 1%__, this is due to the high number of false negatives which can be seen in the confusion matrix out of 5351 loans that were predicted as high only 64 was truly high (see below).  

![Smote CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smote_cm.PNG)

c.Recall Score: The sensitivity for low risk loans is __.69 or 69%__ but this falls for high risk loans to __0.63 or 63%__. Also the __f1 score for high risk loans is .02 pr 2%.

###### 3.ClusterCentroids

![ClusterCentroid accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_accuracy.PNG)

a.Accuracy Score: The accuracy score for the _ClusterCentroid_ model is __0.66 or 66%__. 

![ClusterCentroid Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_classification.PNG)

b.Precision Score: The precision score for __low risk loans is 1.00 or 100%__ but the precision for __high risk loans is only .01 or 1%__. This model seems to be also overfitting for low risk loans. Out of 10,410 loans that predicted as high risk loans only 70 of them were actually high risk loans

![ClusterCentroid CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/cluster_cm.PNG)

c.Recall Score: The sensitivity for __low risk loans is .40 or 40%__ and __0.69 or 69% for high risk loans__. There seems to be a greater sensitivity to high risk loans in this model most likely because this is is an undersampling techinique, wherein all of the data for the miniority class the (high risk loans)is being kept, while decreasing the size of the majority class (low risk loans).
The F1 score for for low risk loans is __0.57__ and for high risk loans is __0.01__ which is extreamly low.

###### 4.Smoteenn

![Smoteenn accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smoteenn_accuracy.PNG)

a.Accuracy Score: The accuracy score for the _Smoteenn Model_ is __0.54__ or 54% 

![Smoteenn Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smoteenn_classification.PNG)

b.Precision Score: The precision for __low risk loans is 1.00 or 100%__,this is indicative of overfitting.  The precision for __high risk loans is 0.01 or 1%__ 

![Smoteenn CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/smoteenn_cm.PNG)

c.Recall Score: The sensitivity score for __low risk loans is 0.57 or 57%__ and the sensitivity score for __high risk loans is 0.72 or 72%__. The sensitivity score for this model also might have been improved because _Smoteenn_ sampling combines both over-sampling and under-sampling which would increase the representation of the high risk loans dataset.  However when we look at the F1 score we see that the score for __high risk loans is 0.02 or 20% is very low__ and the score for __low risk loans is .74%



###### 5.Randomforest

![RandomForest Accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/randomForest_accuracy.PNG)

a.Accuracy Score: The accuracy score for the RandomForest model is __.67 or 67%__

![RandomForest Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/randomForest_classification.PNG)

b.Precision Score: The precision score for __1.00 or 100% for low risk loans and 0.90 or 90% for high risk loans__ This score appears to be highly accurate on both metrics however careful consideration must be given to the sensitivity score

![RandomForest CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/randomForest_cm.PNG)

c.Recall Score: The sensitivity score for __low risk loans is 1.00 or 100%__ but the recall for __high risk loans is .35 %__ which is very poor.
Also the __f1 score for low risk loans is on 1.00 or 100%__ and for __high risk loans it is only .50 or 50% 

###### 6.AdaBoosting

![Ada Boosting Accuracy](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/Ada_accuracy.PNG)

a.Accuracy Score: The accuracy score using the _AdaBoosting Model_ is __99.6 or 100%__

![Ada Boosting Classification](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/Ada_classification.PNG)

b.Precision Score: The precision score for __low risk loans is 1.00 or 100%__ and the precision for __high risk loans is .88 or 88%__ Here we see that the boosting a technique to combine a set of weak learners into a strong learner.Boosting trains a sequence of weak models so that each model learns from the errors of the previous model, and the models form an ensemble. This may be the reason we have seen such an improvement in both the accuracy score and the precision scores.  It is imperative however that we also consider the sensitivity score.

![Ada Boosting CM](https://github.com/wallaceportia/Credit_Risk_Analysis/blob/main/Resources_pictures/Ada_cm.PNG)

c.Recall Score
The recall on __low risk loans is 1.00 or 100%__ however this drops off significantly for __high risk loans the sensitivity is .38 or 38%__ this is an unacceptable score.
The F1 score for __low risk loans is 1.00 or 100%__ however this drops off significantly for __high risk loans to .53%__
	
## Summary:

It is fair to say that none of the models performed optimally , however some were stronger than others. For the models that fell under the umbrella of oversampling: __Naive Random Oversampling and Smote__, the level of accuracy was not very good.  We saw that overfitting towards the data for low risk loans produced high precision for low risk loans but very poor for high risk loans.  Further to this we saw that the sensitivity score was also not very high.  There was a large difference between the F1 score which signifies a huge imbalnce bewtween the precision and sensitity.

The performance of the undersampling models __ClusterCentroids__ also was not very stellar.  We also saw overfitting towards the low risk loans. We saw an imporvement in sensitivity for high risk loans but it the sensitivity for low risk loans tanked.  The F1 score also revealed a huge desparity between precision and accuracy

For the combinatorial model __Smoteenn__ The accuracy did not see any marked improvement.  There was still overfitting towards low risk loans and the precisions score for high risk loans was very unsuccessful.  The sesitivity score also improved for high risk loans in this model but also at the expense of the low risk score falling to 57%.  

Ensamble classifiers: __Randomforest and AdaBoosting__, for the Randomforest classifier the accuracy was moderate however the precision score for both the high risk and low risk loans was on par with each other both scoring very high and would have appeared that the issue of overfitting was taken care of.  This idea however was not seen in the poor performance of the sensitivity for high risk loans.  The AdaBoosting classifier produced the highest accuracy of _100%_ The precision for both low risk and high risk loans was good at 100% and 88% respectively.  However this was deninished by the weak sensitivity for high risk loans.
	
 
###### Recommendation

The team with along with lead Data Scientist Jill have decided that not of these models are ready for adoption.  To many high risk loans will be accepted and thereby causing a loss to the bank or financial institution.  Therefore to ensure that our company maintains it's trustworthiness we would suggest a stronger and better model be developed; possibly take a look at deep neuro networks!
