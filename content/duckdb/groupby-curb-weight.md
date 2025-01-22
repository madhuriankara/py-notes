---
title: Groupby-Curb-Weight
date: 2025-01-22
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




    <duckdb.duckdb.DuckDBPyConnection at 0x106062330>




```python
#Group the cars by body-style and calculate the sum of curb-weight for each group.
```


```python
result = con.execute("""SELECT "body-style", SUM("curb-weight") AS curb
                            FROM automobile
                            GROUP BY "body-style"
                            """).fetchall()
```


```python
result
```




    [('sedan', 250617),
     ('hardtop', 22485),
     ('hatchback', 164373),
     ('convertible', 16810),
     ('wagon', 69606)]




```python

```


---
**Score: 5**
