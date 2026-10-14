# Retail Sales Analysis using SQL and Power BI

## Project overview
This portfolio project analyzes retail orders using SQL and Power BI. It covers sales performance, profit, product categories, monthly trends, customer locations, payment methods, and order status.

> **Dataset note:** `data/retail_sales_dataset.csv` is a generated sample dataset created for this practice project. It is not a real company's data and should be described honestly on your resume or GitHub.

## Files
- `data/retail_sales_dataset.csv` — sample retail transaction data (1,200 rows)
- `sql/retail_sales_analysis.sql` — MySQL database setup and analysis queries
- `analysis/` — place your Power BI `.pbix` file here after building it
- `POWER_BI_GUIDE.md` — dashboard build instructions and DAX measures

## SQL workflow
1. Create a MySQL schema using the SQL script.
2. Import the CSV into a table named `retail_sales`.
3. Run the queries in `sql/retail_sales_analysis.sql`.

## Power BI workflow
1. Open Power BI Desktop → **Get data** → **Text/CSV**.
2. Select `data/retail_sales_dataset.csv`.
3. Check data types: `OrderDate` = Date; `Sales`, `Cost`, `Profit`, `UnitPrice` = Decimal number; `Quantity` = Whole number.
4. Create the measures from `POWER_BI_GUIDE.md`.
5. Build the dashboard using the suggested visuals.
6. Save the report as `analysis/Retail_Sales_Dashboard.pbix`.

## Suggested dashboard pages
- **Overview:** Total Sales, Total Profit, Total Orders, Units Sold; monthly sales line chart; sales by category bar chart.
- **Product & Geography:** top products by sales; sales by city; category slicer.
- **Order Insights:** order status, payment method, monthly trend.

## Important
This repository includes the dataset, SQL queries, and dashboard instructions. The Power BI `.pbix` report must be created in Power BI Desktop by following the guide; it is not included as a prebuilt binary.
