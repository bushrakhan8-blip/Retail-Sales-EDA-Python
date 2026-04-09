# 🛍️ Retail Sales Exploratory Data Analysis — Python

## Overview
An exploratory data analysis (EDA) project using a real-world retail sales dataset. The analysis was performed in a **Microsoft Fabric** notebook environment using **Python**, **Pandas**, **Matplotlib**, and **Seaborn**. The project covers the full EDA workflow — from loading and cleaning data through to visualisation, correlation analysis, and aggregation.

## Dataset
Loaded from an Excel file (`online_sales_retailer.xlsx`) containing three sheets:

- `Sales` — transactional data including invoice number, stock code, quantity, unit price, and date
- `Invoice` — customer and country information per invoice
- `Product` — product categories and descriptions per stock code

## Tasks Completed

**Task 1 — Load the Data**
- Imported all three sheets into separate Pandas DataFrames (`df_sales`, `df_invoice`, `df_product`)
- Inspected structure and displayed first few rows of each table

**Task 2 — Basic Python & Pandas Operations**
- Checked for missing values in the Sales DataFrame — none found
- Calculated descriptive statistics (mean, median, mode, standard deviation) for `Quantity` and `UnitPrice`

**Task 3 — Merging DataFrames**
- Merged `df_sales` with `df_invoice` on `InvoiceNo`
- Merged the result with `df_product` on `StockCode` to create a single unified DataFrame

**Task 4 — Exploratory Data Analysis**
- Computed summary statistics using `describe()`
- Filtered transactions with zero quantity — none found
- Created a `Sales` column (`Quantity * UnitPrice`)
- Identified and visualised outliers via scatter plot; filtered them for cleaner analysis

**Task 5 — Data Visualisation**
- Scatter plot showing the relationship between `Quantity` and `Sales` — positive correlation observed
- Histogram of sales distribution — right-skewed, most transactions are low value
- Line chart of sales over time — generally steady with occasional large spikes

**Task 6 — Correlation Analysis**
- Calculated correlation between `Quantity` and `Sales` — moderate positive relationship (0.66)
- Visualised using a correlation heatmap

**Task 7 — Grouping & Aggregation**
- Grouped sales by `Product_Category` to find total revenue per category — uncategorised products and home décor categories (CANDLE, GLASS, MUG) were top earners
- Created a pivot table showing sales by `Country` and `Product_Category`

## Tools & Skills
`Python` · `Pandas` · `Matplotlib` · `Seaborn` · `Microsoft Fabric` · `EDA` · `Data Cleaning` · `Outlier Detection` · `Data Visualisation` · `Correlation Analysis` · `Pivot Tables`
