# 💳 Credit Card Default Risk Prediction  

---

## 🧠 Overview  
This project builds a machine learning model to predict whether a credit card customer will default on their payment one month in advance. By leveraging a dataset of **25,247 customers**, the model achieves a **76.72% AUC** and identifies **51.77%** of potential defaults—providing significant value to banks in managing financial risk.

---
 
## 🎯 Objective  
To develop a **behavior score model** that predicts customer defaults, enabling proactive interventions and smarter credit decisions.

---

## 🔍 Strategy and Methodology  

- **Data-Driven EDA**: Customer segmentation, default patterns, and financial behavior.
- **Feature Engineering**: Created 11 new domain-aware features from original 28.
- **Model Selection**: Benchmarked 6 models; selected **CatBoost** for best trade-off.
- **Business-Aware Thresholding**: Tuned threshold (0.339) to maximize default capture with fewer false positives.

---

## 📈 Dataset Insights  
- **Total Records**: 25,247  
- **Default Rate**: 19.04%  
- **Missing Values**: 126 in 'Age' (0.5%)



### Key Findings  
- Seniors have higher default risk (~23%)  
- High credit utilization and delayed payments increase default chances  
- University graduates and married individuals show lower risk

---

## 🔧 Feature Engineering  

- **Delinquency Score**: Severity of late payments  
- **Payment Consistency**: Monthly payment regularity  
- **Utilization Ratio**: Spending vs credit limit  
- **Bill Growth Trend**: Tracks financial stress over time


![Top Features](./images/Screenshot%202025-06-30%20160108.png)

---

## 🤖 Model Evaluation  

| Model              | AUC    | Accuracy | Precision | Recall  | F1     |
|-------------------|--------|----------|-----------|---------|--------|
| LogisticRegression| 0.7167 | 75.52%   | 38.92%    | 50.00%  | 43.77% |
| RandomForest       | 0.7755 | 82.75%   | 56.74%    | 39.81%  | 46.06% |
| **CatBoost**       | **0.7672** | **83.45%** | **60.50%** | **37.73%** | **46.48%** |


![ROC_comparison](./images/Screenshot%202025-06-30%20160731.png)

---

## ⚖️ Threshold Tuning  
- **Optimal threshold**: 0.339  
- **Default capture rate**: 51.77%  
- **False alarm rate**: 12.2%  
- **Review population**: 19.7% of all customers  

![Threshold Optimization](./images/Screenshot%202025-06-30%20160017.png)

---

## 📌 Business Value  

### ✅ Risk Management Use Cases  
- Early warning system for defaults  
- Proactive outreach to high-risk customers  
- Smarter credit limit allocation  
- Focused collection efforts

### 💰 Financial Impact  
- Reduced losses and improved retention  
- Lower collection costs  
- Operational scalability with monthly model deployment  

---

## 🧠 Key Learnings  
- **Payment behavior** is the top risk driver  
- **Feature engineering** outperforms raw variables  
- **SMOTE** helped counter class imbalance  
- **Domain-driven ML** delivers business-aligned results  

---
#
