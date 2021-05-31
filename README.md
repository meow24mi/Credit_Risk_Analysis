# Credit Risk Analysis

## Overview
Assessing credit risk using imbalanced-learn and scikit-learn libraries to build and evaluate models using various resampling methods. 

## Results
* Random Oversampling
    * Accuracy: 0.66
    * High Risk
        * Precision 0.01
        * Recall 0.66

![Random Oversampling](Resources/Random_Oversampling.png)
* SMOTE Oversampling
    * Accuracy: 0.63
    * High Risk
        * Precision 0.01
        * Recall 0.62

![SMOTE Oversampling](Resources/SMOTE_Oversampling.png)
* Cluster Centroids Undersampling
    * Accuracy: 0.52
    * High Risk
        * Precision 0.01
        * Recall 0.61

![Cluster Centroids Undersampling](Resources/Cluster_Centroids_Undersampling.png)
* SMOTEEN (Combination Sampling)
    * Accuracy: 0.63
    * High Risk
        * Precision 0.01
        * Recall 0.71

![SMOTEEN (Combination Sampling)](Resources/SMOTEEN_Combination_Sampling.png)
* Balanced Random Forest Classifier
    * Accuracy: 0.78
    * High Risk
        * Precision 0.04
        * Recall 0.67

![Balanced Random Forest Classifier](Resources/Balanced_Random_Forest_Classifier.png)
* Easy Ensemble Classifier
    * Accuracy: 0.92
    * High Risk
        * Precision 0.07
        * Recall 0.91

![Easy Ensemble Classifier](Resources/Easy_Ensemble_Classifier.png)
## Summary

### Accuracy
As displayed in the images above, the two methods of oversampling and the two methods of underoversampling yield poor accuracy. The accuracy ranged from 0.52 to 0.66. The combination sampling, SMOTEEN yielded a accuracy of 0.78, and the Balanced Random Forest Classifier yielded an accuracy of 0.92. However, each of these sampling methods have widly different support for the high_risk class as well as the low_risk class. Due to this highly imbalanced dataset, the accuracy is deemed less meaningful. 

### Precision
The two methods of oversampling and the two methods of undersampling all yielded low precision at 0.01. SMOTEEN (Combination Sampling) had a precision of 0.04 and Easy Ensemble Classifier had a precision of 0.07. Low precision indicates a high number of false positives. In our instance, labling a loan high risk, while it's low risk. 

### Recall
The recall ranges from 0.52 to 0.91. The higher the recall/sensitivity, the lower the number of false negatives. In otherwords, all the sampling methods had a higher sensitivity than precision. Easy Ensemble Classifier had the highest recall at 0.91; and the sensitive sensitive at keeping false negatives low.

### Recommendation
I recommend using the Easy Ensemble Classifier method because it has the highest sensitivty of all the sampling methods and the highest accuracy. It will maximize loan profits and minimize risks to the lender. 