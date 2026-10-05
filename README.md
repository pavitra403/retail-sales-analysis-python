# Retail Sales Analysis & Automated Reporting (Python)

Analysis of 20,000 retail orders (Jan 2023 – Dec 2025) using Python, with an automated Excel summary report.

## Dataset
Retail sales dataset from Kaggle: https://www.kaggle.com/datasets/abirambharathisa/india-retail-sales-dataset-2023-2025
20,000 orders, 17 columns (order date, region, city, category, product, price, quantity, discount, sales, profit, channel, payment method, rating).

## Tools
Python, Pandas, Matplotlib, Google Colab

## What I did
1. **Inspected the data:** checked shape, data types, missing values and duplicates.
2. **Cleaned and validated:** converted order_date to a date type, created a month column, found no duplicates, no zero or negative quantity or sales, and confirmed sales = unit_price × quantity × (1 − discount) for every row. 200 missing ratings (1%) were kept, because they do not affect sales analysis.
3. **Analysed:** calculated KPIs and compared sales and profit by category, region, channel, month and discount level.
4. **Visualised:** made 4 charts with Matplotlib (monthly sales, profit by category, sales by region, average profit by discount).
5. **Automated reporting:** wrote a function, `make_report()`, that reads the raw CSV and produces an Excel report with 5 sheets (Summary, Monthly, By Category, By Region, By Channel).

## Key findings
- Total sales: 222.1M, total profit: 34.3M, profit margin: 15.46%, average order value: 11,104.
- Electronics contributed about 84% of total sales and profit.
- South was the top region (about 32% of sales); East was the weakest (about 17%).
- Online was the top channel (about 45% of sales).
- Sales peaked in October–November each year, and 2025 sales were about 25% higher than 2024.
- Average profit per order fell from about 2,042 (no discount) to about 395 (30% discount).
- All 387 loss-making orders (about 2%) had discounts of 15% or more; about one third of orders at 30% discount lost money.

Note: these results show association, not proven cause.

## Files
- `Online_Retail_Analysis.ipynb`: full code, outputs and charts
- `monthly_sales_report.xlsx`: the automatically generated report

## Author
Pavitra S Patil | [LinkedIn](https://www.linkedin.com/in/pavitra-patil-46494a392)
