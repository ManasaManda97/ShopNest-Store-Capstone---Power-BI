# ShopNest-Store-Capstone---Power-BI
1. Introduction:
The ShopNest Store Power BI Capstone project focuses on analyzing e-commerce sales, delivery performance, customer behaviour, and revenue trends using multiple datasets. The objective of this project is to design an interactive Power BI dashboard that provides meaningful business insights through effective data modeling, DAX calculations, and visual analytics.
The dashboard integrates sales, orders, customers, reviews, payments, and time-based data to support data-driven decision making for ShopNest Store.


2. Data Overview
The project utilises multiple  datasets, using star-schema approach with orders items table as centre table.
    • Orders
    • Order Items
    • Customers
    • Sellers
    • Payments
    • Order Reviews
    • Products
    • Product Category Translation
    • Date Table (created using DAX)

3. DAX Measures:
 I have created certain Measures to achieve the required solutions.
    • **Delayed Orders**  at order items level.
    • **Total Sales** at order items level.
    • **Payment Count** at order Payement level.
    • **Average rating** at order review level
    • **on time orders** and **total orders** at order level

 **  Task 1: Top Categories by Revenue**
 
    Identified and visually represented the top 10 product categories by total sales.
    A new measure named Total Sales was created in the Order Items table using the following DAX formula:
    Total Sales = SUM(Nexusgoods_order_items_Lookup[Price])

 **   Task 2. Delayed Orders Analysis **
 
    Determine the number of delayed orders in each category. 
    A calculated column was created to determine delivery delay:
    Delivery Delay = IF(Orders[Actual Delivery Date] > Orders[Estimated Delivery Date], "Delayed", "On Time")

**
    Task 3: Monthly Comparison of Delayed and On-Time Orders**
    
  Compared delayed orders with on-time orders on a monthly basis using drill through analysis. 

**
  Task 4: Payment Method Analysis **
  
 Analysed the most frequently used payment methods by customers. 
