# 182. Duplicate Emails

## Problem

https://leetcode.com/problems/duplicate-emails/

## Solution

```sql
SELECT email
FROM Person
GROUP BY email
HAVING COUNT(*) > 1;
```

## Explanation

### Idea

The **Person** table contains email addresses.

We group the rows by **email** and then find the emails that appear more than once.

### Keywords to Remember

- **SELECT email** → Display the duplicate email.
- **FROM Person** → Read data from the `Person` table.
- **GROUP BY email** → Group same emails together.
- **HAVING** → Filter grouped data.
- **COUNT(*) > 1** → Keep only emails that appear more than once.

### One-line Logic

Group people by email and return only those emails whose count is greater than 1.
