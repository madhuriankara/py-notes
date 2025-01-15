---
title: Engine-Location-Rear
date: 2025-01-15
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




    <duckdb.duckdb.DuckDBPyConnection at 0x11843db30>




```python
#Filter rows where the engine-location is rear.
```


```python
result = con.execute("""SELECT * FROM automobile
                        WHERE "engine-location" IN ('rear') """).fetchall()
                        
```


```python
result = con.execute("""SELECT make,"engine-location" FROM automobile
                        WHERE "engine-location" IN ('rear') """).fetchall()
                        
```


```python
result
```




    [('porsche', 'rear'), ('porsche', 'rear'), ('porsche', 'rear')]




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
