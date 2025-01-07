---
title: Noincome
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
con.execute("CREATE TABLE food AS SELECT * FROM 'updatedonline_file.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x113bfa8b0>




```python
#How many individuals have no income?
```


```python
result = con.execute("""SELECT * FROM food 
                        WHERE Monthly-Income = 'No Income' LIMIT 10""").fetchall()
```


    ---------------------------------------------------------------------------

    BinderException                           Traceback (most recent call last)

    Cell In[6], line 1
    ----> 1 result = con.execute("""SELECT * FROM food 
          2                         WHERE Monthly-Income = 'No Income' LIMIT 10""").fetchall()


    BinderException: Binder Error: Referenced column "Monthly" not found in FROM clause!
    Candidate bindings: "food.Monthly-Income", "food.Monthly Income", "food.longitude", "food.Marital-Status"
    LINE 2:                         WHERE Monthly-Income = 'No Income' LIMIT 10
                                          ^



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
