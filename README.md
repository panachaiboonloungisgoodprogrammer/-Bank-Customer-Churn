# -Bank-Customer-Churn
# 🏦 Bank Customer Churn Prediction (AI/ML Project)

## 📘 Overview
This project aims to **predict customer churn for a bank** — identifying which customers are likely to leave the bank based on their demographic and financial data.  
The goal is to help the bank improve customer retention strategies and understand the key factors influencing customer churn.

The project was developed as part of the **YDP AI/ML Track 2025**.

---

## 📂 Dataset Description
The dataset used is `Customer-Churn-Records.csv`, which contains information about **10,000 customers**.  
Each row represents one customer, with features describing their demographics, account information, and activity.

### 🧾 Columns Overview
| Column | Description |
|--------|-------------|
| CreditScore | Credit score of the customer |
| Geography | Country of residence (France, Germany, Spain) |
| Gender | Customer gender (Male/Female) |
| Age | Age of the customer |
| Tenure | Years the customer has been with the bank |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Whether the customer has a credit card (1/0) |
| IsActiveMember | Whether the customer is active (1/0) |
| EstimatedSalary | Estimated annual income |
| Card Type | Type of bank card (Blue, Silver, Gold, Platinum) |
| Complain | Whether the customer has ever complained |
| Satisfaction Score | Overall satisfaction level |
| Exited | Target variable: 1 = Customer left, 0 = Still active |

---

## ⚙️ Data Preparation
Before training, the data was cleaned and transformed:
- Removed unnecessary columns: `RowNumber`, `CustomerId`, `Surname`
- Checked for missing values (none found)
- Encoded categorical data using `LabelEncoder`
- Scaled numerical features with `StandardScaler`
- Split data into **80% training** and **20% testing** sets

---

## 🧩 Model Building
Three machine learning models were trained and compared:
1. **Logistic Regression**
2. **Random Forest Classifier**
3. **XGBoost Classifier**

Training and evaluation were performed using the `scikit-learn` and `xgboost` libraries.

---

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1-score |
|--------|-----------|-----------|---------|-----------|
| Logistic Regression | 82% | 0.80 | 0.72 | 0.76 |
| Random Forest | 87% | 0.84 | 0.80 | 0.82 |
| **XGBoost** | **89%** | **0.86** | **0.84** | **0.85** |

✅ **XGBoost achieved the best overall performance**, and was selected as the final model.

---

## 🔍 Key Insights (Feature Importance)
According to XGBoost’s feature importance:
- **Age** and **Complain** were the strongest predictors of churn.
- **Satisfaction Score** and **Balance** also had significant impact.
- Customers who were older or had made complaints were more likely to leave the bank.

---

## 📈 Visualization
Several visualizations were created during EDA and model evaluation:
- Distribution plots of key numerical features (Age, Balance, CreditScore)
- Correlation Heatmap between numerical variables
- Confusion Matrix for model performance
- Feature Importance bar chart (XGBoost)

---

## 💻 How to Run the Project

### 1. Clone this repository
```bash
git clone https://github.com/yourusername/bank-customer-churn.git
cd bank-customer-churn

