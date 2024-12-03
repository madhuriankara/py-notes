---
title: Lessthan
date: 2024-12-03
author: Your Name
cell_count: 6
score: 5
---

```python
import pandas as pd
```


```python
FILEPATH ='food.csv'
```


```python
df= pd.read_csv(FILEPATH)
```


```python
df = df[df['Calories'] < 200] [['Food_Name','Calories']]
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Food_Name</th>
      <th>Calories</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>Salad</td>
      <td>150</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Soup</td>
      <td>100</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


---
**Score: 5**
