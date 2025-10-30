# 🏦 Bank Loan Case Study

### 🎯 Objective
Analyze historical loan data to uncover key factors influencing loan repayment behavior and identify patterns leading to customer defaults.  
Goal: Help the bank make safer, data-driven loan approval decisions by identifying high-risk applicants early.

---

### 🧰 Tools & Technologies
- **Power BI** – Data visualization and dashboard creation  
- **SQL (MySQL Workbench)** – Querying and analysis  
- **Python (VS Code)** – Data cleaning and machine learning  
- **Excel** – Pre-processing and validation  

---

### 📊 Dashboard & Report
 
➡️ [Download Power BI Report (.pbix)](./bank_loan_dashboard.pbix)


---

### 🎞️ Presentation
  
➡️ [Download Presentation (.pptx)](./Bank Loan.pptx)

---

### 🔍 Approach
1. **Data Cleaning & Preparation**  
   - Reduced dataset from 122 → 32 features by removing duplicates and low-variance columns.  
   - Fixed invalid ages and extreme income outliers.  
   - Mean imputation for missing EXT_SOURCE_1–3 values.  
   - Imported cleaned data into MySQL and Power BI.

2. **Exploratory Data Analysis (EDA)**  
   - Family size, income, gender, age, education level, and past credit history analyzed.  
   - SQL queries and Power BI visuals used for trend discovery.

3. **Machine Learning Component**  
   - Built classification models using **CatBoost** and **LightGBM**.  
   - Addressed class imbalance (~8% defaulters) using class weights and threshold tuning.  
   - Optimized for high recall (~85%) to catch potential defaulters early.

---

### 💡 Key Insights
- **91%** of customers show no repayment issues — overall low default rate.  
- **Younger** and **less experienced** customers have higher default risks.  
- **Larger families** show weaker repayment capacity.  
- **Lower income** and **higher loan amounts** correlate with greater default probability.  
- **Higher education** levels lead to better repayment reliability.  
- Past **credit refusals** are a strong indicator of future default.

---

### ⚙️ Model Evaluation
- **Model Used:** CatBoost / LightGBM  
- **Metric Priority:** Recall (detecting defaulters)  
- **Result:** ~85% recall with balanced precision through threshold tuning.  
- **Business Use:** Acts as an early risk-alert system to support manual review for flagged applicants.

---

### 🧭 Business Recommendations
- Strengthen screening for **younger** or **low-experience** applicants.  
- Offer **custom loan terms** (smaller amounts or higher rates) to borderline profiles.  
- Prioritize **low-risk segments** (consistent repayment, strong credit history).  
- Integrate model insights into loan approval workflow for **data-driven decision-making**.

---

### 🧠 Key Learnings
- Real-world data requires **domain understanding and judgment** to clean effectively.  
- **Simple, interpretable models** can outperform complex ones when aligned with business goals.  
- Each project iteration improves analysis quality — **reflection drives growth**.  

---

### 📁 Repository Structure

