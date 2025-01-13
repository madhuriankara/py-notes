---
title: Car-With-Highest-Compression
date: 2025-01-13
author: Your Name
cell_count: 7
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x104f395b0>




```python
#Find the car with the highest compression-ratio for each fuel-type.
```


```python
result = con.execute("""SELECT MAX("compression-ratio"), "fuel-type"
                            FROM automobile
                            GROUP BY "fuel-type"
                            """).fetchall()
```


```python
result
```




    [(23.0, 'diesel'), (11.5, 'gas')]




```python

```


---
**Score: 5**
