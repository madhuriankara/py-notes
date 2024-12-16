---
title: Bore-Between-2.5-3.5
date: 2024-12-15
author: Your Name
cell_count: 7
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x113c33470>




```python
#Find cars where the bore is between 2.5 and 3.5, inclusive.
```


```python
result = con.execute("""SELECT make,"bore"
                     FROM automobile
                     WHERE CAST("bore" AS FLOAT) BETWEEN 2.5 AND 3.5
                     AND bore != '?' """).fetchall()
```


```python
result
```




    [('alfa-romero', '3.47'),
     ('alfa-romero', '3.47'),
     ('alfa-romero', '2.68'),
     ('audi', '3.19'),
     ('audi', '3.19'),
     ('audi', '3.19'),
     ('audi', '3.19'),
     ('audi', '3.19'),
     ('audi', '3.13'),
     ('audi', '3.13'),
     ('bmw', '3.5'),
     ('bmw', '3.5'),
     ('bmw', '3.31'),
     ('bmw', '3.31'),
     ('bmw', '3.31'),
     ('chevrolet', '2.91'),
     ('chevrolet', '3.03'),
     ('chevrolet', '3.03'),
     ('dodge', '2.97'),
     ('dodge', '2.97'),
     ('dodge', '3.03'),
     ('dodge', '2.97'),
     ('dodge', '2.97'),
     ('dodge', '2.97'),
     ('dodge', '3.03'),
     ('dodge', '3.34'),
     ('honda', '2.91'),
     ('honda', '2.91'),
     ('honda', '2.91'),
     ('honda', '2.91'),
     ('honda', '2.91'),
     ('honda', '2.91'),
     ('honda', '2.92'),
     ('honda', '3.15'),
     ('honda', '3.15'),
     ('honda', '3.15'),
     ('honda', '3.15'),
     ('honda', '3.15'),
     ('honda', '3.15'),
     ('isuzu', '3.31'),
     ('isuzu', '3.03'),
     ('isuzu', '3.03'),
     ('isuzu', '3.43'),
     ('mazda', '3.03'),
     ('mazda', '3.03'),
     ('mazda', '3.03'),
     ('mazda', '3.03'),
     ('mazda', '3.08'),
     ('mazda', '3.39'),
     ('mazda', '3.39'),
     ('mazda', '3.39'),
     ('mazda', '3.39'),
     ('mazda', '3.39'),
     ('mazda', '3.39'),
     ('mazda', '3.43'),
     ('mercedes-benz', '3.46'),
     ('mercedes-benz', '3.46'),
     ('mitsubishi', '2.97'),
     ('mitsubishi', '2.97'),
     ('mitsubishi', '2.97'),
     ('mitsubishi', '3.03'),
     ('mitsubishi', '3.17'),
     ('mitsubishi', '3.35'),
     ('mitsubishi', '3.35'),
     ('mitsubishi', '3.35'),
     ('mitsubishi', '3.17'),
     ('mitsubishi', '3.17'),
     ('nissan', '3.15'),
     ('nissan', '2.99'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.15'),
     ('nissan', '3.33'),
     ('nissan', '3.33'),
     ('nissan', '3.43'),
     ('nissan', '3.43'),
     ('nissan', '3.43'),
     ('nissan', '3.43'),
     ('nissan', '3.43'),
     ('nissan', '3.43'),
     ('peugot', '3.46'),
     ('peugot', '3.46'),
     ('peugot', '3.46'),
     ('peugot', '3.46'),
     ('peugot', '3.46'),
     ('plymouth', '2.97'),
     ('plymouth', '3.03'),
     ('plymouth', '2.97'),
     ('plymouth', '2.97'),
     ('plymouth', '2.97'),
     ('plymouth', '3.35'),
     ('renault', '3.46'),
     ('renault', '3.46'),
     ('saab', '2.54'),
     ('toyota', '3.05'),
     ('toyota', '3.05'),
     ('toyota', '3.05'),
     ('toyota', '3.05'),
     ('toyota', '3.05'),
     ('toyota', '3.05'),
     ('toyota', '3.19'),
     ('toyota', '3.19'),
     ('toyota', '3.27'),
     ('toyota', '3.27'),
     ('toyota', '3.19'),
     ('toyota', '3.19'),
     ('toyota', '3.19'),
     ('toyota', '3.19'),
     ('toyota', '3.19'),
     ('toyota', '3.24'),
     ('toyota', '3.24'),
     ('toyota', '3.31'),
     ('toyota', '3.27'),
     ('toyota', '3.31'),
     ('toyota', '3.31'),
     ('toyota', '3.31'),
     ('toyota', '3.27'),
     ('toyota', '3.27'),
     ('toyota', '3.27'),
     ('toyota', '3.27'),
     ('volkswagen', '3.01'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.01'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.01'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.19'),
     ('volkswagen', '3.01'),
     ('volkswagen', '3.19'),
     ('volvo', '3.01')]




```python

```


---
**Score: 5**
