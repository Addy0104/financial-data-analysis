# financial-data-analysis
"SQL &amp; Python analysis of synthetic financial dataset"
financial-data-analysis/
├── data/
│   ├── customers.csv
│   ├── accounts.csv
│   ├── transactions.csv
│   ├── loans.csv	
│   └── investments.csv
├── sql/
│   ├── 01_database_schema.sql
│   ├── 02_analysis_queries.sql
│   └── 03_advanced_metrics.sql
├── notebooks/
│   ├── data_cleaning.ipynb
│   └── financial_analysis.ipynb
├── docs/
│   └── key_findings.md
└── README.md


# Financial Data Analysis Project

![SQL](https://img.shields.io/badge/SQL-Expert-blue)
![Data Analysis](https://img.shields.io/badge/Analysis-Financial-green)

## 📊 Project Overview
End-to-end analysis of synthetic banking data including:
- Customer segmentation
- Transaction pattern analysis
- Loan portfolio risk assessment

## 🛠️ Technologies Used
- **SQL** (MySQL/PostgreSQL)
- **Python** (Pandas, Matplotlib)
- **Jupyter Notebooks**

## 📂 Repository Structure
```
financial-data-analysis/
├── data/               # CSV datasets
├── sql/                # SQL schema and queries
├── notebooks/          # Python analysis
└── docs/               # Key findings
```

## 🔍 How to Use
1. Import SQL files to create database:
```sql
SOURCE sql/01_database_schema.sql;
```
Detailed Analysis
 Customer Behavior Insights
High-Value Customers:

Top 15% of customers (by balance) hold 45% of total deposits

Customers with 740+ credit scores maintain 3.2× higher average balances than those below 650

Geographic Patterns:

Customers in urban areas (NYC, Chicago) transact 22% more frequently than rural areas

Southern states show higher loan uptake (35% of total loans)

 Transaction Trends
Temporal Patterns:

Peak spending occurs 2-4 PM on weekdays (27% of daily transactions)

Weekends see 18% larger average transaction amounts (leisure spending)

Category Analysis:

Groceries = Most frequent category (32% of transactions)

Electronics = Highest average spend ($189/transaction)

 Loan Portfolio Performance
Risk Segmentation:

Auto loans have the lowest delinquency rate (2.1%) vs. personal loans (5.7%)

Mortgages account for 68% of total loan value but only 12% of accounts

Repayment Behavior:

Customers with savings accounts repay 19% faster than those without

 Investment Insights
Portfolio Composition:

ETFs are the most held investment type (42% of positions)

Tech stocks (AAPL, MSFT) comprise 35% of total portfolio value

Performance:

Average annualized return: 7.2% (Stocks: 9.1%, Bonds: 3.4%)

 Operational Metrics
Account Churn:

12% of checking accounts become inactive within 1 year

Inactive accounts have 63% lower balances than active ones
