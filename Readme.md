**Credit Fraud project** to classify fraud and non-fraud.
---
### CRISP-DM processes for data mining.
1. Business Understanding
    * Credit fraud happened by information or credit card stolen and cause problems to bank's reputation, cost to investigate and financial Losses.
    * This project credit fraud aim to classify fraud and can improve to fraud detection in the future.

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
    * Plot learning Curve to observe overfitting.
        * Logistic Regression and SVC are good fitting.
    * Try to improve by GridSearchCV for hyperparameter tuning.
    * Logistic Regression high score by precision and recall, ROC-AUC and much more inexpensive(faster) with SMOTE compare to SVC.

6. Deployment
    * We can use the created model for fraud detection that fast and can be close to real-time.