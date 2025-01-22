---
title: Intermediate-1
date: 2025-01-22
author: Your Name
cell_count: 9
score: 5
---

```python
#Identify the make with the highest number of models in the dataset.
```


```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x107e5c970>




```python
#Identify the make with the highest number of models in the dataset.
```


```python
result = con.execute("""SELECT make, COUNT(*) AS highest_models FROM automobile
                       GROUP BY make """).fetchall()
                        
```


```python
result = con.execute("""SELECT Make, COUNT(*) AS Model_Count
                            FROM automobile
                            GROUP BY Make
                            ORDER BY Model_Count DESC
                            LIMIT 1;
                            """).fetchall()
```


```python
result
```




    [('toyota', 32)]




```python

```


---
**Score: 5**
