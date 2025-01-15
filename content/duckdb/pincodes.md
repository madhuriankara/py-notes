---
title: Pincodes
date: 2025-01-15
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




    <duckdb.duckdb.DuckDBPyConnection at 0x1061fed70>




```python
#List all unique pin codes in the dataset..
```


```python
result = con.execute("""SELECT DISTINCT("pin-code") FROM food LIMIT 10""").fetchall()
```


```python
result
```




    [(560026,),
     (560002,),
     (560096,),
     (560022,),
     (560100,),
     (560079,),
     (560034,),
     (560025,),
     (560046,),
     (560024,)]




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
