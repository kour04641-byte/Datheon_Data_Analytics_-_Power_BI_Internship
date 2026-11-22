# Task 3: Customer Cohort & Churn Analytics (IBM Telco)

## Overview
Segmented telecom customers by tenure cohort, contract type, payment method and monthly charges; computed retention curves (Kaplan-Meier) and churn probability; identified high-risk segments and wrote retention recommendations.

## Key findings
- Baseline churn is 26.5% (1,869 of 7,043 customers); about 55% of churners leave within 12 months.
- Churn by contract: month-to-month 42.7%, one-year 11.3%, two-year 2.8%.
- Electronic-check payers churn at 45.3%, versus 15-19% for other payment methods.
- Fiber optic customers without tech support churn at 49.4% (22.6% with support).
- Month-to-month + fiber + no support + electronic check: 62.9% churn probability.

## Method note
The data is a single snapshot with no signup dates, so cohorts are built from the tenure column.

## Files
- Task3_Telco_Churn_Analysis.ipynb: full analysis
- telco_customer_churn.csv: original dataset
- telco_churn_clean.csv: cleaned dataset

## How to run
pip install pandas numpy matplotlib seaborn jupyter
Open the notebook and run all cells.
