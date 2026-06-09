# Employee Attrition Prediction using Machine Learning

## Project Overview

Employee attrition is a major challenge for organizations as it impacts productivity, recruitment costs, and overall business performance. This project aims to predict whether an employee is likely to leave the company using Machine Learning techniques.

The project follows a complete end-to-end Machine Learning workflow including data preprocessing, exploratory data analysis (EDA), handling class imbalance, model training, threshold optimization, and performance evaluation.

---

## Objectives

* Identify employees who are likely to leave the organization.
* Analyze factors contributing to employee attrition.
* Build a predictive model to assist HR teams in employee retention strategies.
* Optimize classification thresholds based on business requirements.

---

## Dataset

The dataset contains employee-related information such as:

* Age
* Monthly Income
* Job Role
* Business Travel
* Overtime
* Years at Company
* Work-Life Balance
* Job Satisfaction
* Attrition (Target Variable)

Target Variable:

* 0 → Employee Stays
* 1 → Employee Leaves

---

## Project Workflow

### 1. Data Preprocessing

* Removed irrelevant features
* Handled categorical variables
* Applied feature encoding
* Prepared data for model training

### 2. Exploratory Data Analysis (EDA)

Performed analysis to understand:

* Attrition distribution
* Overtime impact on attrition
* Income vs attrition
* Job role trends
* Age distribution
* Business travel impact

### 3. Handling Class Imbalance

The dataset was highly imbalanced.

To address this issue:

* Applied SMOTE (Synthetic Minority Oversampling Technique)
* Generated synthetic samples for the minority class
* Improved model learning for attrition cases

### 4. Feature Scaling

Used StandardScaler to normalize numerical features before model training.

### 5. Model Training

Algorithm Used:

* Logistic Regression

Pipeline:

Train-Test Split
→ SMOTE
→ StandardScaler
→ Logistic Regression
→ Probability Prediction
→ Threshold Optimization

---

## Threshold Optimization

Instead of using the default threshold of 0.50, Precision-Recall analysis was performed.

### Why?

Logistic Regression produces probabilities.

Example:

* 0.20 → Low attrition risk
* 0.75 → High attrition risk

Using Precision-Recall Curve:

* Precision
* Recall
* F1 Score

were calculated across multiple thresholds.

The threshold producing the highest F1 Score was selected as the optimized threshold.

---

## Model Evaluation

Metrics Used:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix
* Cross Validation

---

## Results

### Threshold = 0.60

* Accuracy ≈ 87.8%
* Precision ≈ 72%
* Recall ≈ 38%
* F1 Score ≈ 50%

Suitable when high-confidence predictions are required.

---

### Optimized Threshold ≈ 0.43

* Accuracy ≈ 84%
* Precision ≈ 50%
* Recall ≈ 51%
* F1 Score ≈ 51%

Suitable when identifying more potential attrition cases is important.

---

## ROC-AUC Performance

* Test ROC-AUC ≈ 0.76
* Cross Validation ROC-AUC ≈ 0.83

These results indicate that the model has good ability to distinguish between employees likely to leave and those likely to stay.

---

## Key Learnings

* Handling imbalanced datasets using SMOTE
* Logistic Regression for binary classification
* Precision-Recall tradeoff
* Threshold Optimization
* ROC-AUC evaluation
* Cross Validation for model stability
* End-to-End Machine Learning workflow

---

## Conclusion

A Logistic Regression model was successfully developed to predict employee attrition.

The project demonstrates:

* Data preprocessing
* Exploratory Data Analysis
* Class imbalance handling
* Model training
* Threshold optimization
* Model evaluation

The developed solution can assist HR teams in identifying employees at risk of leaving and enable proactive retention strategies.
