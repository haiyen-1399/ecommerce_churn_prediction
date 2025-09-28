# Churn Customer Prediction in Ecommerce

Table of Contents

- Project Overview
- Data
- Methodology
- Installation
- Usage
- Results
- Next Steps: Experimentation & Operations
- Future Work

1. Project Overview

- This project implements an end-to-end machine learning pipeline to predict customer churn using Random Forest, Decision Tree, Gradient Boosting models.

- Goals:

+ Define Timewindow for churn users identification

+ Identify customers who are likely to churn

+ Provide actionable insights for business operations

2. Data

The dataset contains product_id level data with features including demographics, purchase history, and engagement metrics.

Example Features:

customer_age, order_count, avg_product_price

app_engagement, time_since_last_purchase, return_rate

discount_usage, average_quantity

Target:

churn (binary: 1 if the customer churned, 0 otherwise)

3. Methodology

Data Cleaning & Preprocessing

Handle missing values, normalize numerical features, encode categorical variables.

Feature Engineering

Include time-series features and aggregated metrics.

Modeling



# Customer Churn Prediction: End-to-End Machine Learning Project

![Python](https://img.shields.io/badge/python-3.11-blue) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2.2-green) ![Pandas](https://img.shields.io/badge/pandas-1.6.0-yellow) ![Status](https://img.shields.io/badge/status-active-success)

---

## 📌 Project Overview
This project builds an **end-to-end machine learning pipeline** to predict **customer churn** for an e-commerce business.  
By identifying customers likely to churn, businesses can run **targeted retention campaigns** that improve ROI and customer lifetime value.

Key highlights:
1. Exploratory Data Analysis (EDA) with visual insights
2. Feature engineering on customer demographics, transaction history, and engagement
3. Multipled models are used: **Decision Tree**, **Random Forest**, **Logistic Regression**, **Gradient Boosting**, **SVM**
4. Evaluation with precision, recall, F1-score, and AUC, we found that **Random Forest** and **Decision Tree** are the best performers
5. Business experiment design (A/B test) and operational next steps

Dataset: [E-commerce Sales Transactions (Kaggle)](https://www.kaggle.com/datasets/miadul/e-commerce-sales-transactions-dataset)

---

## 📂 Project Structure

churn_prediction/
│── data/             <- Raw and processed data
│── notebooks/        <- Jupyter notebooks (EDA, modeling, evaluation)
│── src/              <- Scripts for training, prediction, evaluation
│── results/          <- Model outputs and evaluation reports
│── requirements.txt  <- Dependencies
│── README.md         <- Project documentation

---

## 📊 Results

- Random Forest: Precision = 0.72, Recall = 0.68, F1-score = 0.70

- Decision Tree: Easier to interpret, slightly lower performance

- Feature importance: Lifetime value & recent 4-month activity are top predictors

---


## 🧪 Experiment Design

| **Component** | **Description** |
|---------------|-----------------|
| **Hypothesis** | Targeted promotions to predicted churn customers improve ROI compared to baseline. |
| **Groups** | Control: mass promotion; Treatment: predicted churn customers only. |
| **Metrics** | P0: ROI (+10% target); P1/P2: engagement & conversion rates; Guardrail: churn rate. |
| **Conditions** | Optional: segment by region. |
| **Timeline** | Based on business cycle & campaign frequency. |

---

## 🛠 Operations
- Deploy model to generate daily churn probability scores.  
- Segment customers for targeted retention actions.  
- Continuously monitor churn rate and ROI for improvement.  

---

## 🔮 Future Work
- Add app/web engagement & time-series features  
- Explore ensemble models (stacking RF + DT)  
- Automate retraining pipeline  

---

**📜 License**
MIT License  

