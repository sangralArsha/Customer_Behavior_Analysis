🛍️ Customer Behaviour Analysis – E-Commerce Dataset
📊 Project Overview

This project analyzes customer purchasing behaviour in an online retail environment to understand sales trends, customer loyalty, and segment users based on buying patterns.
Using SQL for analysis and Power BI for visualization, the project identifies which product categories drive revenue, which cities have the most engaged customers, and how loyal different customer groups are using RFM (Recency–Frequency–Monetary) segmentation.

🎯 Objectives

Understand overall sales performance and key drivers.

Identify repeat customers and assess customer loyalty.

Perform RFM analysis to segment customers based on behaviour.

Visualize insights through interactive Power BI dashboards.

Translate data findings into actionable business recommendations.

🧩 Steps Followed
Step 1 – Load and Understand the Data

Dataset: customer_orders_10000.csv (10,000 transactions).

Columns include: OrderID, CustomerID, Gender, Age, City, Product, Category, OrderDate, Quantity, UnitPrice, TotalAmount.

Each row represents a single customer purchase.

Step 2 – Data Cleaning

Ensured no duplicates or missing data.

Verified TotalAmount = Quantity * UnitPrice.

Converted OrderDate to date format.

Step 3 – Exploratory Data Analysis (SQL)

Example Queries:

-- Total revenue by category
SELECT Category, SUM(TotalAmount) AS TotalSales
FROM Customer_Orders
GROUP BY Category;

-- Revenue by city
SELECT City, SUM(TotalAmount) AS TotalSales
FROM Customer_Orders
GROUP BY City
ORDER BY TotalSales DESC;

-- Repeat customers
SELECT CustomerID, COUNT(OrderID) AS NumOrders
FROM Customer_Orders
GROUP BY CustomerID
HAVING COUNT(OrderID) > 1;

Step 4 – Behaviour Segmentation (RFM Analysis)

Calculated Recency, Frequency, and Monetary values for each customer:

![Customer_Behavior_Analysis](https://github.com/sangralArsha/Customer_Behavior_Analysis/blob/main/RFM_sqlquery.png)


Segmented customers into groups:
Best Customers, Potential Loyalists, At-Risk, and Lost Customers.

Step 5 – Visualization (Power BI)

Created an interactive Power BI dashboard ![Customer_Behavior_Analysis](https://github.com/sangralArsha/Customer_Behavior_Analysis/blob/main/customer_Behaviour_Dashboard.png)
including:

KPI Cards (Total Revenue, Total Customers, Repeat Rate)

Bar Chart: Sales by Category

Bar Chart: Sales by City

Scatter Plot: RFM segmentation

Pie Charts: Revenue and Repeat Rate by Gender

Table: Top 10 Customers by Spending

Line Chart: Sales Trend over Time

Step 6 – Insights & Storytelling

💰 Electronics dominates with ~50% of total revenue.

📍 Toronto and Ottawa are top-performing cities.

👥 99% repeat rate — strong customer retention.

🛒 Top 10 customers contribute only ~2.4% of revenue → diversified customer base.

💡 Recommendation: Focus on cross-selling between Beauty & Electronics and retention campaigns for “At-Risk” customers.

Step 7 – Final Deliverable

Deliverables include:

Power BI dashboard (Customer_Behaviour_Analysis.pbix)

SQL script (Customer_Behaviour_Analysis.sql)

Dataset (customer_orders_10000.csv)

PDF summary report

🧠 Skills Demonstrated

Data Cleaning & Transformation (SQL, Power Query)

Exploratory Data An
