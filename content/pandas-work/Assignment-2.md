---
title: Assignment-2
date: 2024-12-02
author: Your Name
cell_count: 7
score: 5
---

```python
import pandas as pd
```


```python
FILEPATH = 'food.csv'
```


```python
df = pd.read_csv(FILEPATH)
```


```python
df.all()
```




    Food_ID      True
    Food_Name    True
    Category     True
    Price        True
    Calories     True
    Available    True
    dtype: bool




```python
df['Price'] = df['Price']>10
```


```python

```


```python

```


---
**Score: 5**
