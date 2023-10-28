# ML-Project
Based on the credit card fraud detection analysis, here is a summary report:

# Problem Statement

The objective is to build a model to detect fraudulent credit card transactions using a dataset of 284,807 transactions with 30 anonymous features and a label indicating fraud or not. The data has a high class imbalance with only 0.172% fraudulent transactions.

# Data Exploration

- The dataset contains 31 columns - Time, 30 anonymous features V1 to V28, Amount, and Class
- No missing values 
- 'Amount' and 'Time' features normalized using MinMaxScaler
- Highly imbalanced classes - Only 492 fraud cases out of 284,807 (0.172%)

# Models Compared

- Logistic Regression
- Decision Tree
- Random Forest 
- Support Vector Machine (SVM)

Models evaluated on undersampled data and oversampled data using SMOTE.

# Key Results

- Random Forest best overall performance on oversampled data
  - Accuracy: 99.96%
  - Precision: 90.59%
  - Recall: 84.62%
  - F1-score: 87.50%
  - AUPRC (area under precision-recall curve): 76.68%

- Oversampling improved model metrics compared to undersampling

- Important features identified using RF feature importance - V12, V14, V11, V4

# Recommendations

- Use Random Forest model for fraud detection
- Use oversampling techniques like SMOTE to handle class imbalance
- Retrain model periodically on new data
- Tuning hyperparameters like n_estimators, max_depth could further improve performance
- Reduce false negatives by tuning threshold based on business costs
