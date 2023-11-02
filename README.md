# Loan Risk Analysis

## Overview 

In this analysis, I aimed to build machine learning models to predict the creditworthiness of borrowers based on historical lending activity data from a peer-to-peer lending services company. The primary purpose of this analysis was to assess the risk associated with loans and develop models that can distinguish between healthy loans (`0`) and high-risk loans (`1`).

### Data Description

The data used for this analysis was stored in the "lending_data.csv" file, which contained financial information about loans. The key task was to predict the "loan_status" of each loan, which consits of two classes: `0` for healthy loans and `1` for high-risk loans.

Key variables we were trying to predict:
- `loan_status`: The target variable, which indicates whether a loan is healthy (`0`) or high-risk (`1`).

### Machine Learning Process

The analysis involved the following stages:

1. **Data Splitting**:
   - The dataset was read into a Pandas DataFrame from the "lending_data.csv" file.
   - Labels (y) were created from the "loan_status" column, and the features (X) DataFrame was created from the remaining columns.
   - The data was split into training and testing datasets using the `train_test_split` function.

2. **Model Training**:
   - A logistic regression model was fitted using the training data (X_train and y_train).

3. **Model Evaluation**:
   - Model performance was assessed by:
     - Generating a confusion matrix.
     - Printing the classification report, which included precision, recall, and F1-score for both healthy and high-risk loans.

4. **Oversampling**:
   - Oversampling techniques were applied to balance the dataset to compared to the original, as I dealing with imbalanced classes.

### Methods Used

The main machine learning method employed for this analysis was logistic regression. Additionally, oversampling techniques were used to address class imbalance.

## Results

The results of the machine learning models are summarized below:

### Machine Learning Model 1 (Original Data):
  - Balanced Accuracy: [Balanced Accuracy Score]
  - Precision for Healthy Loans (`0`): 1.00
  - Recall for Healthy Loans (`0`): 1.00
  - Precision for High-Risk Loans (`1`): 0.87
  - Recall for High-Risk Loans (`1`): 0.89

### Machine Learning Model 2 (Resampled Data):
  - Balanced Accuracy: 0.9952
  - Precision for Healthy Loans (`0`): 1.00
  - Recall for Healthy Loans (`0`): 1.00
  - Precision for High-Risk Loans (`1`): 0.87
  - Recall for High-Risk Loans (`1`): 1.00

## Summary

In summary, the machine learning models were built to assess loan risk, and their performance was evaluated. Depending on the specific problem to solve, the choice of the best-performing model may vary.

The choice of the best model depends on various factors, such as the specific problem at hand and the importance of predicting healthy loans (`0`) or high-risk loans (`1`). It is essential to consider the trade-off between precision and recall when making this decision. In general, the second, balaced model using the resampled data imporved as the recall score increased for the high-risk loan category. 

Overall, this analysis provides valuable insights into the creditworthiness of borrowers and helps make informed decisions regarding loan risk.
