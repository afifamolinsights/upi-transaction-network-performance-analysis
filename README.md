# UPI Transaction & Network Performance Analysis

> An end-to-end analysis of UPI digital payment transactions to identify factors affecting transaction success rate, network performance, and payment reliability using Python machine learning models and a Tableau analytics dashboard.

## 📊 Tableau Dashboard

<p align="center">
  <img src="C:\Users\afifa\Pictures\Screenshots\Screenshot 2026-02-28 012855.png" width="900">
</p>

---
# ⚙️ Project Type Flags

* [x] Exploratory Data Analysis (EDA)
* [ ] SQL Analysis / Querying
* [x] Dashboard / Data Visualization
* [ ] Data Pipeline / ETL
* [x] Predictive Modelling / Machine Learning
* [x] Data Cleaning / Wrangling
* [x] End-to-End (multiple of the above)

---
# Table of Contents

1. Project Overview
2. Objectives
3. Project Scope & Tools
4. Repository Structure
5. Data Workflow
6. Data Model & Schema
7. Analysis & Metrics
8. Key Insights
9. Recommendations
10. Assumptions & Limitations
11. Future Enhancements
12. Deliverables
13. Author

---

# 1. Project Overview

**Context**

UPI (Unified Payments Interface) has become one of the most widely used digital payment systems in India, processing millions of transactions daily. Maintaining high transaction success rates and reliable network performance is critical for digital payment platforms and banking institutions.

**Problem Statement**

UPI transaction failures can occur due to multiple technical and infrastructure issues such as network latency, server load, device compatibility, or banking system limitations. Identifying these factors can help improve payment reliability and user experience.

**Approach**

This project analyzes a dataset of UPI transactions using **Python for data cleaning, exploratory data analysis, and machine learning modelling**. The insights are visualized through an **interactive Tableau dashboard** to explore transaction performance across device types, banks, regions, and merchant categories.

**Outcome**

The analysis highlights patterns in **transaction failures, network performance, device usage trends, and bank transaction success rates**, providing insights that can help optimize digital payment systems.

---

# 2. Objectives

**Primary Objective**

* Identify factors that influence **UPI transaction success and failure rates**.

**Secondary Objectives**

* Analyze the relationship between **network latency and server load on transaction outcomes**
* Evaluate **bank performance in handling digital payment transactions**
* Study **device usage distribution in UPI transactions**
* Identify **merchant categories with high transaction volumes**

---

# 3. Project Scope & Tools

## Scope

| Dimension        | Details                                                                                                            |
| ---------------- | ------------------------------------------------------------------------------------------------------------------ |
| **In Scope**     | UPI transaction data including bank name, device type, network latency, server load, region, and merchant category |
| **Out of Scope** | Fraud detection, real-time banking infrastructure, and user demographic data                                       |
| **Time Period**  | Sample transaction dataset used for analytical modelling                                                           |
| **Granularity**  | Transaction-level dataset                                                                                          |

---

## Tools & Technologies

| Category         | Tool(s) Used                 |
| ---------------- | ---------------------------- |
| Data Storage     | CSV / Excel dataset          |
| Data Processing  | Python                       |
| Analysis         | Pandas, NumPy                |
| Visualization    | Tableau, Matplotlib, Seaborn |
| Machine Learning | Scikit-learn                 |
| Version Control  | Git / GitHub                 |
| Documentation    | Markdown                     |

---

# 4. Repository Structure

```
upi-transaction-network-performance-analysis
│
├── data
│   ├── raw
│   │   └── upi_transactions_dataset.csv
│   └── processed
│
├── notebooks
│   └── upi_transaction_analysis.ipynb
│
├── visuals
│   └── tableau_dashboard.png
│
├── reports
│   └── project_presentation.pptx
│
└── README.md
```

---

# 5. Data Workflow

```
UPI Transaction Dataset
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Machine Learning Model Training
        ↓
Model Evaluation
        ↓
Tableau Dashboard Visualization
```

### Source

The dataset contains transaction-level information including bank name, transaction status, latency, server load, merchant category, device type, and region.

### Ingestion

The dataset was imported into Python using **Pandas**.

### Cleaning

* Removed duplicate transactions
* Checked missing values
* Standardized categorical variables

### Transformation

* Calculated **success rate and failure rate**
* Aggregated transaction counts by **bank, device type, region, and merchant category**

### Analysis

* Exploratory data analysis
* Correlation analysis between **latency and server load**
* Machine learning classification models

### Output

* Tableau dashboard
* Jupyter Notebook analysis
* Project report

---

# 6. Data Model & Schema

### Dataset: UPI Transactions

| Field Name         | Data Type | Description                            | Example |
| ------------------ | --------- | -------------------------------------- | ------- |
| Transaction_ID     | String    | Unique identifier for each transaction | TXN1023 |
| Bank_Name          | String    | Bank processing the transaction        | HDFC    |
| Device_Type        | String    | Device used for payment                | Android |
| Merchant_Category  | String    | Type of merchant transaction           | Travel  |
| Region             | String    | Geographic transaction region          | North   |
| Network_Latency    | Float     | Internet latency in milliseconds       | 250     |
| Server_Load        | Float     | Server utilization percentage          | 58      |
| Transaction_Status | String    | Transaction result (Success / Fail)    | Success |

**Row Count:** ~10,000 transactions

---

# 7. Analysis & Metrics

## Analytical Approach

The project uses **exploratory data analysis and machine learning classification models** to identify patterns affecting transaction outcomes and network performance.

---

## Key Metrics

| Metric          | Definition                            | Why It Matters                                  |
| --------------- | ------------------------------------- | ----------------------------------------------- |
| Success Rate    | Percentage of successful transactions | Indicates system reliability                    |
| Failure Rate    | Percentage of failed transactions     | Helps identify network or infrastructure issues |
| Network Latency | Time taken for transaction processing | Higher latency may cause failures               |
| Server Load     | Server processing utilization         | High load can reduce transaction success        |

---

# 8. Key Insights

**Insight 1 — High Transaction Failure Rate**

Approximately **68.9% of transactions resulted in failures**, suggesting that network or infrastructure issues may significantly impact payment reliability.

**Insight 2 — Android Devices Dominate Transactions**

Nearly **60% of transactions were conducted through Android devices**, highlighting strong mobile payment adoption.

**Insight 3 — Network Latency Impacts Transaction Success**

Higher internet latency values were associated with increased transaction failures, indicating the importance of network optimization.

**Insight 4 — Merchant Category Distribution**

Travel, shopping, and utility payments showed higher transaction volumes compared to other categories.

---

# 9. Recommendations

| Priority | Recommendation                                                           | Based On                    | Suggested Owner                 |
| -------- | ------------------------------------------------------------------------ | --------------------------- | ------------------------------- |
| High     | Improve network infrastructure to reduce latency during peak hours       | Latency vs failure analysis | Payment network providers       |
| Medium   | Increase server capacity to handle high transaction loads                | Server load correlation     | Banking IT infrastructure teams |
| Medium   | Implement monitoring systems for early detection of transaction failures | High failure rate trend     | Payment platform administrators |

---

# 10. Assumptions & Limitations

### Assumptions

* Transaction records represent real-world digital payment patterns.
* Network latency and server load metrics accurately reflect system performance.

### Limitations

* Dataset size is limited and may not fully represent real-world transaction volumes.
* Fraud detection and security systems were not included in the analysis.
* External factors such as banking downtime or payment gateway failures were not captured.

---

# 11. Future Enhancements

* Develop **real-time transaction monitoring dashboard**
* Apply **advanced machine learning models (XGBoost, Gradient Boosting)**
* Integrate **live payment transaction APIs**
* Build **transaction failure prediction system**

---

# 12. Deliverables

| Deliverable          | Description                               | Location     |
| -------------------- | ----------------------------------------- | ------------ |
| Jupyter Notebook     | Data analysis and ML model implementation | `/notebooks` |
| Tableau Dashboard    | Interactive visualization dashboard       | `/visuals`   |
| Dataset              | Transaction dataset used for analysis     | `/data`      |
| Project Presentation | Project explanation slides                | `/reports`   |

---

# 13. Author

**Afifa Mol**-
**Data Analyst**

* GitHub: [https://github.com/yourusername](https://github.com/yourusername)
* LinkedIn: [https://linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
.
