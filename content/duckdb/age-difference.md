---
title: Age-Difference
date: 2025-01-22
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




    <duckdb.duckdb.DuckDBPyConnection at 0x104dcb8b0>




```python
#What is the minimum age of individuals in the dataset?
```


```python
result = con.execute("""SELECT Min(Age) FROM food """).fetchall()
```


```python
result
```




    [(18,)]




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
