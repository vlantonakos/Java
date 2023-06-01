In this query:
    The customers table is aliased as c to make the query more readable.
    The LEFT JOIN combines the customers and payments tables based on the customer_id column. This will retrieve all customers, including those who have not made any payments.
    The WHERE clause filters the result based on two conditions:
        p.customer_id IS NULL: This condition ensures that customers who have no corresponding payment records are included in the result. This means customers who have not made any payments at all.
        p.payment_date < DATE_SUB(CURDATE(), INTERVAL 3 MONTH): This condition checks if the payment date is older than the current date minus 3 months. It ensures that customers who have made payments but not in the last 3 months are also included in the result.
By combining these conditions in the WHERE clause, the query will output a list of customers who have not paid their bills in the last 3 months.
```
SELECT c.*
FROM customers c
LEFT JOIN payments p ON c.customer_id = p.customer_id
WHERE p.customer_id IS NULL OR p.payment_date < DATE_SUB(CURDATE(), INTERVAL 3 MONTH);
```
