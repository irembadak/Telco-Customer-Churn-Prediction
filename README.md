#  Telco Customer Churn Prediction

This project focuses on predicting customer attrition (churn) for a telecommunications company. The goal is to identify high-risk customers before they leave, enabling proactive retention strategies.

##  Project Overview
In this analysis, I built an end-to-end machine learning pipeline that covers data cleaning, feature engineering, handling imbalanced data, and model optimization.

##  Key Technical Steps
* **Data Preprocessing:** Handled missing values in `TotalCharges` and converted categorical variables into numerical format using **One-Hot Encoding**.
* **Handling Class Imbalance:** Since the number of customers who stay is much higher than those who leave, I applied **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the training data.
* **Modeling:** Implemented the **XGBoost Classifier**, a powerful gradient boosting algorithm.
* **Hyperparameter Tuning:** Optimized the model using **RandomizedSearchCV** to find the best balance between precision and recall, preventing overfitting.

##  Performance Metrics
After optimization and SMOTE application, the model achieved:
* **Overall Accuracy:** 76%
* **Recall (Churn Class):** **66%** * *Why this matters:* The model successfully identifies 2 out of 3 customers who are actually planning to leave, which is the most critical metric for business retention.

##  Key Insights (Feature Importance)

Based on our optimized XGBoost model, we identified the key factors that drive customer churn. The visualization below displays the top 10 features, ranked by their importance scores.

<p align="center">
  <img src="https://raw.githubusercontent.com/irembadak/Telco-Customer-Churn-Prediction/main/feature_importance.png" width="600" title="Key Features Driving Customer Churn" Alt="Feature Importance Plot">
</p>

### Analysis of Top Features:
1.  **Payment Method (Electronic Check):** This is the most significant predictor of churn. Customers using this method are much more likely to leave, suggesting potential issues with the payment experience or the customer segment using this method.
2.  **Internet Service (Fiber Optic):** Surprisingly, fiber optic users show a higher propensity to churn. This insight warrants further investigation into service quality, pricing, or customer expectations.
3.  **Contract Type (Two Year):** Long-term contracts have a strong influence, likely acting as a strong retention factor (reducing churn).

## 🛠️ Requirements
- Python 3.x
- Pandas, Numpy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)

---
*Developed as part of my Computer Programming studies at Dokuz Eylül University.*
