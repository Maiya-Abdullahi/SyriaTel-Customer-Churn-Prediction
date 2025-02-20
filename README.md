# SyriaTel-Customer-Churn-Prediction

## Project Overview
This project focuses on predicting customer churn for SyriaTel using machine learning models. By analyzing customer behavior and service usage, we aim to identify high-risk customers and provide insights to reduce churn.

## Business Understanding
### **Business Problem**
SyriaTel, a leading telecommunications company, faces a major challenge: customer churn. Customers leaving the network results in revenue loss and increased costs to acquire new users. To maintain profitability and customer loyalty, SyriaTel needs a reliable way to predict which customers are likely to churn and take proactive retention measures.

**The goal of this project** is to build a Classification model to predict whether customers are at risk of churning based on their call usage, account features, and service complaints. SyriaTel can then implement targeted retention strategies, such as offering discounts or improving service.

#### Key Business Questions:
What are the key factors that contribute to customer churn?
Can we predict which customers are likely to churn?
What interventions can be implemented to reduce churn?
How can the model's insights inform marketing and customer service strategies?.

##  Data Understanding
- **Dataset Source:** Kaggle
- **Features include:** State, Account length, Area code, Phone number, International plan, Voice mail plan, and more.
- **Target Variable:** `churn` (1 = Churn, 0 = Not Churn)

##  Data Preprocessing & Feature Engineering
- Handled missing values and outliers.
- Scaled numerical features using MinmaxScaler.
- Applied SMOTE to handle class imbalance.
- Scaled Train and Test set Using StandardScaler
- Selected important features using feature importance from XGBoost.

##  Model Building & Evaluation
| Model                | Precision | Recall | F1-score |
|----------------------|----------|--------|----------|
| Decision Tree       | 0.55     | 0.70   | 0.62     |
| Random Forest      | 0.50     | 0.81   | 0.62     |
| **XGBoost** (Best)  | **0.54** | **0.70** | **0.61** |
| Logistic Regression | 0.37     | 0.80   | 0.50     |

- **Best Model:** XGBoost (Offers the best trade-off between Precision & Recall)
- **Evaluation Metrics:** Precision, Recall, F1-score, Confusion Matrix
- **Feature Importance:** Top factors influencing churn were contract type, tenure, and number of support calls.

## Visualizations
- Churn distribution
![image](https://github.com/user-attachments/assets/386db9c4-8681-4b60-af1c-d68087a94944)

- Correlation heatmap
![image](https://github.com/user-attachments/assets/00d25f9f-54a1-4293-80f9-711f4d82dc92)

- Feature importance from XGBoost
![image](https://github.com/user-attachments/assets/5c51e505-e76c-422b-a339-56ccf48d5711)
  
- Model comparison (Precision, Recall, F1-score bar charts)
![image](https://github.com/user-attachments/assets/eb6aa942-4027-4ade-9a7f-57cdc6c5c85a)

![image](https://github.com/user-attachments/assets/a9423b8c-4719-4bd1-bfda-ef66445b18b4)

  ![image](https://github.com/user-attachments/assets/5ade8d22-fb25-423e-8097-21d2bc000056)

- Confusion matrix for the best model
![image](https://github.com/user-attachments/assets/133893b2-fd45-4db7-95e1-d9a120be4fb5)


## Business Insights & Recommendations
## Business Problem Summary & Final Conclusion
**Business Problem**

SyriaTel, a telecommunications provider, is experiencing customer churn, which negatively impacts revenue and long-term business sustainability. The goal of this analysis was to develop a predictive model that identifies customers at risk of churning, allowing the company to implement proactive retention strategies.

**Model Performance Summary**

We evaluated four machine learning models—Decision Tree, Random Forest, XGBoost, and Logistic Regression—to determine the best-performing model for predicting churn. Performance was assessed based on Precision, Recall, and F1-score to balance false positives and false negatives effectively.

| Model                 | Precision | Recall  | F1-score |
|----------------------|-----------|--------|----------|
| Decision Tree       | 0.5488    | 0.7031 | 0.6164   |
| Random Forest      | 0.5049    | 0.8125 | 0.6228   |
| XGBoost           | 0.5357    | 0.7031 | 0.6081   |
| Logistic Regression | 0.3669    | 0.7969 | 0.5025   |

**Findings & Insights**

- Random Forest achieved the highest F1-score (0.6228), indicating a balanced trade-off between Precision and Recall.
- Decision Tree and XGBoost performed similarly, with XGBoost showing slightly better Precision (0.5357), meaning fewer false positives in churn prediction.
- Logistic Regression had the lowest Precision (0.3669), leading to a higher number of false positives, making it less ideal for customer retention strategies.

**Business Recommendation & Next Steps**
- Adopt the Random Forest model for churn prediction to maximize customer retention efforts while maintaining a balance between correctly identifying churned customers (Recall) and minimizing false positives (Precision).
- Use the model’s insights to target high-risk customers with retention offers, such as personalized discounts, improved service plans, or enhanced customer support.
- Further optimize the XGBoost model as it has strong potential with better Precision than Random Forest, which could reduce unnecessary interventions with non-churning customers.
- Regularly retrain the model using updated customer data to improve prediction accuracy as customer behaviors evolve.
**By leveraging these insights, SyriaTel can reduce churn, improve customer satisfaction, and enhance long-term profitability.**
offering incentives for long-term contracts.
