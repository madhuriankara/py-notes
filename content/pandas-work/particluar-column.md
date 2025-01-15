---
title: Particluar-Column
date: 2025-01-15
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
df = df[df['Available'] == 'Yes'][['Food_Name','Calories']]
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
      <th>0</th>
      <td>Pizza</td>
      <td>300</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Burger</td>
      <td>450</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Sushi</td>
      <td>250</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Salad</td>
      <td>150</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Fried Rice</td>
      <td>350</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Ice Cream</td>
      <td>200</td>
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


```python

```


---
**Score: 5**
