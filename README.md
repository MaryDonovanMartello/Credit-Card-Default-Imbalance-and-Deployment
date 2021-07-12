## Compare Imbalanced Data Approaches, Feature Engineering and Deployment

### Summary

This project includes adjustments and extentions to the a prior credit card defaults project located [here](https://github.com/MaryDonovanMartello/Credit-Card-Default-Prediction).  Phase 1 of the credit card default project involved testing five binary classification models for predicting credit card defaults.  This Phase 2 of the credit card defaults project includes (1) testing multiple approaches to addressing an imbalanced target variable in a binary classification model, (2) employing methodologies other than Principal Component Analysis to address multicollinearity and feature selection in an effort to be able to analyze individual factors that are significant for defaults, and (3) implementing deployment models to make actual predictions and convert the logistic regression coefficients to a risk score that can be used in making lending decisions. 

**Tools**

* Scikit-learn 
* imblearn
* Seaborn
* Matplotlib
* Numpy
* Pandas
* Scipy

**Data**

[UCI](http://archive.ics.uci.edu/ml) 

**Models / Methods / Metrics**

* Logistic Regression
* Receiver Operating Characteristic curve and Youden's J statistic for selecting classification threshold
* Resampling data to address imbalanced target
* Predictions
* Risk score
* Weight of Evidence and Information Value
* Recall

**Results**

Adjusting the probability classification threshold (without resampling the data) showed the best results for predicting pending defaults.  Feature engineering resulted in improved model metrics.  Two deployment tools were implemented:  (1) predictions of default and (2) a risk score for each account holder.

## Project Preview

### Feature Engineering

![Late](/images/Late.PNG)


### Comparison of Approaches to Imbalanced Target

![results](/images/ImbResults.PNG)


![rankings](/images/ImbRanking.PNG)


### Deployment:  Risk Scorecard

![ECD](/images/Scorecard.PNG)

**Notebooks**

1_EDA_Prep
This notebook includes the EDA and data preparation.

1_Panda_Profile
This notebook includes the EDA report produced from running the Panda Profile library.

2_Test_Subsets_of_Features
This notebook tests for best subsets of features with a logistic regression model.

3_OptimizeThreshold
This notebook approaches the imbalanced target in the dataset by making probability predictions to choose the best classification threshold for the imbalanced target.  

4_TrainTestSplitMethod
This notebook approaches the imbalanced target in the dataset by oversampling the training data after splitting the data with the holdout method.

5_GroupKFoldMethodRandomOver
This notebook approaches the imbalanced target in the dataset by oversampling the training data within Group K Fold for cross-validation.

6_imblearnPipelineOverCombined
This notebook approaches the imbalanced target in the dataset by oversampling the training data within an imblearn Pipeline.

7_imblearnPipelineOverUnder
This notebook approaches the imbalanced target in the dataset by both over and under sampling the training data within an imblearn Pipeline.

8_DeployModel
This notebook implements deployment models by making actual predictions and by converting the logistic regression coefficients to a risk score that can be used in making lending decisions.


