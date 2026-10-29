# 📉 Telco Customer Churn Prediction & Retention Strategy

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![CatBoost](https://img.shields.io/badge/CatBoost-Yandex-FFCC00?style=for-the-badge&logo=yandex&logoColor=black)
![XGBoost](https://img.shields.io/badge/XGBoost-111111?style=for-the-badge&logo=xgboost&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🎯 Project Overview
This repository delivers an end-to-end **Machine Learning solution** designed for customer retention (*Customer Success*) in the telecommunications sector, using the **Telco Customer Churn** dataset (7,043 customers).

The main objective was to go beyond abstract technical metrics by building a robust data-leakage-free pipeline, optimizing for the business-oriented **$F_2$-Score** metric, and generating a **Risk Priority List** complete with an actionable **ROI and financial return simulation**.

---

## 🏗️ Pipeline Architecture

```text
┌──────────────────────────┐     ┌──────────────────────────┐     ┌──────────────────────────┐
│ Processing & Pipeline    │ ──► │ Modeling & Optimization  │ ──► │   Business & Strategy    │
│ (ColumnTransformer/Fit)  │     │ (CatBoost / $F_2$ @ 0.32) │     │ (ROI 77% / Top 20% Risk) │
└──────────────────────────┘     └──────────────────────────┘     └──────────────────────────┘
```

### 🛠️ Tech Stack & Methodology
* **Data Engineering & Preprocessing:** Python (Pandas, NumPy) using `ColumnTransformer` and `Pipeline` to strictly isolate training data from test data (*zero data leakage*).
* **Machine Learning Modeling:** Model evaluation comparing **Random Forest**, **XGBoost**, and **CatBoost** via 5-Fold Stratified Cross-Validation.
* **Imbalance Handling:** Comparative benchmarking between class weight balancing (`class_weight`) and **SMOTE**.
* **Threshold Tuning:** Decision threshold optimization based on the **$F_2$-Score** (giving 2x more weight to *Recall* to catch maximum churn-risk customers).

---

## 📊 Key Business Results

* 🏆 **Best Performing Model:** CatBoost with class weight balancing (`class_weight`), reaching an **0.846 ROC-AUC** in cross-validation.
* 🎯 **Optimal Decision Threshold:** Set at **0.32** (via $F_2$-Score), boosting **Recall to 90.1%** on the test set.
* 💰 **Financial Impact (ROI):** Targeting personalized retention offers to the **Top 20% highest-risk customers** captures **51% of total churners**, generating **$15,963 in Net Profit** and a **77% ROI**.

---

## 🖼️ Project Visualizations

| Threshold Optimization ($F_2$) | ROI Simulation by Risk Tier |
| :---: | :---: |
| ![Threshold F2](outputs/otimizacao_threshold_f2.png) | ![ROI Simulation](outputs/simulacao_roi.png) |

---

## 📁 Repository Structure

```text
telco-customer-churn-prediction/
│
├── telco_churn_retencao.ipynb   # Complete end-to-end executed notebook
├── requirements.txt             # Project dependencies and libraries
├── README.md                    # Project documentation (English)
└── outputs/                     # Generated reports, charts, and model files
    ├── lista_prioridade_risco.csv
    ├── modelo_churn_final.joblib
    ├── simulacao_roi.png
    └── ... (other PNG plots)
```

---

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/matheuspaes777/telco-customer-churn-prediction.git
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook:**
   Open `telco_churn_retencao.ipynb` in Jupyter Notebook, VS Code, or Google Colab and run all cells.

---

## 👤 Author
Developed by **Matheus Thiago Paes de Barros**  
*Computer Science Student — UNG*
