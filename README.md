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
