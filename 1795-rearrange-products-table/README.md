# 1795. Rearrange Products Table

## Problem

https://leetcode.com/problems/rearrange-products-table/

## Solution

```sql
SELECT product_id, 'store1' AS store, store1 AS price
FROM Products
WHERE store1 IS NOT NULL

UNION

SELECT product_id, 'store2' AS store, store2 AS price
FROM Products
WHERE store2 IS NOT NULL

UNION

SELECT product_id, 'store3' AS store, store3 AS price
FROM Products
WHERE store3 IS NOT NULL;
```

## Explanation

### Idea

The **Products** table stores prices for different stores in separate columns (`store1`, `store2`, `store3`).

We convert these columns into rows by selecting each store separately and then combine the results using **UNION**.

### Keywords to Remember

- **SELECT** → Choose the required columns.
- **'store1' AS store** → Create a new column named `store` with the value `"store1"`.
- **store1 AS price** → Rename the `store1` column as `price`.
- **WHERE store1 IS NOT NULL** → Exclude products that are not available in `store1`.
- **UNION** → Combine the results of multiple `SELECT` statements into one table while removing duplicates.

### One-line Logic

Convert each store column into rows and combine them into a single table containing `product_id`, `store`, and `price`.
