---
title: Compression-Ratio-10
date: 2025-01-03
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1063d1370>




```python
#Filter cars with a compression-ratio above 10
```


```python
result = con.execute("""SELECT make,"compression-ratio" FROM automobile
                        WHERE CAST("compression-ratio" AS INT) > 10 """).fetchall()
                        
```


```python
result
```




    [('jaguar', 11.5),
     ('mazda', 22.7),
     ('mazda', 22.0),
     ('mercedes-benz', 21.5),
     ('mercedes-benz', 21.5),
     ('mercedes-benz', 21.5),
     ('mercedes-benz', 21.5),
     ('nissan', 21.9),
     ('peugot', 21.0),
     ('peugot', 21.0),
     ('peugot', 21.0),
     ('peugot', 21.0),
     ('peugot', 21.0),
     ('toyota', 22.5),
     ('toyota', 22.5),
     ('toyota', 22.5),
     ('volkswagen', 23.0),
     ('volkswagen', 23.0),
     ('volkswagen', 23.0),
     ('volkswagen', 23.0),
     ('volvo', 23.0)]




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
