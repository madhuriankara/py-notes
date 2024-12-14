---
title: Food-Items
date: 2024-12-13
author: Your Name
cell_count: 12
score: 10
---

```python
#Count the number of food items available (Available = "Yes") in each Category.
```


```python
import pandas as pd
```


```python
FILEPATH ='food.csv'
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
result = df[df['Available'] == 'Yes'].groupby(['Food_Name','Category'])
```


```python
result
```




    <pandas.core.groupby.generic.DataFrameGroupBy object at 0x10472baa0>




```python

```


```python

```


```python
new_df = df[df['Available'] == 'Yes'] [['Food_Name','Category']].count()
```


```python
new_df
```




    Food_Name    7
    Category     7
    dtype: int64




```python

```


---
**Score: 10**
