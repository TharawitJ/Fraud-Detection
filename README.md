**Credit Fraud project** to classify fraud and non-fraud.
https://www.kaggle.com/code/tharawitj/frauddetection-nearmiss-smote
---
### CRISP-DM processes for data mining.
1. Business Understanding
    * Credit fraud happened by information or credit card stolen and cause problems to bank's reputation, cost to investigate and financial Losses.
    * Both fraud and non fraud need to be predicted correctly and fast for the most satisfying customers. 

2. Data Understanding
    * 1081 duplicate rows and 19 of them are fraud.
    * No missing value.
    * Frauds are 0.17% of dataset (Imbalance).
    * Do simple undersampling to more understand in datasets by heatmap correlation.
    * Confirmed most of fraud are outlier in both negative and positive correlation features.

3. Data Preparation
    * Scale data by Robust that less prone to outliers.
    * StratifiedKFold for split datasets to 5 fold.
    * Undersampling by NearMiss.
    * Oversampling by SMOTE.

4. Modeling
    * Train model with NearMiss and SMOTE datasets.
    * Select 4 models for classify.
        1. Logistic Regression 
        2. SVC (Support Vector Classifier)
        3. Decision Tree Classifier
        4. XGB Classifier

5. Evaluate Model
    * Plot Learning Curve to observe overfitting.
        * Logistic Regression and SVC are good fitting.
    * Try to improve by GridSearchCV for hyperparameter tuning.
    * NearMiss (scores are average by fraud and non fraud)
        * Logistic Regression : average precision 96% and average recall 96%, ROC-AUC 94.3%.
        * SVC : average precision 97% and average recall 97%, ROC-AUC 96.3%.
    * SMOTE (scores are average by fraud and non fraud)
        * Logistic Regression : average precision 95% and average recall 95%, ROC-AUC 94.7%.
        * SVC : I decide to not train this model with SMOTE because it too expensive.

    * in Conclusion both SVC and Logistic Regression are good in accuracy result but big different on run-time, Logistic Regression is much more faster so I decide to using this model.

6. Deployment
    * We can use the created model for fraud detection that fast enough to be close to real-time.
---
References:
https://www.kaggle.com/code/janiobachmann/credit-fraud-dealing-with-imbalanced-datasets
