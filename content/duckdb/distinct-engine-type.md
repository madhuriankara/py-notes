---
title: Distinct-Engine-Type
date: 2025-01-20
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




    <duckdb.duckdb.DuckDBPyConnection at 0x10728e2f0>




```python
#Count the number of unique values in the engine-type column.
```


```python
result = con.execute("""SELECT DISTINCT("engine-type") FROM automobile LIMIT 10""").fetchall()
```


```python
result
```




    [('ohc',), ('rotor',), ('ohcv',), ('l',), ('ohcf',), ('dohc',), ('dohcv',)]




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
