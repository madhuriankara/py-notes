---
title: Sqllite-Test1
date: 2025-01-13
author: Your Name
cell_count: 7
score: 5
---

```python
import sqlite3
import pandas as pd

```


```python
# Load CSV file into a DataFrame
df = pd.read_csv('/Users/madhuriankaraboyina/Downloads/student_data.csv')

```


```python
# Connect to SQLite
conn = sqlite3.connect(':memory:')

```


```python
#conn = sqlite3.connect("abc.db")
```


```python
# Write DataFrame to SQLite
df.to_sql('my_table', conn, index=False)

```




    100




```python
# Perform SQL query
result = pd.read_sql_query("SELECT * FROM my_table WHERE student_id = 1", conn)

print(result)
```

       student_id student_name  test_scores  attendance  participation  \
    0           1     John Doe           85          90             80   
    
       project_scores  got_job  
    0              88        1  



```python

```


---
**Score: 5**
