# 📊 Telco Customer Churn Prediction & Analysis

## 🎯 Business Problem
Customer retention is one of the most critical metrics for any subscription-based business. The objective of this project is to analyze a telecommunications dataset, identify the main drivers of customer churn, and build a Machine Learning model capable of predicting which customers are most likely to cancel their services in the near future.

## 🛠️ Tools & Technologies
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (Random Forest Classifier)

## 📈 Key Business Insights (EDA)
1. **Contract Type is Crucial:** Customers with `Month-to-month` contracts have a drastically higher churn rate compared to those with 1-year or 2-year contracts.
2. **Financial Burden:** The density of churn increases significantly as `MonthlyCharges` go up, suggesting price sensitivity or strong competition in premium tiers.
3. **Lack of Support Services:** Customers who do not have `TechSupport` or `OnlineSecurity` are far more likely to leave the ecosystem.

## 🤖 Machine Learning Model
A **Random Forest Classifier** was trained to predict the probability of a customer leaving. 
* **Data Preprocessing:** Handled missing values (blank strings in `TotalCharges`), applied One-Hot Encoding (`pd.get_dummies`), and split the data into 80/20 train-test sets.
* **Top Predictive Features:** According to the model's feature importance, the primary indicators of churn are:
  1. Total Charges
  2. Monthly Charges
  3. Tenure (Months as a customer)
  4. Contract Type (Month-to-month)
  5. Internet Service Type (Fiber Optic)

## 💡 Strategic Recommendations for the Company
* **Incentivize Long-Term Contracts:** Offer discounts or upgrades to transition month-to-month users into annual plans.
* **Proactive Engagement:** Implement targeted retention campaigns for users passing the 70 USD monthly charge threshold.
* **Value-Add Services:** Bundle Tech Support into base packages for the first 3 months to increase platform stickiness.
