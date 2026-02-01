# 🧠 Optimizing Customer Retention Spend Using AI-Driven Churn Risk Intelligence

> **Turning churn predictions into cost-aware retention decisions using the Databricks Lakehouse**

---

## 📌 Overview
Customer churn is one of the largest silent revenue drains for e-commerce businesses.  
While many systems predict *who* might churn, businesses struggle with a more important question:

> **Who should we act on, and how, given limited retention budgets?**

This project delivers an **end-to-end, production-ready AI system** that not only predicts churn but **prioritizes customers and recommends targeted retention actions** to optimize business impact.

---

## 🎯 Business Problem
E-commerce platforms often:
- Lose customers without early warning
- Spend heavily on blanket discounts
- Lack clarity on where retention money should be spent

### Objective
Build an AI-driven system that:
- Identifies churn-prone customers
- Estimates revenue at risk
- Recommends cost-effective retention actions
- Supports real business decisions

---

## 🤔 Why AI (Not Rule-Based Systems)
Rule-based approaches fail because:
- Customer behavior is non-linear
- Purchase patterns vary widely
- Static thresholds don’t adapt to behavior changes

Machine Learning learns patterns from historical data and enables **data-driven retention strategies** instead of fixed rules.

---

## 🏗️ Solution Architecture

### Databricks Lakehouse – Medallion Architecture

![Architecture Diagram](https://github.com/GoduguVeena/IDC_Codebasics_Hackathon/blob/main/architecture.png)

### 🥉 Bronze Layer
- Raw transaction ingestion
- Immutable Delta tables
- Ingestion metadata for auditability

### 🥈 Silver Layer
- Cleaned and validated transactions
- Customer-level feature engineering
- Business-driven churn labeling

### 🥇 Gold Layer
- Churn risk segmentation
- Revenue-at-risk insights
- Actionable retention recommendations

### 🤖 ML Layer
- Supervised churn prediction model
- MLflow experiment tracking
- Predictions written back to Delta tables

---

## 🔧 Feature Engineering
Customer behavior is modeled using:
- **Recency** – Days since last purchase
- **Frequency** – Number of purchases
- **Monetary Value** – Total spend
- **Average Order Value** – Buying behavior

### Churn Definition
A customer is labeled as churned if they have not made a purchase in the last **90 days**  
*(Business assumption, configurable in real deployments)*

---

## 🤖 Machine Learning Approach
- **Task**: Binary Classification (Churn / No Churn)
- **Model**: Logistic Regression
- **Why**:
  - Interpretable and explainable
  - Strong baseline for business use
  - Efficient and scalable

### Evaluation
- Train/Test Split (80/20)
- Metric: **ROC-AUC**
- MLflow used for:
  - Parameter tracking
  - Metric logging
  - Model versioning

![MLflow Experiment](https://github.com/GoduguVeena/IDC_Codebasics_Hackathon/blob/main/mlflow.png)

---

## 🔑 From Prediction to Decision (Key Differentiator)
Most churn projects stop at prediction.  
This system goes further by **enabling action**.

### Risk Segmentation
- High Risk
- Medium Risk
- Low Risk

### Recommended Actions
| Risk Level | Action |
|----------|-------|
| High Risk | Discount Incentive |
| Medium Risk | Re-engagement Campaign |
| Low Risk | Loyalty Reward |

This ensures **retention budgets are spent where they matter most**.

---

## 📊 Analytics & Business Insights

![Gold Table Preview](https://github.com/GoduguVeena/IDC_Codebasics_Hackathon/blob/main/gold_table.png)

Key questions answered:
- How many customers are at high churn risk?
- How much revenue is at risk?
- Who should be prioritized immediately?

Example insight:
- Prevents unnecessary discounts
- Improves marketing efficiency
- Protects high-value customers

---

## ⚙️ Orchestration

The entire pipeline is automated using **Databricks Jobs**.

![Databricks Job Run](https://github.com/GoduguVeena/IDC_Codebasics_Hackathon/blob/main/jobs.png)

Pipeline:  

- Fully automated
- Retrainable
- Production-ready

---

## 🔐 Governance
- Unity Catalog for data organization
- Logical separation of:
  - Raw data
  - Processed features
  - Business insights
  - ML artifacts
- Designed with access control and lineage in mind

---

## ⚠️ Limitations & Future Enhancements
- Churn threshold is a business assumption
- Cost-sensitive optimization can improve decisions
- A/B testing can validate retention strategies
- Real-time inference can be added
- Additional features can improve accuracy

---

## 🔁 Reproducibility
- Modular Databricks notebooks
- Delta Lake storage
- Automated workflows
- Clear end-to-end data flow

---

## 🏁 Conclusion
This project demonstrates how AI can move **beyond prediction** and support **real business decisions**.

By combining Databricks Lakehouse architecture, machine learning, and analytics, the solution helps businesses:
- Retain the right customers
- Spend retention budgets wisely
- Make explainable, data-driven decisions

---

## 👩‍💻 Author
**Veena**  
IDC × Codebasics Hackathon Participant

