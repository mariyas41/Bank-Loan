🏦 Bank Loan Case Study
🎯 Objective

Analyze historical loan data to uncover key factors influencing repayment behavior and identify early-stage default risks.
Goal: Enable safer, data-driven loan approvals by flagging high-risk applicants before disbursal.

🧰 Tools & Technologies

Power BI: Data visualization & dashboard creation

SQL (MySQL Workbench): Data querying & analysis

Python (VS Code): Data cleaning & model analysis

Excel: Pre-processing & validation

📊 Dashboard & Report

➡️ Download Power BI Report (.pbix)

🎞️ Presentation

➡️ Download Presentation (.pptx)

🔍 Approach
🧹 Data Cleaning & Preparation

Reduced 122 → 32 features by removing duplicates & low-variance columns

Fixed invalid ages and extreme income outliers

Imputed missing EXT_SOURCE_1–3 values with mean substitution

Loaded cleaned data into MySQL and Power BI for visualization

📈 Exploratory Data Analysis (EDA)

Analyzed family size, income, age, education, and credit history

Combined SQL queries with Power BI visuals to uncover default trends

🤖 Machine Learning (Interpretative Only)

Built classification models using CatBoost and LightGBM

Addressed 8 % class imbalance using class weights & threshold tuning

Optimized for recall ≈ 85 % to catch potential defaulters early

Identified education, income, and experience as key predictors

💡 Key Insights

91 % of customers show no repayment issues → overall low default rate

Younger & less experienced applicants have higher default risk

Larger families show weaker repayment capacity

Lower income / higher loan amounts increase default probability

Higher education improves repayment reliability

Past credit refusals strongly predict future defaults

⚙️ Model Evaluation
Metric	Value	Purpose
Recall	0.85	Catch defaulters early
Precision	0.70	Maintain review efficiency
Accuracy	0.91	Balanced model
Business Use	Risk alert system	Support manual review of flagged applicants
🧠 Key Learnings

Real-world data cleaning demands statistical and domain understanding

In credit risk, recall > accuracy — catching defaulters protects revenue

Combining SQL + Power BI + Python completes the analytics pipeline

Each iteration improves data storytelling and business insight
