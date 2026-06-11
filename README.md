# HDFC Banking Operations: Efficiency Optimization via Statistical Analysis (Z-Test)

📊 **Domain:** Banking Back-Office Operations & Workforce Analytics  
🛠️ **Tech Stack:** Python (Pandas, NumPy, SciPy.Stats, Matplotlib, Seaborn), Jupyter Notebook, Git  
🎯 **Statistical Methodology:** Two-Sample Z-Test for Means

---

## 📌 Business Overview & Problem Statement
In banking back-office operations, **Transaction Processing Time (TAT)** is a critical Key Performance Indicator (KPI). HDFC Bank's operations team recently migrated from an older legacy data-entry software to a newly optimized automation-assisted platform. 

The core objective of this project is to statistically validate whether the new software significantly reduces processing times or if any observed changes are merely due to random variance. 

---

## 🔬 Hypothesis Setup
To perform a rigorous statistical check, we define our hypotheses at a **95% Confidence Level ($\alpha = 0.05$)**:

* **Null Hypothesis ($H_0$):** $\mu_{\text{old}} = \mu_{\text{new}}$ (The mean processing time of the legacy software is equal to the new software; the upgrade has no impact).
* **Alternative Hypothesis ($H_1$):** $\mu_{\text{old}} \neq \mu_{\text{new}}$ (The mean processing time is significantly different between the two software systems).

---

## 🛠️ Project Workflow & Implementation

### 1. Data Collection & Preprocessing
* Simulated historical banking log data consisting of $n > 30$ sample sizes (satisfying the Central Limit Theorem for Z-Test).
* Cleaned missing values and structured processing hours for both legacy and automated systems using **Pandas**.

### 2. Exploratory Data Analysis (EDA)
* Plotted distribution curves (KDE plots) to check the normality of processing times.
* Generated box plots to spot outliers in back-office operational data.

### 3. Statistical Testing (The Z-Test Core)
* Calculated sample means ($\bar{X}_1, \bar{X}_2$) and population variances ($\sigma^2$).
* Computed the **Z-Statistic** and derived the two-tailed **P-Value** using Python's `scipy.stats`.

---

## 📈 Key Insights & Results

| Metric | Legacy Software | New Automated Software |
| :--- | :--- | :--- |
| **Sample Size ($n$)** | 100+ Transactions | 100+ Transactions |
| **Avg. Processing Time**| 28.4 Hours / Batch | 22.1 Hours / Batch |
| **Z-Statistic** | **Calculated Value > 1.96 (Critical Value)** |
| **P-Value** | **$< 0.05$ (Statistically Significant)** |

### 🚨 Final Data Verdict:
> **Result:** Since the **P-Value is significantly less than 0.05**, we **Reject the Null Hypothesis ($H_0$)**. 
> 
> **Business Impact:** We conclude with 95% statistical confidence that the new software has drastically improved back-office operational speed, saving an average of **6.3 hours per batch processing**. This directly enhances the bank's operational efficiency and customer satisfaction levels.

---

## 📂 Repository Structure
```text
├── HDFC_Banking_Ops_ZTest_Analysis.ipynb  # Core Jupyter Notebook with Python Code
├── banking_ops_data.csv                   # Cleaned Operational Dataset
└── README.md                              # Professional Project Documentation
