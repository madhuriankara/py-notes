---
title: Gender-Distinct
date: 2025-01-06
author: Your Name
cell_count: 6
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE food AS SELECT * FROM 'onlinefoods.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x10ac935b0>




```python
result = con.execute("""SELECT DISTINCT(Gender) FROM food 
                         """).fetchall()
```


```python
result
```




    [('Female',), ('Male',)]




```python

```


---
**Score: 5**
