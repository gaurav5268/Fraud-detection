# Fraud-detection
<<<<<<< HEAD
## Overview

This project focuses on building a machine learning model to detect fraudulent financial transactions

The objective is to help financial institutions:

    Reduce financial losses

    Detect fraud proactively

    Improve customer trust and safety

    The project follows a complete end-to-end data science workflow

    Business Problem

    Fraudulent transactions are rare but cause significant financial damage

    Manual fraud detection systems are slow and error-prone

    An automated predictive system is required to:

    Identify suspicious transactions early

    Reduce the number of missed fraud cases

    Avoid blocking genuine customers unnecessarily

Dataset

Format: CSV file

Size: Approximately 6.3 million rows

Target column:

isFraud

1 = Fraud

0 = Not Fraud

Important features include:

Transaction amount

Transaction type

Origin account balance

Destination account balance

System-flagged fraud indicator

Data Preprocessing

Checked dataset for missing values (none found)

Treated outliers by capping extreme transaction amounts

Performed correlation analysis to understand relationships between variables

Handled multicollinearity using a tree-based model (Random Forest)

Converted categorical feature (type) into numerical form using one-hot encoding

Created additional meaningful features such as:

Origin balance change

Destination balance change

Approach

Split the data into training and testing sets using stratified sampling

Built a Random Forest classification model

Used probability-based predictions instead of only class labels

Tuned the prediction threshold to 0.3 instead of 0.5 to improve fraud detection (recall)

Evaluated model using appropriate metrics for imbalanced data

Model Used

Random Forest Classifier

Chosen because:

It handles non-linear relationships well

It performs effectively on large datasets

It is robust to multicollinearity

It provides feature importance for interpretation

Model Evaluation

Since fraud data is highly imbalanced, accuracy alone is not reliable

Model evaluated using:

Confusion Matrix

Precision

Recall

F1-score

ROC-AUC

Greater importance was given to Recall to ensure fewer fraud cases are missed

Threshold Tuning

Default threshold (0.5) was changed to 0.3

This helps:

Catch more fraudulent transactions

Improve the model’s sensitivity to fraud

Simulate real-world cost-sensitive decision making

Model Saving

The trained model is saved as:

fraud_rf_model.pkl

This allows the model to be reused later without retraining

Key Insights

The model identified strong fraud indicators such as:

High transaction amounts

Transaction types like TRANSFER and CASH_OUT

Sudden abnormal balance changes

Inconsistent transaction behavior patterns

Outcome

The model successfully learns meaningful fraud patterns

It can distinguish between normal and suspicious transactions

Demonstrates a practical and industry-relevant fraud detection pipeline
=======
>>>>>>> a01e9d1560ce6faae731d48ddec265bd0bab153c
