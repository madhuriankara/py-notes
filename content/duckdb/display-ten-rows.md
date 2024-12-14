---
title: Display-Ten-Rows
date: 2024-12-13
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




    <duckdb.duckdb.DuckDBPyConnection at 0x110028b70>




```python
#Display only the first 10 rows of the dataset.
```


```python
result = con.execute("""SELECT * FROM automobile LIMIT 10""").fetchall()
```


```python
result
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
      '16500'),
     (1,
      '?',
      'alfa-romero',
      'gas',
      'std',
      'two',
      'hatchback',
      'rwd',
      'front',
      94.5,
      171.2,
      65.5,
      52.4,
      2823,
      'ohcv',
      'six',
      152,
      'mpfi',
      '2.68',
      '3.47',
      9.0,
      '154',
      '5000',
      19,
      26,
      '16500'),
     (2,
      '164',
      'audi',
      'gas',
      'std',
      'four',
      'sedan',
      'fwd',
      'front',
      99.8,
      176.6,
      66.2,
      54.3,
      2337,
      'ohc',
      'four',
      109,
      'mpfi',
      '3.19',
      '3.4',
      10.0,
      '102',
      '5500',
      24,
      30,
      '13950'),
     (2,
      '164',
      'audi',
      'gas',
      'std',
      'four',
      'sedan',
      '4wd',
      'front',
      99.4,
      176.6,
      66.4,
      54.3,
      2824,
      'ohc',
      'five',
      136,
      'mpfi',
      '3.19',
      '3.4',
      8.0,
      '115',
      '5500',
      18,
      22,
      '17450'),
     (2,
      '?',
      'audi',
      'gas',
      'std',
      'two',
      'sedan',
      'fwd',
      'front',
      99.8,
      177.3,
      66.3,
      53.1,
      2507,
      'ohc',
      'five',
      136,
      'mpfi',
      '3.19',
      '3.4',
      8.5,
      '110',
      '5500',
      19,
      25,
      '15250'),
     (1,
      '158',
      'audi',
      'gas',
      'std',
      'four',
      'sedan',
      'fwd',
      'front',
      105.8,
      192.7,
      71.4,
      55.7,
      2844,
      'ohc',
      'five',
      136,
      'mpfi',
      '3.19',
      '3.4',
      8.5,
      '110',
      '5500',
      19,
      25,
      '17710'),
     (1,
      '?',
      'audi',
      'gas',
      'std',
      'four',
      'wagon',
      'fwd',
      'front',
      105.8,
      192.7,
      71.4,
      55.7,
      2954,
      'ohc',
      'five',
      136,
      'mpfi',
      '3.19',
      '3.4',
      8.5,
      '110',
      '5500',
      19,
      25,
      '18920'),
     (1,
      '158',
      'audi',
      'gas',
      'turbo',
      'four',
      'sedan',
      'fwd',
      'front',
      105.8,
      192.7,
      71.4,
      55.9,
      3086,
      'ohc',
      'five',
      131,
      'mpfi',
      '3.13',
      '3.4',
      8.3,
      '140',
      '5500',
      17,
      20,
      '23875'),
     (0,
      '?',
      'audi',
      'gas',
      'turbo',
      'two',
      'hatchback',
      '4wd',
      'front',
      99.5,
      178.2,
      67.9,
      52.0,
      3053,
      'ohc',
      'five',
      131,
      'mpfi',
      '3.13',
      '3.4',
      7.0,
      '160',
      '5500',
      16,
      22,
      '?')]




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
