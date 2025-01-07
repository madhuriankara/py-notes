---
title: Drive-Wheels-Category
date: 2025-01-06
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1237fb030>




```python
#Find the number of cars for each drive-wheels category.
```


```python
result = con.execute("""SELECT "drive-wheels",make, COUNT(*) AS number_cars FROM automobile
                         GROUP BY make, "drive-wheels" """).fetchall()
                        
```


```python
result
```




    [('4wd', 'audi', 2),
     ('fwd', 'dodge', 9),
     ('fwd', 'mazda', 11),
     ('rwd', 'mazda', 6),
     ('fwd', 'mitsubishi', 13),
     ('rwd', 'porsche', 5),
     ('fwd', 'renault', 2),
     ('fwd', 'volkswagen', 12),
     ('rwd', 'bmw', 8),
     ('rwd', 'mercury', 1),
     ('fwd', 'nissan', 15),
     ('rwd', 'nissan', 3),
     ('fwd', 'plymouth', 6),
     ('rwd', 'plymouth', 1),
     ('rwd', 'volvo', 11),
     ('rwd', 'isuzu', 2),
     ('fwd', 'isuzu', 2),
     ('rwd', 'jaguar', 3),
     ('fwd', 'honda', 13),
     ('fwd', 'subaru', 7),
     ('fwd', 'toyota', 16),
     ('rwd', 'toyota', 14),
     ('rwd', 'alfa-romero', 3),
     ('rwd', 'mercedes-benz', 8),
     ('4wd', 'subaru', 5),
     ('4wd', 'toyota', 2),
     ('fwd', 'audi', 5),
     ('fwd', 'chevrolet', 3),
     ('rwd', 'peugot', 11),
     ('fwd', 'saab', 6)]




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
