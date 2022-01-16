# Credit Risk Analysis
 
## Overview:
The purpose of this risk analysis was to look at credit card lending data with a variety of models to predict the credit risk for each application, as well as determine which model best predicted that risk. I used the Ensemble methods - Random Forest Classifier and the AdaBoost Classifier to test in addition to Oversampling, Undersampling, and Combination sampling (SMOTEEN) to model the data after it was sorted and fit.
<br>
## Results:
The following are results, in the order the various models were run: 
<ol>
   <li><strong>Random Oversampling</strong> <I>(See Example A below):</i> </li>
       <ul>
           <li>Balanced Accuracy Score: 0.64</li>
           <li>Precision: 0.99</li>
           <li>Recall: 0.69</li>
           <li>Notes: There is a very low precision rate (0.01) when it comes to predicting the high risk applications, as well as a low F1 score (0.02). </li>   
       </ul>
   <li><strong>SMOTE Oversampling</strong> <I>(See Example B below):</i>  </li>
       <ul>
           <li>Balanced Accuracy Score: 0.62</li>
           <li>Precision: 0.99</li>
           <li>Recall: 0.66</li>
           <li>Notes: These results are similar to the Random Oversampling, and also saw a very low precision rate(0.01) and F1 score (0.02) for the high risk predictions.</li>   
       </ul>
   <li><strong>Cluster Centroids Algorithm</strong> <I>(See Example C below):</i>  </li>
       <ul>
           <li>Balanced Accuracy Score: 0.62</li>
           <li>Precision: 0.99</li>
           <li>Recall: 0.44</li>
           <li>Notes: While this model performed the same for high risk predictions as the first two, this model additionally had a lower recall score than the previous two models.</li>   
       </ul>
   <li><strong>SMOTEEN</strong> <I>(See Example D below):</i>  </li>
       <ul>
           <li>Balanced Accuracy Score: 0.64</li>
           <li>Precision: 0.99</li>
           <li>Recall: 0.44</li>
           <li>Notes: This model performed the same as the Cluster Centroids model. </li>   
       </ul>
   <li><strong>Balanced Random Forest Classifier</strong> <I>(See Example E below):</i> </li>
       <ul>
           <li>Balanced Accuracy Score: 0.79</li>
           <li>Precision:  0.99</li>
           <li>Recall: 0.91</li>
           <li>Notes: This model performed slightly better for the high risk category (0.04) but had the same f1. In addition this model had a higher balanced accuracy score than previous models run.</li>   
       </ul>
   <li><strong>Adaboost Classifier</strong> <I>(See Example F below):</i> </li>
       <ul>
           <li>Balanced Accuracy Score: 0.93</li>
           <li>Precision: 0.99</li>
           <li>Recall: 0.94</li>
           <li>Notes: This model performed very similar to the Balanced Random Forest Classifier, but had an even higher Balanced Accuracy score at .93.</li>   
       </ul>
</ol>
<br>
 
The following are screenshot of the results as listed above:
<br>Example A: Random Oversampling<br>
![Random Oversampling](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/Random_Oversampling.png?raw=true)
 
<br>Example B: SMOTE Oversampling<br>
![SMOTE Oversampling](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/SMOTE_oversampling.png?raw=true)
 
<br>Example C: Cluster Centroids Algorithm<br>
![Cluster Centroids Algorithm](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/Cluser_Centroids.png?raw=true)
 
<br>Example D: SMOTEEN<br>
![SMOTEEN](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/Smoteenn.png?raw=true)
 
<br>Example E: Balanced Random Forest Classifier<br>
![Balanced Random Forest Classifier](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/Balanced_Random_Forrest_Classifier.png?raw=true)
 
<br>Example F: AdaBoost Classifier<br>
![Adaboost Classifier](https://github.com/jmmadson/Credit_Risk_Analysis/blob/main/Images/adaboost_classifier.png?raw=true)
 
 
## Summary:
 
Out of all the models, the Ensemble models performed the most effectively. The AdaBoost model  specifically performed the best, with a higher balance accuracy score, precision, recall and F1 scores over all the other models.
 
None of the models were effective at determining if the credit risk was high, which is shown through the classification report scores for precision and F1 scores for high_risk. Due to the low precision score for high credit risk incorrectly flagging low risk credit applications as high risk, the bank may miss out on additional interest and income from those applicants.
 
For that reason, I'd advise the bank to not use any of these models for prediction, to find additional ways to assess risk in lending.
