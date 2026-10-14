# Power BI Dashboard Guide

## Import and prepare
Import `data/retail_sales_dataset.csv` using **Get data → Text/CSV**. In Power Query:
- Set `OrderDate` to Date.
- Set `Quantity` to Whole number.
- Set `UnitPrice`, `Discount`, `Sales`, `Cost`, and `Profit` to Decimal number.
- Review blanks and duplicate `OrderID` values. This sample is designed with one row per order.

## DAX measures
```DAX
Total Sales = SUM(retail_sales[Sales])

Total Profit = SUM(retail_sales[Profit])

Total Orders = DISTINCTCOUNT(retail_sales[OrderID])

Units Sold = SUM(retail_sales[Quantity])

Average Order Value = DIVIDE([Total Sales], [Total Orders])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Total Cost = SUM(retail_sales[Cost])
```

## Visuals to create
1. **Card:** Total Sales
2. **Card:** Total Profit
3. **Card:** Total Orders
4. **Card:** Units Sold
5. **Line chart:** Axis = OrderDate (Month); Values = Total Sales
6. **Clustered bar chart:** Axis = Category; Values = Total Sales
7. **Bar chart:** Axis = ProductName; Values = Total Sales; sort descending; Top N 10
8. **Map or bar chart:** Axis = City; Values = Total Sales
9. **Donut chart:** Legend = OrderStatus; Values = Total Orders
10. **Slicer:** OrderDate
11. **Slicer:** Category
12. **Slicer:** City

## Formatting
- Title: `Retail Sales Dashboard`
- Use consistent number formats (currency for sales/profit).
- Turn on data labels for key charts.
- Add a subtitle: `Sales Performance | Product Insights | Order Trends`.
- Save as `analysis/Retail_Sales_Dashboard.pbix`.

## Interview-ready summary
“Analyzed retail transaction data using MySQL and Power BI. Wrote SQL queries to evaluate sales, profit, product categories, monthly trends, cities, and order statuses. Designed an interactive dashboard with KPI cards, trend charts, and slicers to communicate business insights.”
