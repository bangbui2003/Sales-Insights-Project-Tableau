<h1 align="center">Sales Insights - Data Analysis using Tableau & SQL</h1>

### About Project 👨‍💻
What i have done:

- Performed India based hardware company sales insights.

- Created ETL mappings using SQL to extract unstructured data and transformed it for staging, performing data cleaning and structuring it into a star schema design for Tableau.

- Designed a Tableau dashboard to conduct analysis, producing quantitative visualizations that revealed valuable insights into the factors impacting company performance year over year, leading to business solution recommendations..

## Technologies used ⚙️

* MySQL

* Tableau

## Project - India based Hardware company Sales Insights - Data Analysis performed on Tableau & SQL

### Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 Products by revenue.
  
- Q5. Net Profit & Profit Margin by Market
    
## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`


## Data Analysis Using Tableau 



  
