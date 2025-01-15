---
title: Average-Price-Groupby-Make
date: 2025-01-15
author: Your Name
cell_count: 12
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




    <duckdb.duckdb.DuckDBPyConnection at 0x104472bb0>




```python
#Identify the average price of cars grouped by make.
```


```python
result = con.execute("""SELECT make, AVG(CAST(price AS INT)) FROM automobile
                        WHERE price != '?'
                       GROUP BY make """).fetchall()
                        
```


```python
result                  
```




    [('audi', 17859.166666666668),
     ('peugot', 15489.09090909091),
     ('saab', 15223.333333333334),
     ('mitsubishi', 9239.76923076923),
     ('nissan', 10415.666666666666),
     ('alfa-romero', 15498.333333333334),
     ('dodge', 7875.444444444444),
     ('honda', 8184.692307692308),
     ('volvo', 18063.18181818182),
     ('mercury', 16503.0),
     ('subaru', 8541.25),
     ('mercedes-benz', 33647.0),
     ('volkswagen', 10077.5),
     ('jaguar', 34600.0),
     ('porsche', 31400.5),
     ('bmw', 26118.75),
     ('isuzu', 8916.5),
     ('mazda', 10652.882352941177),
     ('plymouth', 7963.428571428572),
     ('toyota', 9885.8125),
     ('chevrolet', 6007.0),
     ('renault', 9595.0)]




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
