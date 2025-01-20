---
title: Top-3-Body-Style
date: 2025-01-20
author: Your Name
cell_count: 7
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x105c8fe30>




```python
#Identify the top 3 body-style categories with the highest average price.
```


```python
result = con.execute("""SELECT "body-style",AVG(CAST(price AS FLOAT)) AS avg_price
                     FROM automobile
                     WHERE price != '?'
                     GROUP BY "body-style"
                     ORDER BY avg_price DESC
                     LIMIT 3;""").fetchall()
```


```python
result
```




    [('hardtop', 22208.5), ('convertible', 21890.5), ('sedan', 14459.755319148937)]




```python

```


---
**Score: 5**
