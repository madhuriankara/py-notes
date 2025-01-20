---
title: Average-Engine-Size
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




    <duckdb.duckdb.DuckDBPyConnection at 0x10392b8b0>




```python
#Group the data by fuel-type and calculate the average engine-size.
```


```python
result = con.execute("""SELECT 'fuel-type', AVG("engine-size") FROM automobile 
                        GROUP BY 'fuel-type' """).fetchall()
```


```python
result
```




    [('fuel-type', 126.90731707317073)]




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
