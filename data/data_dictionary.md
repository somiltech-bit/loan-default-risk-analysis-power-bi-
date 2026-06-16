# Data Dictionary

## Dataset Overview

This dataset contains information about loan applicants, their financial profiles, and loan default status. It is used to analyze borrower behavior, identify risk factors, and understand patterns associated with loan defaults.

### Dataset Summary

* Total Records: 255,348
* Domain: Financial Risk Analysis
* Data Type: Structured Tabular Data

---

## Column Definitions

| Column Name    | Data Type   | Description                                    |
| -------------- | ----------- | ---------------------------------------------- |
| LoanID         | Integer     | Unique identifier for each loan application    |
| Age            | Integer     | Age of the borrower                            |
| Income         | Decimal     | Annual income of the borrower                  |
| LoanAmount     | Decimal     | Approved loan amount                           |
| CreditScore    | Integer     | Borrower's credit score                        |
| MonthsEmployed | Integer     | Number of months employed                      |
| NumCreditLines | Integer     | Number of active credit lines                  |
| InterestRate   | Decimal     | Annual interest rate (%)                       |
| LoanTerm       | Integer     | Loan duration in months                        |
| DTIRatio       | Decimal     | Debt-to-Income ratio                           |
| Education      | Categorical | Highest education level attained               |
| EmploymentType | Categorical | Employment status of borrower                  |
| MaritalStatus  | Categorical | Marital status                                 |
| HasMortgage    | Boolean     | Indicates if borrower has an existing mortgage |
| HasDependents  | Boolean     | Indicates if borrower has dependents           |
| LoanPurpose    | Categorical | Purpose of the loan                            |
| HasCoSigner    | Boolean     | Indicates presence of a co-signer              |
| Default        | Boolean     | Loan default status (Target Variable)          |
| LoanDate       | Date        | Date when the loan was issued                  |

---

## Engineered Features

The following calculated fields were created in Power BI:

| Feature           | Description                                      |
| ----------------- | ------------------------------------------------ |
| Year              | Loan issue year extracted from LoanDate          |
| Income Bracket    | Low, Medium, High income categories              |
| Credit Score Bins | Very Low, Low, Medium, High credit score groups  |
| Age Groups        | Teen, Adults, Middle Age Adults, Senior Citizens |

---

## Target Variable

**Default**

* 0 → Loan not defaulted
* 1 → Loan defaulted

This variable is used to identify risky borrower segments and analyze default patterns.
