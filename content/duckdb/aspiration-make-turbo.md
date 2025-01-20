---
title: Aspiration-Make-Turbo
date: 2025-01-20
author: Your Name
cell_count: 13
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1077b42b0>




```python
#Retrieve all rows where aspiration is turbo.
```


```python
result = con.execute("""SELECT * FROM automobile
                        WHERE "aspiration" = 'turbo' """).fetchall()
                        
```


```python
result = con.execute("""SELECT make, aspiration FROM automobile
                        WHERE "aspiration" = 'turbo' """).fetchall()
```


```python
result
                        
```




    [('audi', 'turbo'),
     ('audi', 'turbo'),
     ('dodge', 'turbo'),
     ('dodge', 'turbo'),
     ('dodge', 'turbo'),
     ('mercedes-benz', 'turbo'),
     ('mercedes-benz', 'turbo'),
     ('mercedes-benz', 'turbo'),
     ('mercedes-benz', 'turbo'),
     ('mercury', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('mitsubishi', 'turbo'),
     ('nissan', 'turbo'),
     ('peugot', 'turbo'),
     ('peugot', 'turbo'),
     ('peugot', 'turbo'),
     ('peugot', 'turbo'),
     ('peugot', 'turbo'),
     ('peugot', 'turbo'),
     ('plymouth', 'turbo'),
     ('plymouth', 'turbo'),
     ('saab', 'turbo'),
     ('saab', 'turbo'),
     ('subaru', 'turbo'),
     ('subaru', 'turbo'),
     ('toyota', 'turbo'),
     ('volkswagen', 'turbo'),
     ('volkswagen', 'turbo'),
     ('volvo', 'turbo'),
     ('volvo', 'turbo'),
     ('volvo', 'turbo'),
     ('volvo', 'turbo'),
     ('volvo', 'turbo')]




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
