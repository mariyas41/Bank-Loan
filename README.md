# 🏦 **Bank Loan Case Study**

---

## 🎯 **Objective**
Analyze historical loan data to uncover key factors influencing loan repayment behavior and identify patterns leading to customer defaults.  
**Goal:** Help the bank make safer, data-driven loan approval decisions by identifying high-risk applicants early.

---

## 🧰 **Tools & Technologies**
- **Power BI:** Data visualization and dashboard creation  
- **SQL (MySQL Workbench):** Querying and analysis  
- **Python (VS Code):** Data cleaning and machine learning  
- **Excel:** Pre-processing and validation  

---

## 📊 **Dashboard & Report**

➡️ [**Download Power BI Report (.pbix)**](https://drive.google.com/file/d/1ii_fkYFg6W5eWQ4ElD5hkXPNwLHQzuRc/view?usp=sharing)

---

### 🎞️ **Presentation**
  
➡️ [**Download Presentation (.pptx)**](./Bank_Loan.pptx)

---

## 🔍 **Approach**

### 🧹 **Data Cleaning & Preparation**
- Reduced dataset from 122 → 32 features by removing duplicates and low-variance columns.  
- Fixed invalid ages and extreme income outliers.  
- Mean imputation for missing `EXT_SOURCE_1–3` values.  
- Imported cleaned data into **MySQL** and **Power BI** for further analysis.

### 📈 **Exploratory Data Analysis (EDA)**
- Analyzed family size, income, gender, age, education level, and past credit history.  
- SQL queries and Power BI visuals used for trend discovery.

### 🤖 **Machine Learning Component (Interpretative Use Only)**
- Built classification models using **CatBoost** and **LightGBM**.  
- Addressed class imbalance (~8% defaulters) using class weights and threshold tuning.  
- Optimized for **high recall (~85%)** to catch potential defaulters early.

---

## 💡 **Key Insights**
- **91%** of customers show no repayment issues — overall low default rate.  
- **Younger and less experienced** customers have higher default risks.  
- **Larger families** show weaker repayment capacity.  
- **Lower income and higher loan amounts** correlate with greater default probability.  
- **Higher education levels** lead to better repayment reliability.  
- **Past credit refusals** are a strong indicator of future default.

---

## ⚙️ **Model Evaluation**

| Metric | Value | Purpose |
|:--|:--:|:--|
| **Recall** | 0.85 | Detect potential defaulters early |
| **Precision** | 0.70 | Maintain review accuracy |
| **Accuracy** | 0.91 | Balanced model performance |
| **Business Use** | Risk-alert system | Supports manual review of flagged applicants |

---

## 🧠 **Key Learnings**
- Real-world data requires **domain understanding** to clean effectively.  
- In credit risk, **recall > accuracy** — catching defaulters saves money.  
- Simple, interpretable models often work best when aligned with business goals.  
- Combining **SQL + Power BI + Python** gives a complete end-to-end analytical view.

---

## ✍️ **Author**
**Mariya Shaji**  

---


