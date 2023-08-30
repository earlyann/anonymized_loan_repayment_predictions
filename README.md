## Loan Repayment Prediction and Analysis

### Project Overview
The objective of this project is to predict whether a customer will fail to repay their loans based on various factors such as employment length, loan purpose, annual income, income verification status, etc. Additionally, the project aims to provide an exploratory data analysis (EDA) of the loan data and its associated attributes, and a model interpretation using SHAP (SHapley Additive exPlanations) values instead of traditional feature importance.

The dataset contains various attributes like loan amount, funded amount, interest rate, installment, employment length, home ownership, annual income, verification status, issue date, loan status, purpose, zip code, address state, DTI (Debt-to-Income) ratio, delinquency of 2 years, earliest credit line, inquiries in the last 6 months, months since last delinquency, open accounts, public records, revolving balance, revolving utilization, total accounts, total payment, total payment inv, total received principal, total received interest, last payment date, last payment amount, next payment date, last credit pull date, and repayment failure.

### Technologies Used
- Python: The primary programming language used for data analysis, data visualization, and model building.
- Tableau: A data visualization tool used for creating an interactive dashboard that explores the data and the anonymized people data it contains.
- CatBoost: A gradient boosting library that is particularly efficient and effective for categorical data. Used for building the classification model.
- SHAP: A Python library that uses Shapley values from game theory to provide a unified measure of feature importance.
Data Exploration

The first step involves understanding the data and its various attributes. A Tableau dashboard is created to visually explore the data, which includes the anonymized people data like how long they have been employed, what the loan was for, annual income, whether the income was verified, etc.

### Model Building
A CatBoost classification model is trained using the available data to predict whether a customer will fail to repay their loans. CatBoost is particularly suitable for this task due to its capability to handle categorical data efficiently.

### Model Interpretation
The CatBoost model provides feature importances that indicate the global importance of features in predicting the target variable across the entire dataset. However, to provide a more detailed and fair interpretation, both locally and globally, SHAP values are used instead of traditional feature importance. SHAP values have two key properties:
- Local Interpretability: For each instance (or row) in the dataset, SHAP values explain the difference between the model's prediction for that instance and the average prediction for all instances. This helps to understand the model's prediction for a single instance.
- Global Interpretability: By aggregating SHAP values for all instances, you can also get a global measure of feature importance. This helps to understand the overall model behavior across the entire dataset.

### Next Steps
Model Deployment: Deploy the model as a web application or API that can predict loan repayment failure for new customers.
User Interface: Develop a user-friendly interface for the web application that allows users to input their data and get a prediction on their loan repayment ability.
Conclusion
This project provides a comprehensive analysis of loan data and builds a predictive model to determine the loan repayment ability of a customer. The use of SHAP values for model interpretation provides a more detailed and fair distribution of feature importance, both locally and globally, enhancing the model's interpretability and trustworthiness.





