# Case Study: Fraud Detection Using Machine Learning

## Introduction

Fraudulent transactions pose a significant risk in financial systems, making fraud detection a critical area of research. In this study, we apply machine learning techniques to analyze transaction data, identify patterns associated with fraudulent activities, and improve the accuracy of fraud detection.

## Objective

The primary objective of this study is to develop a robust fraud detection model by leveraging feature selection, clustering techniques, and resampling strategies to address class imbalance.

## Data Overview

The dataset consists of anonymized financial transactions with features such as transaction amount, time, and engineered variables (V1-V28). The key challenge in this dataset is the extreme imbalance, where fraudulent transactions make up a very small percentage of the total data.

[Dataset Link](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

## Data Preprocessing

- Handling Missing Values

- No missing values were found in the dataset.

## Feature Engineering

- Extracted hour-based features from the transaction time column.

- Normalization

- Applied Standard Scaler to standardize features such as transaction amount.

- Class Balancing

- Used Random UnderSampling (RUS) to balance the dataset, ensuring fair model training.

## Exploratory Data Analysis (EDA)

1. Correlation Analysis

  - A heatmap was used to identify highly correlated features. The most correlated variables with fraud transactions were:

    - V17
    - V14
    - V12
    - V10
    - V16
    - V3

2. Fraud Distribution by Time

  - Fraudulent transactions were analyzed across different time periods, revealing that a significant portion of fraud occurs during non-peak hours (late night and early morning).

3. Clustering Fraudulent Transactions

  - K-Means clustering was performed on high-impact features (V17 and V14) to identify different fraud transaction patterns. The fraud transactions were grouped into three distinct clusters:

    - Cluster 0: High-value fraudulent transactions.

    - Cluster 1: Mid-range fraudulent transactions with moderate feature deviations.

    - Cluster 2: Low-value fraudulent transactions with significant anomalies.

## Modeling Approach

- Baseline Models

    - Logistic Regression and Decision Tree were initially used to assess performance.

- Advanced Models

  - Random Forest and XGBoost were implemented for improved accuracy.

## Evaluation Metrics

Since fraud detection is a highly imbalanced classification problem, precision, recall, and F1-score were used instead of accuracy to evaluate models.

## Results & Insights

- Clustering helped in understanding different types of fraudulent activities, aiding model explainability.

- Undersampling effectively improved fraud detection rates but required careful tuning to avoid loss of key transaction patterns.

- XGBoost outperformed other models in fraud detection, achieving the best balance between precision and recall.

## Conclusion

- This study highlights the importance of combining machine learning, clustering, and class balancing techniques to enhance fraud detection. The insights gained from the analysis can help financial institutions strengthen their fraud prevention strategies and improve transaction security.

## Future Work
Incorporating real-time transaction monitoring with adaptive learning models.

