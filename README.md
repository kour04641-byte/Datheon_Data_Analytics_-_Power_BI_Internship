# Superstore Retail Sales – Exploratory Data Analysis

Datheon Data Analytics & Power BI Internship – **Task 1**

## Objective
Clean the Superstore sales dataset and analyse purchase volume, monthly seasonality,
category-wise revenue and discount sensitivity, then summarise 5 executive takeaways.

## Files
| File | Description |
|---|---|
| `Task1_Superstore_EDA.ipynb` | Main notebook: cleaning code, charts, 5 annotated business findings |
| `superstore_sales.csv` | Original dataset |

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Data cleaning summary
- Removed 806 non-order rows (lookup tables appended to the CSV); 9,994 order lines remain
- Filled 11 missing postal codes (Burlington, VT) and stored postal codes as text
- Parsed order and ship dates; created Year-Month, Ship Days and Profit Margin
- Checked for duplicates, invalid dates and invalid discounts (none found)

## Key findings
1. Discounts above 20% make orders loss-making (margin about -119% above 50%)
2. Furniture earns only about a 2.5% margin because Tables and Bookcases lose money
3. September to December generates about 52% of annual sales
4. The Central region has the lowest margin (about 7.9%); Texas, Ohio and Pennsylvania lose the most
5. Technology leads on profit; the top 20% of customers drive about 48% of sales

## How to run
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Task1_Superstore_EDA.ipynb
```
Run all cells from top to bottom (the CSV must be in the same folder).
