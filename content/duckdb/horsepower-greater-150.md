---
title: Horsepower-Greater-150
date: 2025-01-22
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




    <duckdb.duckdb.DuckDBPyConnection at 0x106adebf0>




```python
#Filter rows where horsepower is greater than 150
```


```python
result = con.execute("""SELECT make,horsepower FROM automobile 
                     WHERE CAST(horsepower AS INT) > 150
                     AND horsepower != '?' LIMIT 2""").fetchall()
```


```python
result
```




    [('alfa-romero', '154'), ('audi', '160')]




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
