# credit-risk-classification
---
# Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

---
# Before You Begin
1. Create a new repository for this project called credit-risk-classification. Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Inside your credit-risk-classification repository, create a folder titled "Credit_Risk."
4. Inside the "Credit_Risk" folder, add the credit_risk_classification.ipynb and lending_data.csv files found in the "Starter_Code.zip" file.
5. Push your changes to GitHub.

---
# Files
Download the following files to help you get started:
- [Module 20 Challenge files](https://static.bc-edx.com/data/dl-1-2/m20/lms/starter/Starter_Code.zip)

---
# Instructions
The instructions for this Challenge are divided into the following subsections:
  - Split the Data into Training and Testing Sets
  - Create a Logistic Regression Model with the Original Data
  - Write a Credit Risk Analysis Report

# Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:
  1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
  2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

*Note* : A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
  
  3. Split the data into training and testing datasets by using train_test_split.

# Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:
  1. Fit a logistic regression model by using the training data (X_train and y_train).
  2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
  3. Evaluate the model’s performance by doing the following:
    - Generate a confusion matrix.
    - Print the classification report.
  4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

# Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
1. **An overview of the analysis:** Explain the purpose of this analysis.
2. **The results:** Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
3. **A summary:** Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

---

# **Credit Risk Analysis Report**

# Overview
The goal of this analysis was to build a machine learning model that could predict whether a loan was high-risk or healthy based on financial data. The dataset included features like loan size, interest rate, income, and debt-to-income ratio. We were trying to figure out if we could spot risky loans early to help lenders make better decisions.

To start off, I looked at the target variable (`loan_status`) and noticed that most of the loans were healthy, so the data was imbalanced. I preprocessed the data by scaling it and split it into training and test sets to make sure the model would generalize well.

For this challenge, I used the `LogisticRegression` model because it's good for binary classification problems like this. After training it, I evaluated how well it did using accuracy, precision, recall, and F1-score.

![image](https://github.com/user-attachments/assets/116e87d9-a10b-4927-b332-bafadfb95712)
* Machine Learning Model 1: Logistic Regression
    * Accuracy: 0.99
    * Precision (Healthy Loans - 0): 1.00
    * Recall (Healthy Loans - 0): 0.99
    * Precision (High-Risk Loans - 1): 0.84
    * Recall (High-Risk Loans - 1): 0.99
    * F1 Score (High-Risk Loans - 1): 0.91

# Summary
The logistic regression model did a great job overall. It was super accurate when it came to predicting healthy loans and almost never got them wrong. It also did a really good job finding high-risk loans, with a high recall score, meaning it caught almost all the risky ones. The precision for high-risk loans was a little lower, so it sometimes flagged healthy loans as risky, but that’s better than missing a loan that could default.

# Recommendation:
Since the model is excellent at catching risky loans (which is super important in the real world), I recommend using this logistic regression model. It helps reduce risk for lenders by making sure most of the dangerous loans are caught early, even if that means a few safe loans get flagged by mistake.



