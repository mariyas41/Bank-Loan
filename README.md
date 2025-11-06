# 🏦 **Bank Loan Case Study — Credit Risk Analysis**

## 🎯 **Objective**
Analyze historical loan data to identify patterns influencing repayment behavior and help the bank make **data-driven lending decisions**.  
**Goal:** Detect potential defaulters early, reduce financial loss, and optimize the manual review process.

---

## 💼 **Business Context**
Banks face two key challenges:
- **Lost opportunity:** Safe customers get rejected due to overly cautious screening.  
- **Financial loss:** Risky customers get approved and default later.  

By understanding **who defaults and why**, we can build a model that supports balanced, profitable, and safe lending.

---

## 🧰 **Tools & Technologies**
- **Power BI** → Data visualization and interactive dashboards  
- **SQL (MySQL Workbench)** → Querying, trend discovery, and aggregation  
- **Python (VS Code)** → Data cleaning, feature processing, and model building  
- **Excel** → Data inspection and preliminary validation  

---

## 🔍 **Approach**

### 🧹 **1. Data Cleaning & Preparation**
- Reduced dataset from **122 → 32 features** by removing irrelevant, duplicate, and high-missing columns.  
- Replaced **invalid ages** (e.g., 1001 years) with realistic estimates derived from `work_experience + 18`.  
- Flagged and removed **income outliers** > ₹10 crore (<0.01 % of records).  
- Imputed missing `EXT_SOURCE_1–3` values using mean to retain external credit score information.  
- Rounded fractional family sizes for demographic consistency.  
- Imported cleaned dataset into **MySQL** for querying and **Power BI** for visualization.

---

## 📈 **2. Exploratory Data Analysis (EDA)**

| Factor | Analytical Finding |
|:--|:--|
| **Customer Reliability** | 91 % of customers have no repayment issues → stable portfolio. |
| **Family Size** | Default risk rises sharply for large families (9 + members). |
| **Age** | Younger borrowers (< 30 yrs) have the highest default rate. *(t = –17.8, p < 0.001)* |
| **Work Experience** | Default rate drops steadily with more experience. *(t = –17.4, p < 0.001)* |
| **Income & Credit** | Low income and large loan amounts both increase default probability. *(t = –5.19, p < 0.001)* |
| **Previous Refusals** | Strongest behavioral signal — default risk doubles after ≥ 2 refusals. |
| **Client Type** | “Refresher” clients (repeat borrowers) are most reliable (6.7 % default). |
| **Education Level** | Higher education → lower default. *(χ² = 213.8, p < 0.001)* |

---

## 🤖 **3. Machine Learning — CatBoost Classifier**

A **decision-support model** was built to prioritize loan application reviews.  
It helps analysts focus on the riskiest 66 % of applicants while safely auto-approving the low-risk 34 %.

### ⚙️ **Model Evaluation**

| Metric | Class | Value | Interpretation |
|:--|:--|:--:|:--|
| **Precision** | Non-Defaulters (0) | **0.96** | 96 % of customers predicted as “safe” were truly non-defaulters. |
| **Recall** | Non-Defaulters (0) | **0.33** | Model correctly identified one-third of all safe customers; intentionally low because priority was recall on defaulters. |
| **Precision** | Defaulters (1) | **0.10** | 10 % of flagged risky customers actually defaulted. |
| **Recall** | Defaulters (1) | **0.86** | Model caught 86 % of all true defaulters — the key objective. |
| **Accuracy** | Overall | **0.37** | Lower due to recall-first tuning in an 8 %-imbalanced dataset. |
| **F1-Score (Class 1)** | — | **0.18** | Reflects trade-off between catching defaulters and precision. |


---

### 🔎 **Interpretation**
- Out of 50 000 applicants, the model **flags 66 %** for manual review.  
  Among these, it captures **≈ 85 % of all actual defaulters**.  
- The remaining **34 % predicted “safe”** segment shows **96 % precision**, meaning they can be auto-approved with minimal risk.  
- This reduces **manual workload by one-third** while maintaining a high defaulter-capture rate.  
- The model serves as a **smart filter** — *not an auto-decision system* — guiding analysts toward riskier cases first.

---

## 💡 **4. Business Insights & Recommendations**

1. **High-Risk Segments** → Younger borrowers, large families, low income, multiple past refusals.  
2. **Reliable Segments** → Educated, experienced, and previously consistent customers.  
3. **Operational Strategy**
   - Prioritize manual review of the flagged 66 %.  
   - Auto-approve the low-risk 34 % with high precision (96 %).  
   - Customize loan terms (smaller amounts, adjusted rates) for borderline cases.  
4. **Business Impact**
   - Manual review effort reduced by **≈ 33 %**.  
   - Potential default losses minimized by **catching 85 % of risky applicants early**.  

---

## 📊 **Power BI Dashboard**
- KPI Cards → Total Applicants, Default %, High-Risk Segment Size  
- Drill-downs → Age, Income, Family Size, Education, Experience  
- Filters → Gender, Client Type, Credit History  
- Visualization Flow → Overview → Demographics → Behavior → Recommendations  

📁 [**Download Power BI Report (.pbix)**](https://drive.google.com/file/d/1ii_fkYFg6W5eWQ4ElD5hkXPNwLHQzuRc/view?usp=sharing)  
📑 [**View Presentation (.pptx)**](./Bank_Loan.pptx)


---

## ✍️ **Author**
**Mariya Shaji**  
📂 [GitHub Profile](https://github.com/mariyas41)  

---





---


