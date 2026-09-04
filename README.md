# Northwind Traders: Sales Performance and Growth Analysis

A data analysis project examining sales trends, product performance, customer concentration, and employee performance for Northwind Traders, a specialty food and beverage importer/exporter, using their historical order data.

## Business Question

How has Northwind's sales performance changed over time, and what is driving that growth or decline?

## Key Findings

- **Revenue grew steadily**, from about $27,800/month in July 2024 to $123,800/month by April 2026.
- **Product revenue is concentrated**: the top 3 products account for ~23% of all revenue, with Côte de Blaye alone contributing ~11%, a supply risk worth flagging.
- **Geographic revenue is concentrated in core markets**: the top 5 countries (USA, Germany, Austria, Brazil, France) generate ~63% of total revenue.
- **Sales team performance splits into two patterns**: high-volume sellers (e.g. Margaret Peacock) versus high-value-per-deal sellers (e.g. Anne Dodsworth).

## Recommendations

1. Track monthly revenue against this baseline going forward, since growth
   has not been perfectly smooth, an early slowdown could otherwise go
   unnoticed.
2. Secure supply continuity (backup suppliers, safety stock) for the top 3
   products, given how much of total revenue depends on them.
3. Continue investing in the top 5 core markets, while testing the long
   tail of smaller countries as an area for growth, since they currently
   contribute little individually.
4. Evaluate the sales team on both total revenue and average order value,
   not total revenue alone, so high-value sellers are not undervalued
   relative to high-volume ones.

## Visuals

![Monthly Revenue Trend](images/monthly_revenue_trend.png)
![Top 10 Products by Revenue](images/top_10_products.png)
![Revenue by Country](images/revenue_by_country.png)

## Data

This project uses the [Northwind Traders sample database](https://github.com/microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs), specifically the orders, order details, products, categories, customers, and employees tables. Supplier, shipper, and territory data were excluded, as they relate to logistics questions outside this project's sales performance scope.

## Limitations

This analysis covers roughly 22 months of order history (July 2024 to
April 2026) and focuses on sales performance only. It does not include
shipping cost, delivery reliability, or inventory data, these fall outside
this project's scope and would be natural next steps for a follow-up
analysis. Product, customer, and employee identities reflect this sample
dataset and are not real Northwind Traders records.

## Tools

Python, pandas, matplotlib, seaborn, Jupyter Notebook

## How to Run

1. Clone or download this repository
2. Create and activate a virtual environment:
   `py -m venv venv` then `venv\Scripts\activate` (Windows)
3. Install dependencies: `pip install -r requirements.txt`
4. Open `notebooks/Northwind_Sales_Analysis.ipynb` in Jupyter or VS Code,
   and select the `venv` kernel
5. Run all cells

## Project Structure

```
Northwind-Sales-Analysis/
├── data/
│   ├── processed/
│   |   └── sales_fact_table.csv
│   ├── raw/
│   |   ├── categories.csv
│   |   ├── customers.csv
│   |   ├── employee_territories.csv
│   |   ├── employees.csv
│   |   ├── order_details.csv
│   |   ├── orders.csv
│   |   ├── products.csv
│   |   ├── regions.csv
│   |   ├── shippers.csv
│   |   ├── suppliers.csv
│   |   └── territories.csv
│   └── data_dictionary.csv
├── images/
│   ├── employee_performance.png
│   ├── monthly_revenue_trend.png
│   ├── revenue_by_category.png
│   ├── revenue_by_country.png
│   ├── top_10_customers.png
│   └── top_10_products.png
├── notebooks/
│   └── Northwind_Sales_Analysis.ipynb
├── README.md
└── requirements.txt
```

## Full Analysis

See the full notebook for detailed methodology, data cleaning steps, and findings for each section: notebooks/Northwind_Sales_Analysis.ipynb
