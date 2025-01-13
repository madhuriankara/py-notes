---
title: Sum-Price
date: 2025-01-13
author: Your Name
cell_count: 12
score: 10
---

```python
#Display the sum of Price for each Calorie_Level
```


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
      <th>Food_ID</th>
      <th>Food_Name</th>
      <th>Category</th>
      <th>Price</th>
      <th>Calories</th>
      <th>Available</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Pizza</td>
      <td>Fast Food</td>
      <td>8.99</td>
      <td>300</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400</td>
      <td>No</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200</td>
      <td>No</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Salad</td>
      <td>Healthy</td>
      <td>4.99</td>
      <td>150</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700</td>
      <td>No</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
import numpy as np
```


```python
df['Calorie_Level'] = np.where(df['Calories'] < 200, 'Low',
                      np.where(df['Calories'] <= 400, 'Medium', 'High'))
```


```python
df['Calorie_Level']
```




    0    Medium
    1      High
    2    Medium
    3    Medium
    4    Medium
    5       Low
    6    Medium
    7    Medium
    8      High
    9       Low
    Name: Calorie_Level, dtype: object




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
      <th>Food_ID</th>
      <th>Food_Name</th>
      <th>Category</th>
      <th>Price</th>
      <th>Calories</th>
      <th>Available</th>
      <th>Calorie_Level</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Pizza</td>
      <td>Fast Food</td>
      <td>8.99</td>
      <td>300</td>
      <td>Yes</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450</td>
      <td>Yes</td>
      <td>High</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400</td>
      <td>No</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250</td>
      <td>Yes</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200</td>
      <td>No</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Salad</td>
      <td>Healthy</td>
      <td>4.99</td>
      <td>150</td>
      <td>Yes</td>
      <td>Low</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350</td>
      <td>Yes</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200</td>
      <td>Yes</td>
      <td>Medium</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700</td>
      <td>No</td>
      <td>High</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100</td>
      <td>Yes</td>
      <td>Low</td>
    </tr>
  </tbody>
</table>
</div>




```python
result = df.groupby('Calorie_Level')[['Calories']].sum()
```


```python
result
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
      <th>Calories</th>
    </tr>
    <tr>
      <th>Calorie_Level</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>High</th>
      <td>1150</td>
    </tr>
    <tr>
      <th>Low</th>
      <td>250</td>
    </tr>
    <tr>
      <th>Medium</th>
      <td>1700</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


---
**Score: 10**
