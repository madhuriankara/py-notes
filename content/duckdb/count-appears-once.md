---
title: Count-Appears-Once
date: 2025-01-03
author: Your Name
cell_count: 9
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1071919b0>




```python
#Find all cars where the make appears only once in the dataset.
```


```python
result = con.execute("""
    SELECT *
    FROM automobile
    WHERE make IN (
        SELECT make
        FROM automobile
        GROUP BY make
        HAVING COUNT(*) = 1
    )
""").fetchall()
```


```python
result
```




    [(1,
      '?',
      'mercury',
      'gas',
      'turbo',
      'two',
      'hatchback',
      'rwd',
      'front',
      102.7,
      178.4,
      68.0,
      54.8,
      2910,
      'ohc',
      'four',
      140,
      'mpfi',
      '3.78',
      '3.12',
      8.0,
      '175',
      '5000',
      19,
      24,
      '16503')]




```python

```


```python

```


```python

```


---
**Score: 5**
