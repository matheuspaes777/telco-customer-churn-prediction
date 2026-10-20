# 📉 Telco Customer Churn Prediction & Analytics

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

## 📌 Overview & Business Context
Customer retention is one of the most critical metrics for telecom and SaaS companies. Acquiring a new customer can cost up to **5x more** than retaining an existing one. 

This project delivers an end-to-end Machine Learning pipeline to predict customer churn, identify key risk indicators, and provide actionable business recommendations to reduce customer attrition.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3.10+
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Seaborn, Matplotlib
- **Machine Learning:** Scikit-Learn (Random Forest Classifier)
- **Evaluation Metrics:** Precision, Recall, F1-Score, ROC-AUC

---

## 🚀 Key Project Steps

1. **Data Cleaning & Preprocessing:**
   - Handled missing and blank values in structural columns (`TotalCharges`).
   - Feature Engineering and categorical encoding using `pd.get_dummies()` with `drop_first=True` to avoid multicollinearity.

2. **Exploratory Data Analysis (EDA):**
   - Identified that month-to-month contracts and lack of tech support are the top churn drivers.
   - Tenure analysis revealed that customers are most vulnerable within their first 12 months.

3. **Machine Learning Modeling:**
   - Split dataset into **80% Training / 20% Testing**.
   - Trained a **Random Forest Classifier** with tuned hyper-parameters (`max_depth=8`) to prevent overfitting.
   - Evaluated model using classification metrics with a strong focus on **Recall** (minimizing false negatives).

---

## 📊 Key Results & Business Insights
- **Top Risk Factors:** Month-to-month contract type, Fiber optic internet service, and Electronic check payment method.
- **Actionable Advice:** Incentivize long-term contract switching (annual plans) by offering discounts on tech support packages during the first 6 months.

---

## 💻 How to Run This Project

```bash
# 1. Clone the repository
git clone [https://github.com/matheuspaes777/telco-customer-churn-prediction.git](https://github.com/matheuspaes777/telco-customer-churn-prediction.git)

# 2. Navigate to the project directory
cd telco-customer-churn-prediction

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the Jupyter Notebook or Python Script
python churn_prediction.py
