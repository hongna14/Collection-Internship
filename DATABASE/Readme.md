# DATABASE
## What is databse
 Database is an organized collection of data and information or interrelated data collected at one place. Easy to update data, Security of data, Data integrity, Easy to research data.
## What is relation database
 A relational database organizes data into rows and columns, which collectively form a table. Data is typically structured across multiple tables, which can be joined together via a primary key or a foreign key.
## What is Structured Query Language (SQL)
 Invented by Don Chamberlin and Ray Boyce at IBM, Structured Query Language (SQL) is the standard programming language for interacting with relational database management systems, allowing database administrator to add, update, or delete rows of data easily.
## Practicing
*1. Product list in a month*
```sql
SELECT 
	orders.order_date,
	product.product_name,
	EXTRACT (MONTH FROM orders.order_date) AS Month
FROM orders
INNER JOIN product ON product.product_id = orders.product_id
WHERE EXTRACT (MONTH FROM orders.order_date) =1;
```
*2. Orders quantities in a month*
```sql
SELECT 
	SUM(payment.payment_amount) AS sumAmount,
	product.product_name AS productName,
	product.product_id,
	COUNT(orders.order_id)
FROM orders
RIGHT JOIN product ON product.product_id = orders.product_id
LEFT JOIN payment ON payment.payment_id= orders.payment_id
GROUP BY product.product_id, product.product_name;
```
*3. Top 1 product in a month*
```sql
SELECT 
	product.product_name,
	orders.product_id,
	SUM(orders.order_quantity) as sumQuantity
FROM orders
INNER JOIN product ON product.product_id = orders.product_id
WHERE EXTRACT (MONTH FROM orders.order_date) =1
GROUP BY orders.product_id,product.product_name
ORDER BY SUM(orders.order_quantity) DESC
LIMIT 1;
```