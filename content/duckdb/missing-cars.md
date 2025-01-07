---
title: Missing-Cars
date: 2025-01-06
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1067b4930>




```python
#Count the total number of cars with missing values in any column.
```


```python
result = con.execute("""SELECT COUNT(*) FROM automobile
                       WHERE make IS  NULL """).fetchall()
                        
```


```python
result
                        
```




    [(0,)]




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
