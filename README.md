# Module 20 Supervised Machine Learning Report

## Overview of the Analysis

The goal of this analysis was to develop and evaluate a machine learning model to predict the creditworthiness of borrowers. By analyzing historical loan data, I aimed to classify loans into two categories:
- `0`: Healthy loans, indicating a low risk of default.
- `1`: High-risk loans, indicating a high likelihood of default.

The dataset provided financial information on borrowers and their loans. My objective was to use this data to predict whether a loan would fall into the healthy or high-risk category.

### Data Information:
- **Target Variable**: `loan_status` (0 for healthy loans, 1 for high-risk loans).
- **Features**: The remaining columns in the dataset, which included various borrower financial metrics.

### Machine Learning Process:
This analysis involved the following stages:
1. **Data Preparation**:
   - The dataset was split into training and testing subsets using `train_test_split`.
   - The training data was used to build a logistic regression model to classify loans.
2. **Model Training**:
   - A `LogisticRegression` model was trained on the training data.
3. **Model Evaluation**:
   - The model's performance was assessed using a confusion matrix and a classification report, which provided metrics such as accuracy, precision, recall, and F1-score.

---

## Results

### Logistic Regression Model
- **Accuracy**: 99%
- **Precision**:
  - `0` (Healthy loans): 1.00
  - `1` (High-risk loans): 0.86
- **Recall**:
  - `0` (Healthy loans): 0.99
  - `1` (High-risk loans): 0.94
- **F1-Score**:
  - `0` (Healthy loans): 1.00
  - `1` (High-risk loans): 0.90

The results indicate that the model is highly accurate overall, with strong performance in predicting healthy loans (`0`). The model’s precision and recall for high-risk loans (`1`) were slightly lower, reflecting minor misclassifications.

---

## Summary

The logistic regression model demonstrated strong performance, achieving an accuracy score of 99%. It was highly effective at predicting healthy loans (`0`), with perfect precision and a recall of 0.99. For high-risk loans (`1`), the model performed well, but its precision (0.86) suggests that it sometimes misclassified healthy loans as high-risk. However, its recall (0.94) indicates that it successfully identified the majority of high-risk loans.

### Recommendation:
This model is suitable for applications where identifying high-risk loans is critical, as it achieves high recall for the `1` category. However, its lower precision for high-risk loans may lead to unnecessary caution in lending decisions. For scenarios requiring a greater emphasis on precision, further model tuning or exploration of alternative algorithms could be beneficial. Overall, the logistic regression model is a strong candidate for deployment with minimal adjustments.
