---
title: Price-Ascending
date: 2025-01-03
author: Your Name
cell_count: 11
score: 10
---

```python
!pip install duckdb
```

    Collecting duckdb
      Downloading duckdb-1.1.3-cp312-cp312-macosx_12_0_arm64.whl.metadata (762 bytes)
    Downloading duckdb-1.1.3-cp312-cp312-macosx_12_0_arm64.whl (15.5 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m15.5/15.5 MB[0m [31m34.2 MB/s[0m eta [36m0:00:00[0m31m36.0 MB/s[0m eta [36m0:00:01[0m
    [?25hInstalling collected packages: duckdb
    Successfully installed duckdb-1.1.3



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




    <duckdb.duckdb.DuckDBPyConnection at 0x103769370>




```python
#Sort the data by price in ascending order.
```


```python
result = con.execute("""SELECT price FROM automobile 
                        ORDER BY price ASC LIMIT 10""").fetchall()
```


```python
result
```




    [('10198',),
     ('10245',),
     ('10295',),
     ('10345',),
     ('10595',),
     ('10698',),
     ('10795',),
     ('10898',),
     ('10945',),
     ('11048',)]




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
