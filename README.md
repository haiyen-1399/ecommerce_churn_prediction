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


Compare performance using precision, recall, F1-score

Evaluation

Deployment Pipeline

Generate daily churn probability scores

Segment customers for targeted promotions


4. Results

Random Forest: Precision = 0.72, Recall = 0.68, F1-score = 0.70

Decision Tree: Slightly lower performance but easier to interpret

Feature Importance: Lifetime value and recent 4-month activity are key predictors

5. Next Steps: Experimentation & Operations

Experiment Design (A/B Test):

Component	Description
Hypothesis	Targeted retention promotions to predicted churn customers improve ROI compared to the baseline (control) segment.
Groups	Control: mass retention promotion; Treatment: target predicted churn customers.
Success Metrics	P0: ROI (+10% improvement), P1/P2: engagement & conversion rates; Guardrail: churn rate.
Other Conditions	Optional: segment by region or customer type.
Timeline	Define based on business cycle.

Operational Steps:

Deploy model to generate daily churn probability tags.

Segment customers based on risk score and apply targeted retention strategies.

Monitor daily churn rate and ROI for continuous improvement.

Future Work

Integrate upper-funnel metrics (app/web engagement, conversion rate)

Explore ensemble models (stacking Random Forest + Decision Tree)

Deployment: 
- Automate model retraining with new data

- Expand experiment design for multi-region testing

# Customer Churn Prediction: End-to-End Machine Learning Project

![Python](https://img.shields.io/badge/python-3.11-blue) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2.2-green) ![Pandas](https://img.shields.io/badge/pandas-1.6.0-yellow) ![Status](https://img.shields.io/badge/status-active-success)

---

## 📌 Project Overview
This project builds an **end-to-end machine learning pipeline** to predict **customer churn** for an e-commerce business.  
By identifying customers likely to churn, businesses can run **targeted retention campaigns** that improve ROI and customer lifetime value.

Key highlights:
- Exploratory Data Analysis (EDA) with visual insights
- Feature engineering on customer demographics, transaction history, and engagement
- Model building using **Decision Tree** and **Random Forest**
- Evaluation with precision, recall, F1-score, and AUC
- Business experiment design (A/B test) and operational next steps

Dataset: [E-commerce Sales Transactions (Kaggle)](https://www.kaggle.com/datasets/miadul/e-commerce-sales-transactions-dataset)

---

## 📂 Project Structure

churn_prediction/
│── data/ <- Raw and processed data
│── notebooks/ <- Jupyter notebooks (EDA, modeling, evaluation)
│── src/ <- Scripts for training, prediction, evaluation
│── results/ <- Model outputs and evaluation reports
│── requirements.txt <- Dependencies
│── README.md <- Project documentation
---

## ⚙️ Installation
```bash
# Clone the repo
git clone https://github.com/yourusername/churn-prediction.git
cd churn-prediction

# Install dependencies
pip install -r requirements.txt

# Train models
python src/train_models.py

# Predict churn on new data
python src/predict.py --input data/new_customers.csv --output results/predictions.csv

# Evaluate performance
python src/evaluate_model.py

📊 Results

Random Forest: Precision = 0.72, Recall = 0.68, F1-score = 0.70

Decision Tree: Easier to interpret, slightly lower performance

Feature importance: Lifetime value & recent 4-month activity are top predictors

🧪 Experiment Design
Component	Description
Hypothesis	Targeted promotions to predicted churn customers improve ROI compared to baseline.
Groups	Control: mass promotion; Treatment: predicted churn customers only.
Metrics	P0: ROI (+10% target); P1/P2: engagement & conversion rates; Guardrail: churn rate.
Conditions	Optional: segment by region.
Timeline	Based on business cycle & campaign frequency.
🛠 Operations

Deploy model to generate daily churn probability scores.

Segment customers for targeted retention actions.

Continuously monitor churn rate and ROI for improvement.

🔮 Future Work

Add app/web engagement & time-series features

Explore ensemble models (stacking RF + DT)

Automate retraining pipeline

Expand experiments across customer segments

📜 License

MIT License

