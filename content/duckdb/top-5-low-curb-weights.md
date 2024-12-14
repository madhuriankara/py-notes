---
title: Top-5-Low-Curb-Weights
date: 2024-12-13
author: Your Name
cell_count: 12
score: 10
---

```python
#!pip install duckdb
```


```python
import duckdb
```


```python
# Connect to DuckDB
con = duckdb.connect()

```


```python
# Load CSV file
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x106461270>




```python
#Find cars with the top 5 lowest curb-weight
```


```python
result = con.execute("""SELECT "curb-weight" FROM automobile
                       ORDER BY  "curb-weight" ASC LIMIT 5 """).fetchall()
                        
```


```python
result
                        
```




    [(1488,), (1713,), (1819,), (1837,), (1874,)]




```python

```


```python


```


```python

```


```python

```


```python

```


---
**Score: 10**
