---
title: Family-Size-Max
date: 2025-01-13
author: Your Name
cell_count: 11
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
con.execute("CREATE TABLE food AS SELECT * FROM 'updatedonline_file.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x105ae9070>




```python
#What is the maximum family size recorded in the dataset?
```


```python
result = con.execute("""SELECT MAX("Family-size") FROM food """).fetchall()
```


```python
result
```




    [(6,)]




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
