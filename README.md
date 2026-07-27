# 🛡️ Fraud Detection Using Machine Learning

## Overview

Financial fraud costs banks and fintech companies millions of dollars each year. Traditional rule-based detection systems often struggle to identify new fraud patterns and generate large numbers of false alerts.

This project develops and evaluates multiple machine learning models capable of identifying fraudulent transactions while minimizing false positives and false negatives. The objective is to support fraud analysts by automatically prioritizing high-risk transactions for investigation.

---

## Business Problem

Manual fraud detection is:

* Time-consuming
* Costly
* Difficult to scale
* Unable to detect evolving fraud patterns quickly

A predictive fraud detection model enables financial institutions to:

* Detect suspicious transactions in real time
* Reduce financial losses
* Improve customer trust
* Increase operational efficiency

---

## Project Objectives

* Perform exploratory data analysis (EDA)
* Clean and preprocess transaction data
* Handle missing values and duplicate records
* Engineer and prepare features for modeling
* Train and compare multiple machine learning algorithms
* Evaluate models using fraud-specific metrics
* Improve model performance through hyperparameter tuning

---

## Dataset

The dataset contains transaction-level information used to classify whether a transaction is fraudulent.

### Target Variable

* **is_fraud**

  * 0 = Legitimate Transaction
  * 1 = Fraudulent Transaction

The dataset is imbalanced, with legitimate transactions significantly outnumbering fraudulent ones. Because of this, evaluation focuses on Precision, Recall, F1-score, and ROC-AUC instead of relying solely on accuracy.

---

## Exploratory Data Analysis

The analysis included:

* Dataset overview
* Summary statistics
* Missing value analysis
* Duplicate detection and removal
* Distribution of numerical variables
* Correlation analysis
* Fraud class distribution
* Feature relationship analysis

### Key Findings

* The dataset is highly imbalanced.
* Merchant Risk Score shows a strong relationship with fraudulent transactions.
* Previous Fraud Flag is also an important predictor.
* Duplicate observations were removed to prevent model bias.

---

## Data Preprocessing

The preprocessing pipeline included:

* Removal of duplicate records
* Conversion of object columns into numeric values
* Missing value handling
* Feature scaling
* Data splitting into training and testing datasets

Scikit-learn preprocessing pipelines were used to ensure reproducibility.

---

## Machine Learning Models

The following classification algorithms were evaluated:

* Logistic Regression
* Random Forest
* Gradient Boosting
* Support Vector Machine (SVM)
* XGBoost
* LightGBM

---

## Model Evaluation

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC Score

Because fraud detection is an imbalanced classification problem, ROC-AUC, Precision, and Recall were the primary evaluation metrics.

---

## Cross Validation

A 5-fold Stratified Cross Validation was performed using ROC-AUC.

### Key Result

Among the evaluated models:

* **Logistic Regression achieved the highest mean ROC-AUC (≈0.829)** while maintaining one of the lowest standard deviations across folds, demonstrating strong and consistent generalization performance.

---

## Hyperparameter Tuning

GridSearchCV was used to optimize the following models:

* Logistic Regression
* Gradient Boosting
* LightGBM

The best-performing configurations were selected using ROC-AUC as the optimization metric.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* LightGBM

---

## Project Structure

```text
Fraud-Detection/
│
├── Fraud Detection.ipynb
├── README.md
├── requirements.txt
└── data/
    └── credit_fraud.csv
```

---

## Future Improvements

Potential enhancements include:

* Feature engineering for transaction behavior
* Handling class imbalance using SMOTE or class weighting
* Threshold optimization for fraud detection
* Model explainability using SHAP
* Deployment as a REST API
* Real-time fraud scoring pipeline

---

## Key Takeaways

* Built an end-to-end fraud detection pipeline from data cleaning to model evaluation.
* Compared multiple machine learning algorithms for fraud classification.
* Used cross-validation and hyperparameter tuning to improve model robustness.
* Focused on business-relevant metrics appropriate for highly imbalanced datasets.

---

## Author

**Samuel Bentum**

Data Analyst | Credit Risk & Portfolio Analytics

**Skills:** SQL • Python • Machine Learning • Power BI • Excel • Data Visualization

LinkedIn: *Add your LinkedIn URL*

GitHub: *Add your GitHub URL*

