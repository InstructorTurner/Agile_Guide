# 🍳 SQL Recipes (Advanced)

This guide provides common complex query patterns for everyday development.

## 📄 Pagination
Use `LIMIT` and `OFFSET` for paginating results.
```sql
-- Page 1 (10 results)
SELECT * FROM orders 
ORDER BY created_at DESC 
LIMIT 10 OFFSET 0;

-- Page 2 (10 results)
SELECT * FROM orders 
ORDER BY created_at DESC 
LIMIT 10 OFFSET 10;
```

## 🔍 Inner Selects & Subqueries
### Subquery in WHERE clause
Find users who have placed at least one order:
```sql
SELECT username FROM users 
WHERE id IN (SELECT user_id FROM orders);
```

### Correlated Subquery
Find users whose order total is above the average:
```sql
SELECT username FROM users u 
WHERE (SELECT SUM(total) FROM orders o WHERE o.user_id = u.id) > 100;
```

## 🤝 Joins Cheat Sheet
| Join Type | Result | Use Case |
| :--- | :--- | :--- |
| **INNER JOIN** | Only matching rows in both | Get orders with their customer info |
| **LEFT JOIN** | All from left, matches from right | Get all users, including those with no orders |
| **RIGHT JOIN** | All from right, matches from left | Get all orders, including those without users |
| **FULL JOIN** | All rows from both | Comprehensive union of two tables |

### Example: Complex Join
```sql
SELECT u.username, o.order_date, p.product_name
FROM users u
INNER JOIN orders o ON u.id = o.user_id
INNER JOIN order_items oi ON o.id = oi.order_id
INNER JOIN products p ON oi.product_id = p.id
WHERE p.category = 'Electronics';
```

## 📈 Aggregations
```sql
-- Count orders per user
SELECT user_id, COUNT(*) as total_orders 
FROM orders 
GROUP BY user_id 
HAVING COUNT(*) > 5;
```
