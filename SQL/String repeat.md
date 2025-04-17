Write a function that accepts a non-negative integer n and a string s as parameters, and returns a string of s repeated exactly n times.
Examples (input -> output)

```text
6, "I"     -> "IIIIII"
5, "Hello" -> "HelloHelloHelloHelloHello"
```

---

```sql
--# write your SQL statement here: you are given a table 'repeatstr' with columns 'n' and 's', return a table with all columns and your result in a column named 'res'.
SELECT s, n, repeat(s, n) AS res FROM repeatstr;
```
