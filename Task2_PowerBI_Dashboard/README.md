# Task 2: Superstore Executive Sales & Profit Dashboard (Power BI)

## Overview
An interactive Power BI dashboard built on the Superstore sales data, with KPI cards, a monthly sales trend, Year and Region slicers, a category and sub-category treemap, a profitability matrix, a regional treemap and a state-level table.

## Data model (star schema)
- Fact_Orders
- Dim_Customer
- Dim_Product
- Dim_Date

## DAX measures
- Total Sales = SUM ( Fact_Orders[Sales] )
- Total Profit = SUM ( Fact_Orders[Profit] )
- Profit Margin % = DIVIDE ( [Total Profit], [Total Sales], 0 )
- Total Orders = DISTINCTCOUNT ( Fact_Orders[Order ID] )
- Total Quantity = SUM ( Fact_Orders[Quantity] )
- Avg Order Value = DIVIDE ( [Total Sales], [Total Orders], 0 )
- Sales LY = CALCULATE ( [Total Sales], SAMEPERIODLASTYEAR ( Dim_Date[Date] ) )
- YoY Sales Growth % = DIVIDE ( [Total Sales] - [Sales LY], [Sales LY] )

## Key insights
- Total sales are about 2.30M with about 286K profit (12.5% margin).
- Furniture earns only about a 2.5% margin; Tables and Bookcases lose money.
- The Central region has the lowest margin; the West has the highest sales.

## Files
- Superstore_Executive_Dashboard.pbix: Power BI report
- Superstore_Executive_Dashboard.pdf: exported dashboard
- data/: the model tables (CSV)
- Screenshots/: dashboard screenshots
