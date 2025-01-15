---
title: City-Max-Min-Mpg
date: 2025-01-15
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
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x109af7770>




```python
#Identify the minimum and maximum city-mpg
```


```python
result = con.execute("""SELECT MIN("city-mpg"),MAX("city-mpg") FROM automobile""").fetchall()
```


```python
result
```




    [(13, 49)]




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
