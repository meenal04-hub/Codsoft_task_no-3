Customer Churn Prediction

Introduction

Customer churn refers to the phenomenon of customers discontinuing their relationship with a company. For businesses, retaining customers is more cost-effective than acquiring new ones, making churn prediction a critical aspect of customer relationship management (CRM).

This project focuses on building a machine learning model to predict customer churn based on historical customer data. The objective is to identify customers at risk of leaving so businesses can take proactive steps to retain them.

The dataset used in this project includes customer demographics, account information, and service usage patterns. The problem is framed as a binary classification task where the goal is to classify whether a customer will churn or not.

About the Model
This project implements a predictive model using machine learning techniques. Below is an overview of the pipeline:

1. Dataset
The dataset used for this project includes:

Demographics: Age, gender, and location of customers.

Service Features: Subscription plans, monthly charges, and contract type.

Usage Patterns: Data consumption, call duration, and payment history.

Churn Indicator: A binary label (1 for churn, 0 for non-churn).

2. Data Preprocessing

Missing Values: Imputation techniques applied to handle missing or incomplete data.

Encoding: Categorical variables (e.g., gender, contract type) encoded using one-hot or label encoding.

Feature Scaling: Numerical features like monthly charges and tenure normalized for consistency.

Train-Test Split: The data was split into training and testing sets (80%-20%).

3. Exploratory Data Analysis (EDA)

Key insights were derived from the data, such as:

The correlation between tenure and churn likelihood.
Higher churn rates among customers with month-to-month contracts.
Importance of payment methods and customer demographics.

4. Model Selection

The following machine learning models were evaluated:

Logistic Regression: A simple baseline for binary classification.

Decision Tree Classifier: To capture non-linear relationships.

Random Forest Classifier: A robust ensemble method for better accuracy.

Gradient Boosting (e.g., XGBoost, LightGBM): Known for excellent performance on tabular data.

Neural Networks: Applied to explore deep learning capabilities.

5. Evaluation Metrics

Given the business implications of misclassifying churners, the following metrics were prioritized:

Precision: To minimize false positives (incorrectly labeling customers as churners).

Recall: To ensure most actual churners are identified.

F1 Score: A balance between precision and recall.

ROC-AUC: To evaluate the model's performance comprehensively.

6. Results

The best-performing model achieved:

Model: Gradient Boosting

Precision:  0.7287
Recall: 0.4580
F1 Score:  0.5625
Accuracy: 0.8600

7. Feature Importance

Feature importance analysis revealed the key drivers of churn, such as:

Contract type (e.g., month-to-month).
Monthly charges and payment method.
Service usage patterns and customer tenure.

8. Deployment

The final model is integrated into a pipeline for real-time predictions. Deployment includes:

Building an API using Flask or FastAPI for serving predictions.
Creating dashboards for business stakeholders to monitor churn metrics.
