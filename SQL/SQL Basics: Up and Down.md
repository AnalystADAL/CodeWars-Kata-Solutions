Given a table of random numbers as follows:
numbers table schema

- id
- number1
- number2

Your job is to return table with similar structure and headings, where if the sum of a column is odd, the column shows the minimum value for that column, and when the sum is even, it shows the max value. You must use a case statement.
output table schema

- number1
- number2

Fundamentals,
SQL

```sql
SELECT

  CASE 
      WHEN SUM(number1) % 2 = 1 THEN MIN(number1)   -- %: The modulo operator
      WHEN SUM(number1) % 2 = 0 THEN MAX(number1)   -- Used mod 2 to find odd/even
END AS number1,

  CASE 
      WHEN SUM(number2) % 2 = 1 THEN MIN(number2)   -- If sum is  odd, take MIN
      WHEN SUM(number2) % 2 = 0 THEN MAX(number2)   -- If sum is even, take MAX
END AS number2

FROM numbers


-- Some CASEs WHEN even for this solution THEN sometimes solutions can be odd...
```
