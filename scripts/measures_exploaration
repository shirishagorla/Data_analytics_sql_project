/*
===============================================================================
Measures Exploration (Key Metrics)
===============================================================================
Purpose:
    - To calculate aggregated metrics (e.g., totals, averages) for quick insights.
    - To identify overall trends or spot anomalies.

SQL Functions Used:
    - COUNT(), SUM(), AVG() */
===============================================================================
/*find the totalsales*/
select sum(sales_amount) from gold_fact_sales;
/*find how many items sold*/
select sum(quantity) from gold_fact_sales;
/*avg selling price*/
select avg(price) from gold_fact_sales;
/*find the no of orders*/
select count(order_number) from gold_fact_sales;
/*find the total no of products*/
select count(product_key) from gold_dim_products;
/*find the total no of customers*/
select count(customer_key) from gold_dim_customers;
/*find the total nu of customers who has placed orders*/
select count(distinct(customer_key)) from gold_fact_sales;

-- Generate a Report that shows all key metrics of the business
SELECT 'Total Sales' AS measure_name, SUM(sales_amount) AS measure_value FROM gold_fact_sales
UNION ALL
SELECT 'Total Quantity', SUM(quantity) FROM gold_fact_sales
UNION ALL
SELECT 'Average Price', AVG(price) FROM gold_fact_sales
UNION ALL
SELECT 'Total Orders', COUNT(DISTINCT order_number) FROM gold_fact_sales
UNION ALL
SELECT 'Total Products', COUNT(DISTINCT product_name) FROM gold_dim_products
UNION ALL
SELECT 'Total Customers', COUNT(customer_key) FROM gold_dim_customers;
