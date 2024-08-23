# COFFEE-SALES-DASHBOARD-EXCEL-PROJECT
Coffee Sales
Overview
This project features a comprehensive Coffee Sales Dashboard created in Excel. The dashboard provides valuable insights into the 2019-2022 sales performance of a coffee shop, helping to identify trends, patterns, and areas for improvement.

The Coffee Sales Dashboard provides a detailed analysis of coffee sales data, helping businesses understand their sales performance over time, identify top customers, and analyze product preferences. This project uses Excel functions like XLOOKUP, INDEX, and MATCH to gather and analyze data, along with IF statements for data simplification.

Data Description
The dataset includes the following columns in the Orders sheet:

-Order ID: Unique identifier for each order.

-Order Date: The date the order was placed.

-Customer ID: Unique identifier for each customer.

-Product ID: Unique identifier for each product.

-Quantity: The number of units sold.

-Customer Name: The name of the customer.

-Email: The email address of the customer.

-Country: The country where the order was placed (created using XLOOKUP from the Customers sheet).

-Coffee Type: The type of coffee product sold.

-Roast Type: The roast type of the coffee.

-Size: The size of the coffee product.

-Unit Price: The price per unit of each product.

-Sales: The total revenue generated from each sale (calculated as Quantity x Unit Price).

-Coffee Type Name: Name of the coffee type (created using IF function).

-Roast Type Name: Name of the roast type (created using IF function).

-Loyalty Card: Indicates whether the customer has a loyalty card (created using XLOOKUP from the Customers sheet).

Dashboard Features
The Excel dashboard provides:

-Sales Trends: Visualization of sales over time to identify peaks and troughs.

-Product Performance: Analysis of the sales performance of different coffee products.

-Revenue Breakdown: Detailed breakdown of total sales revenue by product and country.

-Customer Insights: Understanding of sales patterns by customer type and loyalty card holders.

-Top Products: Identification of top-selling products and their contribution to total sales.

Usage
To use the dashboard:

-Open the Excel file provided in this repository.

-Navigate through the different sheets to explore various aspects of the data.

-Use filters and pivot tables to customize the view according to your interest.

Snapshot of Dashboard (Excel)
coffee_sales_dashboard_2019_2022
![Screenshot (8)](https://github.com/user-attachments/assets/358ada95-53ba-4de4-aa3b-a3a562996618)


Steps followed
1. Data Exploration and Initial Setup
Step 1: Check the Data
Open the Excel file and examine the three different sheets available: Orders, Customers, and Products. Identify the key information and how it is distributed across these sheets.

2. Data Gathering and Preparation
Step 2: Gather Customer Data
-Use the XLOOKUP function to create the Customer Name column in the Orders sheet.

=XLOOKUP([@Customer ID], Customers!A:A, Customers!B:B)

-Apply the same XLOOKUP function to create the Email, Country, and Loyalty Card columns.

=XLOOKUP([@Customer ID], Customers!A:A, Customers!C:C) ' For Email

=XLOOKUP([@Customer ID], Customers!A:A, Customers!G:G) ' For Country

=XLOOKUP([@Customer ID], Customers!A:A, Customers!I:I) ' For Loyalty Card

Step 3: Gather Product Data
-Use the INDEX MATCH functions to create the Coffee Type, Roast Type, Size, and Unit Price columns in the Orders sheet.

Step 4: Calculate Sales
Create the Sales column by multiplying the Quantity and Unit Price.

Step 5: Simplify Coffee Type and Roast Type Names
Use the IF function to create readable names for Coffee Type Name and Roast Type Name columns.

Here is the formula;
=IF([@Coffee Type]="Rob","Robusta",IF([@Coffee Type]="Exc","Excelsa",IF([@Coffee Type]="Ara","Arabica",IF([@Coffee Type]="Lib","Liberica",""))))

3. Creating the Dashboard
Step 6: Design the Dashboard Layout
Plan the layout of your dashboard, deciding which charts and tables will best display your insights.

Step 7: Create Pivot Tables and Charts
-Use pivot tables to summarize the data by various dimensions such as date, roast type, and top 5 customers.

-Create charts to visualize trends, product performance, revenue breakdown, and customer insights.

Step 8: Integrate Pivot Tables and Charts into the Dashboard
-Arrange the pivot tables and charts on a new sheet designated as the dashboard.

-Ensure the dashboard is interactive, using slicers and filters to allow users to explore the data dynamically.

Step 9: Format and Finalize the Dashboard
-Apply consistent formatting to ensure the dashboard is visually appealing and easy to read.

-Add titles, labels, and legends to charts for clarity.

Step 10: Review and Test the Dashboard
-Verify the accuracy of the data and the functionality of the dashboard.

-Test the dashboard to ensure all interactions work as expected.
