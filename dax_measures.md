# DAX Measures & Calculated Columns

## Overview

This project uses DAX (Data Analysis Expressions) to create business KPIs, perform time-intelligence analysis, and build borrower segmentation for financial risk analysis.

---

# Calculated Columns

## 1. Year

Extracts the loan issue year from the loan date.

```DAX
Year =
YEAR('Loan_default'[Loan_Date_DD_MM_YYYY].[Date])
```

---

## 2. Income Bracket

Categorizes borrowers into income groups.

```DAX
Income Bracket =
SWITCH(
TRUE(),
'Loan_default'[Income] < 30000,"Low Income",
'Loan_default'[Income] < 60000,"Medium Income",
"High Income"
)
```

---

## 3. Credit Score Bins

Categorizes borrowers based on credit score.

```DAX
Credit Score Bins =
IF(
'Loan_default'[CreditScore] < 400,"Very Low",
IF(
'Loan_default'[CreditScore] < 450,"Low",
IF(
'Loan_default'[CreditScore] < 650,"Medium",
"High"
)))
```

---

## 4. Age Groups

Segments borrowers by age.

```DAX
Age Groups =
IF(
'Loan_default'[Age] <= 19,"Teen",
IF(
'Loan_default'[Age] <= 39,"Adults",
IF(
'Loan_default'[Age] <= 59,"Middle Age Adults",
"Senior Citizens"
)))
```

---

# Time Intelligence Measures

## 5. YOY Default Loans Change (%)

Calculates Year-over-Year percentage change in default loans.

```DAX
YOY Default Loans Change
```

---

## 6. YOY Loan Amount Change (%)

Calculates Year-over-Year percentage change in loan amount.

```DAX
YOY Loan Amount Change
```

---

## 7. YTD Loan Amount

Calculates cumulative loan amount year-to-date.

```DAX
YTD Loan Amount
```

---

# Financial Analysis Measures

## 8. Average Loan Amount (High Credit)

Calculates average loan amount for borrowers with high credit scores.

```DAX
Average Loan Amount (High Credit)
```

---

## 9. Total Loan Amount (Credit Bins)

Calculates total loan amount grouped by credit score category.

```DAX
Total Loan (Credit Bins)
```

---

## 10. Median Loan Amount by Credit Score Bins

Calculates median loan amount across credit score categories.

```DAX
Median by Credit Score Bins
```

---

# Demographic Analysis Measures

## 11. Loans by Education Type

Counts loans by education category.

```DAX
Loans by Education Type
```

---

## 12. Total Loan (Middle Age Adults)

Calculates total loan amount for middle-age borrowers.

```DAX
Total Loan (Middle Age Adults)
```

---

## 13. Average Income by Employment Type

Calculates average borrower income across employment categories.

```DAX
Average Income by Employment Type
```

---

## 14. Average Loan Amount by Age Group

Calculates average loan amount for each age group.

```DAX
Average Loan Amount by Age Group
```

---

# Risk Analysis Measures

## 15. Default Rate by Employment Type

Calculates default percentage across employment categories.

```DAX
Default Rate by Employment Type
```

---

## 16. Default Rate by Year

Calculates yearly loan default percentage.

```DAX
Default Rate by Year
```

---

## 17. Loan Amount by Purpose

Calculates total loan amount distributed across loan purposes.

```DAX
Loan Amount by Purpose
```

---

# Key DAX Concepts Used

* Calculated Columns
* Measures
* Time Intelligence
* Context Transition
* Filter Context
* Row Context
* CALCULATE()
* FILTER()
* DIVIDE()
* AVERAGE()
* MEDIANX()
* SUM()
* COUNTROWS()
* DATESYTD()
* ALLEXCEPT()
* SWITCH()

These DAX calculations were used to build interactive dashboards and derive actionable business insights related to borrower behavior, credit risk, and financial performance.
