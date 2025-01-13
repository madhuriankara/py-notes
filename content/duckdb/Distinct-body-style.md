---
title: Distinct-Body-Style
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




    <duckdb.duckdb.DuckDBPyConnection at 0x103747c70>




```python
#Group by make and count the number of unique body-style values.
```


```python
result = con.execute("""SELECT make,COUNT(DISTINCT "body-style") AS unique_body_style
                       FROM automobile
                       GROUP BY make""").fetchall()
```


```python
result
```




    [('nissan', 4),
     ('mitsubishi', 2),
     ('audi', 3),
     ('peugot', 2),
     ('saab', 2),
     ('mercedes-benz', 4),
     ('volkswagen', 4),
     ('subaru', 3),
     ('mercury', 1),
     ('jaguar', 1),
     ('porsche', 3),
     ('renault', 2),
     ('chevrolet', 2),
     ('dodge', 3),
     ('honda', 3),
     ('volvo', 2),
     ('alfa-romero', 2),
     ('isuzu', 2),
     ('mazda', 2),
     ('toyota', 5),
     ('bmw', 1),
     ('plymouth', 3)]




```python

```


---
**Score: 5**
