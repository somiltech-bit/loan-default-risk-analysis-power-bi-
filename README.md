# 💳 Loan Default Risk Analysis Dashboard

An end-to-end Power BI project that analyzes borrower behavior, loan default trends, and financial risk patterns using 2,55,348 loan application records.

This project transforms raw loan data into actionable business insights through data modeling, DAX calculations, and interactive dashboards.

---

# 🚀 Project Overview

Financial institutions need to identify high-risk borrowers and monitor lending patterns to minimize defaults.

This project provides a data-driven solution to analyze:

- Loan default trends over time
- Borrower demographics
- Financial risk indicators
- Credit score segmentation
- Income and employment analysis
- Loan distribution patterns

The final solution was developed as a 3-page interactive Power BI dashboard.

---

# 🎯 Business Objectives

This project aims to answer the following questions:

1. Which borrower segments have the highest default rates?
2. How do employment types influence loan performance?
3. How does credit score affect loan amount and default behavior?
4. Which loan purposes receive the highest loan amounts?
5. How do demographics impact borrowing patterns?
6. What are the Year-over-Year (YOY) changes in loan amounts and defaults?
7. How can financial institutions identify high-risk borrower groups?

---

# 📊 Dataset Information

Dataset Size:

- Total Records: 255,348
- Total Features: 18

Columns:

- LoanID
- Age
- Income
- LoanAmount
- CreditScore
- MonthsEmployed
- NumCreditLines
- InterestRate
- LoanTerm
- DTIRatio
- Education
- EmploymentType
- MaritalStatus
- HasMortgage
- HasDependents
- LoanPurpose
- HasCoSigner
- Default
- Loan Date

---

# 🛠️ Tech Stack

Tools Used:

- Power BI
- Power Query
- DAX
- Microsoft Excel

Skills Demonstrated:

- Data Cleaning
- Data Transformation
- Data Modeling
- Data Visualization
- Financial Risk Analysis
- Business Intelligence
- KPI Development
- Time Intelligence Analysis
- Dashboard Design

---

# ⚙️ Data Preparation

Performed the following preprocessing steps:

- Imported and validated the dataset
- Created a Date hierarchy
- Removed unnecessary fields
- Standardized data types
- Built calculated columns
- Created business categories for analysis

---

# 🧮 DAX Calculations

Created custom DAX measures and calculated columns.

### Calculated Columns

### Year

```DAX
Year = YEAR([Loan_Date])
```

### Income Bracket

```DAX
Income Bracket =
SWITCH(
TRUE(),
[Income] < 30000,"Low Income",
[Income] < 60000,"Medium Income",
"High Income"
)
```

### Credit Score Bins

```DAX
Credit Score Bins =
IF([CreditScore]<400,"Very Low",
IF([CreditScore]<550,"Low",
IF([CreditScore]<650,"Medium","High")))
```

### Age Groups

```DAX
Age Groups =
IF([Age]<19,"Teen",
IF([Age]<39,"Adults",
IF([Age]<59,"Middle Age Adults",
"Senior Citizens")))
```

---

# 📈 DAX Measures

Implemented various KPIs including:

- Default Rate (%)
- Average Income by Employment Type
- Average Loan Amount by Age Group
- Number of Loans by Education Type
- Median Loan Amount by Credit Score Category
- Total Loan Amount
- YTD Loan Amount
- YOY Loan Amount Change
- YOY Default Loan Change

---

# 📑 Dashboard Pages

## 1️⃣ Loan Default & Overview

Key insights:

- Loan Amount by Purpose
- Average Income by Employment Type
- Default Rate by Employment Type
- Average Loan Amount by Age Group
- Default Rate by Year

---

## 2️⃣ Applicant Demographics & Financial Profile

Key insights:

- Median Loan Amount by Credit Score Category
- Loan Distribution by Age Groups
- Loan Distribution by Mortgage/Dependents
- Number of Loans by Education Type
- Loan Analysis by Marital Status

---

## 3️⃣ Financial Risk Metrics

Key insights:

- Year-over-Year Loan Amount Change
- Year-over-Year Default Loan Change
- YTD Loan Amount Analysis
- Income Bracket Analysis
- Employment Type Analysis

---

# 🔍 Key Business Insights

### 📌 Employment Risk

Unemployed borrowers exhibited the highest default rates compared to other employment categories.

### 📌 Credit Score Impact

Borrowers with stronger credit profiles generally showed lower financial risk.

### 📌 Income Segmentation

High-income borrowers accounted for the largest share of total loan amounts.

### 📌 Demographic Analysis

Loan behavior varied significantly across age groups, education levels, and marital statuses.

### 📌 Financial Trends

YOY analysis revealed fluctuations in both loan amounts and default percentages over time.

---

# 📂 Repository Structure

```

loan-default-risk-analysis-power-bi/

│

├── README.md

├── powerbi/
│ └── loan_default_dashboard.pbix

├── screenshots/
│ ├── dashboard_overview.png
│ ├── demographics.png
│ └── financial_risk_metrics.png

├── data/
│ ├── loan_default.csv
│ └── data_dictionary.xlsx

└── docs/
└── dax_measures.md

```

---

# 📸 Dashboard Preview

Dashboard includes:

- Loan Default & Overview
- Applicant Demographics & Financial Profile
- Financial Risk Metrics

---

# 🔮 Future Improvements

Potential enhancements:

- Build a machine learning model to predict default probability
- Deploy dashboards to Power BI Service
- Add drill-through functionality
- Add borrower risk scoring
- Build real-time dashboards

---

# 🏆 Project Outcome

Successfully built an end-to-end Business Intelligence solution that converts raw loan data into actionable financial insights for risk assessment and decision-making.

---

# 👨‍💻 Author

Somil Verma

LinkedIn: https://www.linkedin.com/in/somil-verma-576a02305/

****
