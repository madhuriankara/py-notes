---
title: Count-Occupation
date: 2025-01-15
author: Your Name
cell_count: 8
score: 5
---

```python
#Count the number of individuals with "Post Graduate" qualifications.

```


```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE food AS SELECT * FROM 'updatedonline_file.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x106cef770>




```python
result = con.execute(""" SELECT COUNT(Occupation) FROM food """).fetchall()
```


```python
result
```




    [(388,)]




```python

```


---
**Score: 5**
