# Credit Risk Classification 

## Overview

This project aims to analyze credit risk by classifying loans as either healthy (0) or high-risk (1) using a logistic regression model. The dataset includes financial attributes such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.

## Data Processing

* The dataset was split into training (80%) and testing (20%) sets using train_test_split.

* The target variable (loan_status) was used as the label (y), while all other features were used as predictors (X).

* Due to class imbalance (more healthy loans than high-risk loans), performance metrics beyond accuracy were considered.

## Model Training

* A Logistic Regression model was instantiated with random_state=1 and trained using the training dataset.

* The model was evaluated on the testing dataset using standard classification metrics.

## Model Evaluation

### Confusion Matrix

```
[[14953    55]
[   41   459]]
```

### Classification Report

```
precision    recall  f1-score   support

       0       1.00      1.00      1.00     15008
       1       0.89      0.88      0.88       500

accuracy                           0.99     15508

macro avg       0.94      0.94      0.94     15508
weighted avg       0.99      0.99      0.99     15508
```

## Summary & Recommendations

* The model performs exceptionally well in predicting healthy loans (0), achieving 100% precision and recall.

* For high-risk loans (1), the model has 89% precision and 88% recall, meaning it correctly identifies most high-risk loans but still misses 12% of them.

* Accuracy: 99%, but due to class imbalance, focusing on recall for high-risk loans is essential.

* If further improvement is needed, class balancing techniques (e.g., oversampling, undersampling) or alternative models (e.g., Random Forest, XGBoost) could be explored.

## Installation & Usage

1. Install dependencies:`pip install pandas scikit-learn`

2. Load the dataset (lending_data.csv) into a pandas DataFrame.

3. Run the logistic regression training script to generate predictions.

4. Evaluate the model using the provided performance metrics.
#


This README provides a high-level summary of the Credit Risk Classification project, ensuring clarity for future reference and potential improvements.