---
title: Mean-Median-Duckdb
date: 2025-01-20
author: Your Name
cell_count: 13
score: 10
---

```python
#Find the mean, median, and standard deviation of the price column.
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




    <duckdb.duckdb.DuckDBPyConnection at 0x113d68070>




```python

```


```python
result = con.execute("SELECT AVG(CAST(price AS INT)) FROM automobile WHERE price != '?'").fetchall()
```


```python
result
```




    [(13207.129353233831,)]




```python
#Identify the number of cars for each fuel-type.
```


```python
result = con.execute(""" SELECT "fuel-type",make, COUNT(*) AS number_cars
                        FROM automobile
                        WHERE "fuel-type" IN ('gas','diesel')
                        GROUP BY make, "fuel-type" """).fetchall()
```


```python
result
```




    [('gas', 'honda', 13),
     ('diesel', 'mazda', 2),
     ('gas', 'subaru', 12),
     ('gas', 'toyota', 29),
     ('diesel', 'volkswagen', 4),
     ('gas', 'isuzu', 4),
     ('gas', 'jaguar', 3),
     ('gas', 'bmw', 8),
     ('gas', 'mercury', 1),
     ('gas', 'nissan', 17),
     ('gas', 'plymouth', 7),
     ('gas', 'volvo', 10),
     ('gas', 'audi', 7),
     ('gas', 'chevrolet', 3),
     ('diesel', 'mercedes-benz', 4),
     ('gas', 'peugot', 6),
     ('gas', 'saab', 6),
     ('gas', 'dodge', 9),
     ('gas', 'mazda', 15),
     ('gas', 'mitsubishi', 13),
     ('gas', 'porsche', 5),
     ('gas', 'renault', 2),
     ('diesel', 'toyota', 3),
     ('gas', 'volkswagen', 8),
     ('gas', 'alfa-romero', 3),
     ('gas', 'mercedes-benz', 4),
     ('diesel', 'peugot', 5),
     ('diesel', 'nissan', 1),
     ('diesel', 'volvo', 1)]




```python
con.execute("""SELECT * FROM automobile WHERE "fuel-type" IN ('gas') LIMIT 2""").fetchall()
```




    [(3,
      '?',
      'alfa-romero',
      'gas',
      'std',
      'two',
      'convertible',
      'rwd',
      'front',
      88.6,
      168.8,
      64.1,
      48.8,
      2548,
      'dohc',
      'four',
      130,
      'mpfi',
      '3.47',
      '2.68',
      9.0,
      '111',
      '5000',
      21,
      27,
      '13495'),
     (3,
      '?',
      'alfa-romero',
      'gas',
      'std',
      'two',
      'convertible',
      'rwd',
      'front',
      88.6,
      168.8,
      64.1,
      48.8,
      2548,
      'dohc',
      'four',
      130,
      'mpfi',
      '3.47',
      '2.68',
      9.0,
      '111',
      '5000',
      21,
      27,
      '16500')]




```python
con.execute("""SELECT DISTINCT("fuel-type") FROM automobile""").fetchall()
```




    [('gas',), ('diesel',)]




```python

```


---
**Score: 10**
