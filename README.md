# Project Title: Sales Performance Analysis with Power BI

## 📌 Project Overview

This Power BI report analyzes **Mavin Toy's sales performance**, highlighting revenue trends, product performance, and store location insights for data-driven decision-making.

## Dataset
- **Source:** A total of four datasets were used the "Sales.csv", "Stores.csv", "Calendar.csv", "Products.csv" from

## 🚀 Objectives

- Using Power BI connect to the Sales, Stores, Products, and Calendar csv files through Transform Data > New Source > Text/CSV 
- Review table columns, check for blank or null values, confirm that datatypes are accurately defined, and identify any primary and foreign keys
- Add calculated columns in the calendar table for ‘start of month’ and ‘start of week’
- Load the tables to the data model and create relationships from the sales table to the products, stores, and calendar tables
- Your model should take the form of a star schema, with 1:many relationships between fact and dimension tables
- Create a date hierarchy containing the ‘start of month’, ‘start of week’, and ‘date’ fields
- Create calculated columns in the sales table to pull in ‘cost’ and ‘price’ from the products table, then use those fields to calculate revenue and profit for each transaction
- Create measures to calculate the count of orders (‘total orders’), sum of revenue (‘total revenue’) and sum of profit (‘total profit’)
- Add KPI card visuals showing ‘total orders’, ‘total revenue’ and ‘total profit’ for the current month, along with monthly trends for each metric
- Add a slicer to filter the report page by store location and a bar chart showing ‘total orders’ by product category, and a line chart showing ‘total revenue’ with the date hierarchy on the x-axis
- Assemble the charts into a logical layout and adjust formatting, alignment and polish to finalize the report as you see fit

## DAX Function
Here are some DAX function or calculated columns that were used
1. Revenue = sales[Price] * sales[Units] 
2. Profit = sales[Revenue] - (sales[Cost] * sales[Units])
3. Total Order = DISTINCTCOUNT(sales[Sale_ID])
4. Total Profit = SUM(sales[Profit])

## 📊 Key Insights

- **Total Orders:** **41,830** orders recorded.
- **Revenue Performance:** **₦658,194** in total revenue, with peaks observed in early and late months of each year.
- **Profitability:** **₦180,445** total profit, indicating a moderate margin.
- **Top-Selling Product Categories:**
  - **Toys** (221,227 orders) and **Art & Crafts** (220,673 orders) lead in sales volume.
  - **Electronics** had the lowest orders (99,025), suggesting lower demand.
- **Revenue Trends:**
  - Sales experience periodic spikes, likely influenced by seasonal demand.
  - Highest revenue months align with peak shopping seasons (holidays and promotions).

## Recommendations

- **Inventory Optimization:** Ensure high stock availability for Toys and Art & Crafts, as they contribute the most sales.
- **Marketing Focus:** Increase promotional efforts for low-performing categories like Electronics.
- **Profit Maximization:** Investigate pricing strategies to improve profit margins despite high revenue.
- **Seasonal Campaigns:** Leverage peak sales months for targeted marketing and discount campaigns.



