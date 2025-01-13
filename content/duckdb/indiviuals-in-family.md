---
title: Indiviuals-In-Family
date: 2025-01-13
author: Your Name
cell_count: 7
score: 5
---

```python
##How many individuals belong to each family size?
```


```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE food AS SELECT * FROM 'updated_file.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x107a0df70>




```python
#Retrieve all records where the monthly income is "Below Rs.10000".
```


```python
result = con.execute("""SELECT * FROM food
            WHERE CAST("Monthly-Income" AS INTEGER) == 10000""").fetchall()
```


    ---------------------------------------------------------------------------

    ConversionException                       Traceback (most recent call last)

    Cell In[17], line 1
    ----> 1 result = con.execute("""SELECT * FROM food
          2             WHERE CAST("Monthly-Income" AS INTEGER) == 10000""").fetchall()


    ConversionException: Conversion Error: Could not convert string 'No Income' to INT32
    LINE 2:             WHERE CAST("Monthly-Income...
                              ^



```python

```


---
**Score: 5**
