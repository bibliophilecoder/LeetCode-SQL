# 627. Swap Salary

## Problem

https://leetcode.com/problems/swap-salary/

## Solution

```sql
UPDATE Salary
SET sex = IF(sex = 'm', 'f', 'm');
```

## Explanation

- **UPDATE Salary** → Updates the `Salary` table.
- **SET sex =** → Modifies the `sex` column.
- **IF(condition, true_value, false_value)** → MySQL's if-else function.
- If `sex = 'm'`, change it to `'f'`; otherwise, change it to `'m'`.

## Logic

Swap all `'m'` values with `'f'` and vice versa in a single query.
