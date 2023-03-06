# 234

SELECT
order_items.id,
customers.first_name,
company_orders.date,
company_orders.total_amount
FROM order_items
LEFT JOIN
company_orders ON
company_orders.id=order_items.order_id
LEFT JOIN
customers ON
customers.id=company_orders.customer_id
