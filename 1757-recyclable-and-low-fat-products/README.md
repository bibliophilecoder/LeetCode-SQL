# 1757. Recyclable and Low Fat Products

## Problem

https://leetcode.com/problems/recyclable-and-low-fat-products/

---

## Solution

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
AND recyclable = 'Y';
```

---

## Explanation

- **SELECT** → Returns `product_id`.
- **FROM** → Reads from the `Products` table.
- **WHERE** → Filters rows.
- **AND** → Both conditions must be true.

### Logic

Return products that are both low-fat and recyclable.
