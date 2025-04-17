Write a function that returns the total surface area and volume of a box.

The given input will be three positive non-zero integers: width, height, and depth.

The output will be language dependant, so please check sample tests for the corresponding data type, (list, tuple, struct, query, et cetera).

---

```sql
-- # write your SQL statement here: 
-- you are given a table 'box' with columns: width (int), height (int), depth (int)
-- return a query with columns: width, height, depth, area (int), volume (int)
-- sort results by area ascending, then volume ascending, then width ascending, then height ascending

SELECT 
  *,
  2 * (width * height + height * depth + width * depth) AS area,
  width * height * depth AS volume
FROM box
ORDER BY area, volume, width, height ASC;
```
