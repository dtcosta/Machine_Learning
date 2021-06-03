# Risky Business

![Credit Risk](Images/credit-risk.jpg)

## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you will need to employ different techniques for training and evaluating models with imbalanced classes. You will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:


#### Resampling

### Process:

1. Read the CSV into a DataFrame. 
2. Split the data into Training and Testing sets. 
3. Scale the training and testing data using the `StandardScaler` from `sklearn.preprocessing`. 
4. Use the provided code to run a Simple Logistic Regression:
    * Fit the `logistic regression classifier`.
    * Calculate the `balanced accuracy score`.
    * Display the `confusion matrix`.
    * Print the `imbalanced classification report`.

Next:

1. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.
2. Undersample the data using the `Cluster Centroids` algorithm.
3. Over- and undersample using a combination `SMOTEENN` algorithm.


For each of the above:

1. Train a `logistic regression classifier` from `sklearn.linear_model` using the resampled data.
2. Calculate the `balanced accuracy score` from `sklearn.metrics`.
3. Display the `confusion matrix` from `sklearn.metrics`.
4. Print the `imbalanced classification report` from `imblearn.metrics`.


### Questions and Conclusions:

* Which model had the best balanced accuracy score?

    **Simple Logistic Regression balanced accuracy score0.9543211898288821**
    **Naive Random Oversampling balanced accuracy score 0.9934649587814939**
    **SMOTE Oversampling balanced accuracy score 0.9936781215845847**
    **Undersampling balanced accuracy score 0.8099934699520943**
    **Combination balanced accuracy score 0.9935715401830394**
    **The best balanced accuracy score was SMOTE but it is notable that SMOTE, Naive and Combination all had scores of higher than the simple logistic regression.**
    
* Which model had the best recall score?

    **Simple Logistic Regression recall score .99**
    **Naive Random Oversampling balanced recallscore .99**
    **SMOTE Oversampling balanced recall score .99**
    **Undersampling balanced recall score .64**
    **Combination balanced recall score .99**
    **All of the models with the exception of undersampling have a recall score of .99**

* Which model had the best geometric mean score?
    **Simple Logistic Regression geo score .95**
    **Naive Random Oversampling geo score .99**
    **SMOTE Oversampling geo score .99**
    **Undersampling geo score .79**
    **Combination geo score .99**
    **Naive random, SMOTE and combination all have a geo score of .99**
    
#### Ensemble Learning

### Process:

1. Read the data into a DataFrame using the provided starter code.
2. Split the data into training and testing sets.
3. Scale the training and testing data using the `StandardScaler` from `sklearn.preprocessing`.


Then, for each model:

1. Train the model using the quarterly data from LendingClub provided in the `Resource` folder.
2. Calculate the balanced accuracy score from `sklearn.metrics`.
3. Display the confusion matrix from `sklearn.metrics`.
4. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.
5. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.


### Questions and Conclusions:

* Which model had the best balanced accuracy score?

    **Random Forest accuracy score .78**
    **Easy ensemble accuracy score of .93**
    **Easy ensemble has the best balanced accuracy score.**
    
* Which model had the best recall score?

    **Random Forest recall score .87**
    **Easy ensemble recall score of .94**
    **Easy ensemble has the best recall score.**
    
* Which model had the best geometric mean score?

    **Random Forest geo mean score .78**
    **Easy ensemble geo mean score of .93**
    **Easy ensemble has the best geo mean score.**

* What are the top three features?

    **total_rec_prncp 0.078768**
    **total_pymnt 0.058838**
    **total_pymnt_inv 0.056256**
