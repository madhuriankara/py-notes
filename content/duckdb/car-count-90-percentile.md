---
title: Car-Count-90-Percentile
date: 2025-01-22
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
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x1062feb30>




```python
#Count how many cars have a height above the 90th percentile.
```


```python
result = con.execute("""SELECT "height" ,make, COUNT(*) AS num_cars FROM automobile
                        WHERE height > 0.9
                        GROUP BY make, "height" """).fetchall()
                        
```


```python
result
```




    [(52.6, 'honda', 3),
     (54.5, 'honda', 1),
     (50.8, 'mercedes-benz', 1),
     (49.4, 'mitsubishi', 2),
     (50.6, 'plymouth', 1),
     (54.5, 'toyota', 3),
     (52.6, 'toyota', 4),
     (48.8, 'alfa-romero', 2),
     (53.7, 'bmw', 1),
     (59.8, 'dodge', 1),
     (50.2, 'dodge', 1),
     (50.8, 'honda', 2),
     (54.1, 'mazda', 5),
     (54.4, 'mazda', 2),
     (56.7, 'mercedes-benz', 1),
     (55.4, 'mercedes-benz', 1),
     (50.2, 'mitsubishi', 3),
     (50.2, 'porsche', 1),
     (54.3, 'subaru', 2),
     (59.1, 'toyota', 3),
     (53.2, 'chevrolet', 1),
     (51.4, 'isuzu', 1),
     (53.7, 'mazda', 2),
     (56.5, 'mercedes-benz', 2),
     (54.8, 'mercury', 1),
     (49.7, 'nissan', 3),
     (59.8, 'plymouth', 1),
     (50.2, 'plymouth', 1),
     (55.2, 'renault', 1),
     (55.7, 'subaru', 1),
     (54.9, 'subaru', 2),
     (54.9, 'toyota', 3),
     (54.3, 'audi', 2),
     (58.3, 'honda', 1),
     (53.3, 'honda', 2),
     (52.0, 'isuzu', 2),
     (52.8, 'jaguar', 2),
     (47.8, 'jaguar', 1),
     (55.5, 'mazda', 4),
     (51.6, 'mitsubishi', 4),
     (51.6, 'porsche', 3),
     (52.5, 'subaru', 3),
     (53.0, 'subaru', 2),
     (53.0, 'toyota', 4),
     (55.6, 'volkswagen', 1),
     (51.4, 'volkswagen', 1),
     (56.2, 'volvo', 3),
     (55.7, 'audi', 2),
     (51.0, 'honda', 1),
     (54.5, 'nissan', 6),
     (54.7, 'nissan', 2),
     (56.1, 'nissan', 1),
     (58.7, 'peugot', 3),
     (56.0, 'peugot', 1),
     (50.5, 'porsche', 1),
     (50.5, 'renault', 1),
     (53.9, 'toyota', 2),
     (57.5, 'volvo', 3),
     (55.5, 'volvo', 5),
     (53.1, 'audi', 1),
     (55.7, 'bmw', 2),
     (50.8, 'dodge', 3),
     (54.1, 'honda', 3),
     (49.6, 'mazda', 4),
     (56.3, 'mercedes-benz', 1),
     (50.8, 'mitsubishi', 4),
     (55.1, 'nissan', 2),
     (56.7, 'peugot', 7),
     (56.1, 'saab', 6),
     (54.1, 'toyota', 2),
     (55.9, 'audi', 1),
     (54.3, 'bmw', 4),
     (53.5, 'isuzu', 1),
     (50.8, 'plymouth', 4),
     (53.7, 'subaru', 2),
     (52.8, 'toyota', 4),
     (52.0, 'toyota', 7),
     (55.7, 'volkswagen', 7),
     (55.1, 'volkswagen', 3),
     (52.4, 'alfa-romero', 1),
     (52.0, 'audi', 1),
     (56.3, 'bmw', 1),
     (52.0, 'chevrolet', 2),
     (50.6, 'dodge', 4),
     (58.7, 'mercedes-benz', 1),
     (54.9, 'mercedes-benz', 1),
     (53.5, 'nissan', 2),
     (53.3, 'nissan', 2)]




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
