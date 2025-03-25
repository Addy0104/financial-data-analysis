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

2. Run analysis queries:
```sql
-- Customer lifetime value
SELECT customer_id, SUM(balance) as net_worth 
FROM accounts 
GROUP BY customer_id;
```
```

-- Customer distribution by city
SELECT city, COUNT(*) AS customer_count
FROM customers
GROUP BY city
ORDER BY customer_count DESC;

-- Credit score distribution
SELECT 
  CASE 
    WHEN credit_score >= 800 THEN 'Excellent'
    WHEN credit_score >= 740 THEN 'Very Good'
    WHEN credit_score >= 670 THEN 'Good'
    WHEN credit_score >= 580 THEN 'Fair'
    ELSE 'Poor' 
  END AS credit_rating,
  COUNT(*) AS count,
  ROUND(COUNT(*)/(SELECT COUNT(*) FROM customers)*100,1) AS percentage
FROM customers
GROUP BY credit_rating
ORDER BY credit_rating;
```
