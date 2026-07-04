# 175. Combine Two Tables

## Problem

https://leetcode.com/problems/combine-two-tables/

## Solution

```sql
SELECT firstName, lastName, city, state
FROM Person
LEFT JOIN Address
ON Person.personId = Address.personId;
```

## Explanation

### Idea

The **Person** table contains the person's name, while the **Address** table contains their city and state.

We use a **LEFT JOIN** to combine both tables based on the **personId** so that **every person is included**, even if they don't have an address.

### Keywords to Remember

- **SELECT** → Choose the columns to display.
- **FROM Person** → Read data from the `Person` table.
- **LEFT JOIN Address** → Include all rows from the `Person` table and matching rows from the `Address` table.
- **ON Person.personId = Address.personId** → Join the tables where the `personId` values are equal.

### One-line Logic

Return every person's first name, last name, city, and state by joining the `Person` and `Address` tables using `personId`.
