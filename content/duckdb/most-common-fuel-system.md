---
title: Most-Common-Fuel-System
date: 2024-12-15
author: Your Name
cell_count: 9
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




    <duckdb.duckdb.DuckDBPyConnection at 0x106725db0>




```python
#Find the most common value in the fuel-system column.
```


```python
result = con.execute("""SELECT  "fuel-system", COUNT(*) AS count
                     FROM automobile
                     GROUP BY "fuel-system"
                     ORDER BY count DESC
                     LIMIT 1
                     """).fetchall()
```


```python
result
```




    [('mpfi', 94)]




```python

```


```python

```


```python

```


---
**Score: 5**
