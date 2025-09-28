# Customer Churn Prediction: End-to-End Machine Learning Project

![Python](https://img.shields.io/badge/python-3.11-blue) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.2.2-green) ![Pandas](https://img.shields.io/badge/pandas-1.6.0-yellow) ![Status](https://img.shields.io/badge/status-active-success)

---

## 📌 Project Overview
This project builds an **end-to-end machine learning pipeline** to predict **customer churn** for an e-commerce business.  
By identifying customers likely to churn, businesses can run **targeted retention campaigns** that improve ROI and customer lifetime value.

**Key highlights:**
1. **Churn analysis and time window definition:** A customer is considered churned if they have no transaction activity within a defined four-month period.
2. **Exploratory Data Analysis (EDA):** Lifetime values and long-term behaviors show a higher correlation with the probability of churn.
3. **Feature engineering:** Conducted on customer demographics, transaction history, and buying behaviors.
4. **Modeling:** Multiple models were applied, including **Decision Tree**, **Random Forest**, **Logistic Regression**, **Gradient Boosting**, and **SVM**.
5. **Evaluation:** Using precision, recall, F1-score, and ROC-AUC, we found that **Random Forest**, **Gradient Boosting**, and **Decision Tree** performed the best.
6. **Business experiment design:** A/B testing and operational next steps were planned.


Dataset: [E-commerce Sales Transactions (Kaggle)](https://www.kaggle.com/datasets/miadul/e-commerce-sales-transactions-dataset)


---

## 📊 Results

- **Overall Best:** Random Forest → strongest performance across all metrics, with the highest ROC-AUC.  
- **High-cost retention campaigns** (minimize false positives, prioritize precision): Gradient Boosting, Random Forest.  
- **Mass low-cost engagement** (minimize false negatives, prioritize recall): Decision Tree.  
- **Balanced approach** (optimize F1-score for overall balance): Gradient Boosting, Random Forest.

### Model Performance Metrics

| Model               | Accuracy | Precision | Recall | F1    | ROC-AUC |
|--------------------|---------|----------|-------|-------|---------|
| Decision Tree       | 0.763   | 0.767    | 0.744 | 0.755 | 0.762   |
| Gradient Boosting   | 0.796   | 0.846    | 0.714 | 0.774 | 0.879   |
| Logistic Regression | 0.734   | 0.731    | 0.726 | 0.728 | 0.804   |
| Random Forest       | 0.796   | 0.833    | 0.729 | 0.777 | 0.884   |
| SVM                 | 0.671   | 0.655    | 0.692 | 0.673 | 0.745   |


- **Feature importance**: Lifetime value & recent 4-month activity are top predictors

---


## Next Steps

### 🧪 Experiment Design

| **Component** | **Description** |
|---------------|-----------------|
| **Hypothesis** | Targeted promotions to predicted churn customers improve ROI compared to baseline. |
| **Groups** | Control: mass promotion; Treatment: predicted churn customers only. |
| **Metrics** | P0: ROI (+10% target); P1/P2: promotion conversion rate, profit per user; Guardrail: churn rate. |
| **Conditions** | Optional: segment by region. |
| **Timeline** | Based on business cycle & campaign frequency. |

---

### 🛠 Operations
- Deploy model to generate daily churn probability scores.  
- Segment customers for targeted retention actions.  
- Continuously monitor churn rate and ROI for improvement.  

---

### 🔮 Model Improvements
- Add app/web engagement & time-series features  
- Explore ensemble models (stacking RF + DT)  
- Automate retraining pipeline  

---

**📜 License**
MIT License  

