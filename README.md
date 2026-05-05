# SYRIA TEL COMMUNICATION COMPANY
## Table of Contents
1. Overview
2. Business Problem
3. Business Understanding
4. Data Understanding (EDA)
5. Data Preprocessing
6. Data Models
7. Business Analysis, Key Findings, and Recommendations
8. Conclusion
9. Resources and Links
## Overview
This project uses machine learning to predict whether a customer will churn (leave a service) based on historical patterns

## Business Problem
The goal is to identify high-risk customers early,enabling SyriaTel to take targeted retention actions before they churn.
# Business Understanding
Customer churn is a significant issue in Syria Tel Company as it result in loss of revenue, customer disatisfaction and increase in cost of acquiring new customers to replace them.
The goal of this project is to build a model that can predict whether a customer will churn in the near future. 

This can be formulated using binary classification where:

1 = customer will churn

0 = customer will remain

using selected features.


## Business Objective
1.To retain Valuable customers

2.To increase customer satisfaction

3.To reduce revenue loss

4.To optimize marketing and retention efforts

# Dataset Summary

Rows: 3,333 customers

Columns: 21 features

Observations

No missing values or duplicates

Class imbalance present 14.5% churn

Strong relationships between:

Customer service calls and churn

Usage (minutes/charges) and churn
 
 # Exploratory Data Analysis (EDA)
Key Insights

Customers with more service calls are more likely to churn

Higher daily usage is associated with churn

Customers with an international plan churn more

Strong multicollinearity between minutes and charges
# Data Preprocessing

Dropped irrelevant/leakage features:
    phone number, area code charge variables (perfectly correlated with minutes)

Encoded categorical variables:

Binary encoding for plans

One-hot encoding for state

Train-test split: 80/20 (stratified)

Feature scaling applied

Handled imbalance using class weights

# Models Built

1. Dummy Classifier (Baseline)

     Predicts majority class (no churn)

     Demonstrates the accuracy trap

2. Logistic Regression

    Linear model with balanced class weights

     Good at identifying churners (high recall)

3. Decision Tree (Tuned)

     Captures non-linear relationships

     Hyperparameter tuning using GridSearchCV
   # Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score | AUC  |
| ------------------- | -------- | --------- | ------ | -------- | ---- |
| Dummy               | 0.855    | 0.000     | 0.000  | 0.000    | 0.50 |
| Logistic Regression | 0.745    | 0.325     | 0.701  | 0.444    | 0.73 |
| Decision Tree       | 0.903    | 0.648     | 0.722  | 0.683    | 0.83 |
# Key Findings

## Dummy Model
  
   Misleading high accuracy due to imbalance

   Fails completely at detecting churn

## Logistic Regression
  
   High recall → detects most churners
  
   Low precision → many false positives

## Decision Tree (Best Model)

    Best overall balance (Precision + Recall)

    Strong classification performance

    High AUC → good class separation
    # Recommendation

## Primary Model: Decision Tree
   
     Best overall performance
    
     Strong business applicability

     Balanced detection vs false alarms

## Secondary Model: Logistic Regression
     
     Use for early warning systems

     Helps capture more potential churners

## Avoid

Dummy classifier (baseline only)

### On Features

Features such as customer service,charges,minutes, voicemail,international plan have a strong effect on churn therefore the company can improve by

1.Increase customer quality through staff staining and service responsiveness

2.Compare charges with the industry charge so that customers don't switch to  your competitors

3.Intoduce flexible call  minutes packages as a form of discounts and marketing to customer inorder to retain them and attract new ones

4.Review international clients plans pricing and service efficiency ensuring fairness while maintaining operational sustainability 

# CONCLUSION

Overall,the Decision Tree model combined with these business insights provides a strong foundation for proactive churn management. 

By focusing on both predictive modeling and targeted business interventions, the company can significantly improve customer retention, reduce churn-related losses, and enhance long-term customer satisfaction.

# Resouces 
Syria Tel Communication Company PDf

Project Notebook



