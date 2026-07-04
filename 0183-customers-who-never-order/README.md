# 183. Customers Who Never Order

## Problem

https://leetcode.com/problems/customers-who-never-order/

## Solution

```sql
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (
    SELECT customerId
    FROM Orders
);
```

## Explanation

### Idea

The **Orders** table contains the IDs of customers who have placed orders.

We first get those customer IDs using a **subquery**.

Then we select customers from the **Customers** table whose **id** is **not** in that list.

### Keywords to Remember

- **SELECT** → Choose the column to display (`name`).
- **AS Customers** → Rename the output column to **Customers**.
- **FROM Customers** → Read data from the **Customers** table.
- **WHERE** → Filter the rows.
- **NOT IN** → Exclude values present in another list.
- **Subquery (`SELECT customerId FROM Orders`)** → Returns the IDs of customers who have placed orders.

### One-line Logic

Find all customers whose **id** is **not present** in the `Orders.customerId` column because those customers never placed an order.
