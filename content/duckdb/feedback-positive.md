---
title: Feedback-Positive
date: 2025-01-13
author: Your Name
cell_count: 12
score: 10
---

```python
# Created: 2025-01-02
```


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




    <duckdb.duckdb.DuckDBPyConnection at 0x105987530>




```python
#Find the total number of individuals whose feedback is "Positive"
```


```python
result = con.execute("""SELECT COUNT(*) AS positive_Feedback 
                        FROM food 
                        WHERE Feedback = 'Positive'""").fetchall()
```


```python
result
```




    [(317,)]




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
