# Personal_Loan_Modelling

## Description 
This is a project of personal loan modelling using Support Vector Machine (SVM) method. The SVM predictive technique will forecast whether individual customers accept the personal loan offer or not. This greatly improves the efficiency of marketing campaign as it classifies those are more possible to accpet the offer and so the organisation will likely to promote their loan service successfully by pivoting on target customers.

## Analytics Background
Capitalising on machine learning for loan prediction brings 3 main advantages for finanacial insititutions:

1. **Risk assessment precision:**
   - Analyse historical data and applicant features to predict loan default risk accurately.
   - Minimise losses by identifying low-risk applicants likely to accept loan offers.

2. **Targeted marketing optimisation:**
   - Tailor marketing strategies based on customer characteristics and behavioral preferences.
   - Enhance lead conversion rates by focusing efforts on qualified loan applicants.

3. **Resource allocation efficiency:**
   - Prioritise leads with high likelihood of conversion to optimise resource use.
   - Increase operational efficiency and reduce costs in sales and marketing efforts.

## Data Input and Preparation

### Feature names
| Age | Experience | Income | Zip code | Family | CCAvg | Education | Mortgage | Personal_loan | Security_account | Cd_account | Online | Creditcard |
|-----|------------|--------|----------|--------|-------|-----------|----------|---------------|------------------|------------|--------|------------|

### Data cleansing
Highlighting three essential data preparation steps for modelling out of the 13 features:

* Converting negative values in the 'Experience' column to positive using the 'Absolute Conversion' method to address data entry errors.
* Evaluating and managing input noise and outliers present in the 'ZIP Code' and 'Mortgage' features.
* Transforming 'ZIP Code' into 'Place', 'Latitude', and 'Longitude' to quantify location input for predictive modeling accuracy.

#### Note: You can find the dataset and feature explanations stored in the 'Data_sources' folder.

## Modelling

This section explores SVM modelling on feature preprocessing, fitting assessment, and model comparison. The purpose is to understand the impact of kernel use on classification accuracy and to identify any visible patterns influenced by hyperparameter changes. The tests reveal that SVM with the **radial basis function (RBF)** kernel achieves the best accuracy, ranging from **0.9650 to 0.9750**, which performs optimally when the hyperparameter **C=100.0**. Also, compared to the null accuracy of 0.8990, this model demonstrates excellent performance in predicting class labels.

## Evaluation and Fine-tuning

With thorough assessment shown below, the SVM model employs various methods to evaluate prediction performance on the testing set, ensuring reliability and validity of results. The linear kernel produces a higher average stratified k-fold cross-validation score of 0.9078. However, with a model accuracy of **0.9750**, it seems that the stratified cross-validation method doesn't notably improve performance. The best hyperparameters **{'C': 10, 'gamma': 0.1, 'kernel': 'rbf'}** are determined through grid search, securing a final accuracy of 0.9760 for the training set.

* Confusion Matrix
* Classification Metrics
* ROC - AUC
* Stratified k-fold Cross-Validation with Shuffle Split

## Results and Concludion
The testing set accuracy using the optimal hyperparameters also reached 0.9760. This means the model generalises well beyond the training set and demonstrates robust label prediction accuracy on unseen data. 
Based on this modeling, we draw the following conclusions:

- Some outliers, particularly in features like 'mortgage', are present in our dataset. Adjusting the value of C to decrease sensitivity to these outliers improves accuracy across various kernel types.

- The highest accuracy, at 0.9750, is obtained with an rbf kernel and C=100.0. However, this evaluation is flawed due to the imbalanced dataset, considering the drawbacks of accuracy as a sole metric. To address this, we adopt multiple assessment methods for a more comprehensive evaluation.

- While the original model attains a test accuracy of 0.9750, the GridSearch CV score on the test set slightly surpasses it at 0.9760. This underscores the advantage of GridSearch CV in identifying optimal parameters for levelling up performance.

---

## Contents

**Table of Contents**

1. **Library Import**
2. **Data Exploration**
   - 2.1 Data loading
   - 2.2 Pre-stage data visualisation
3. **Data Preparation**
   - 3.1 Missing values
   - 3.2 Negative values
   - 3.3 Noise and outliers
   - 3.4 Mid-stage data visualisation
   - 3.5 ZIP Code
     - 3.5.1 ZIP Code conversion
     - 3.5.2 Missing values
   - 3.6 Post-stage data visualisation
4. **Modelling**
   - 4.1 Feature vector & target variable
   - 4.2 Data splitting into training and testing sets
   - 4.3 Feature scaling
   - 4.4 SVM with default hyperparameters (RBF)
     - 4.4.1 Model training and accuracy check
     - 4.4.2 Evaluating model fit: overfitting and underfitting
     - 4.4.3 Performance assessment: Null accuracy
   - 4.5 SVM with linear kernel
   - 4.6 SVM with polynomial kernel
   - 4.7 SVM with sigmoid kernel
5. **Evaluation**
   - 5.1 Confusion matrix
   - 5.2 Classification metrics
   - 5.3 ROC - AUC
     - 5.3.1 ROC Curve
     - 5.3.2 ROC AUC
   - 5.4 Stratified k-fold Cross-Validation with shuffle split
   - 5.5 Hyperparameter optimisation with GridSearchCV
6. **Conclusion and results**
---

| Project                                                                                                                                           | Author           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Personal Loan Modelling SVM](https://github.com/Yuxi-Cn/Personal_Loan_Modelling/blob/main/Personal_Loan_Modelling_SVM.ipynb)                   | Yuxi Chen        |


#### Welcome to drop any comments to discuss further about this work!

