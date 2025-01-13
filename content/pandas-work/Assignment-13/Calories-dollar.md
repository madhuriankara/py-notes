---
title: Calories-Dollar
date: 2025-01-13
author: Your Name
cell_count: 12
score: 10
---

```python
#Add a new column that calculates Calories per Dollar (Calories / Price).
```


```python
import pandas as pd
```


```python
food = pd.read_csv('food.csv')
```


```python
food_sales = pd.read_csv('food_sales.csv')
```


```python
ratings = pd.read_csv('ratings.csv')
```


```python
df = pd.merge(food, food_sales, on='Food_Name', how='outer')
```


```python
df = pd.merge(df, ratings, on='Food_Name', how='outer')
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
      <th>Units_Sold</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450</td>
      <td>Yes</td>
      <td>200</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350</td>
      <td>Yes</td>
      <td>100</td>
      <td>3.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200</td>
      <td>Yes</td>
      <td>400</td>
      <td>4.8</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400</td>
      <td>No</td>
      <td>150</td>
      <td>3.8</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>Pizza</td>
      <td>Fast Food</td>
      <td>8.99</td>
      <td>300</td>
      <td>Yes</td>
      <td>120</td>
      <td>4.5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Salad</td>
      <td>Healthy</td>
      <td>4.99</td>
      <td>150</td>
      <td>Yes</td>
      <td>300</td>
      <td>4.6</td>
    </tr>
    <tr>
      <th>6</th>
      <td>10</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100</td>
      <td>Yes</td>
      <td>250</td>
      <td>4.3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>9</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700</td>
      <td>No</td>
      <td>80</td>
      <td>4.4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250</td>
      <td>Yes</td>
      <td>50</td>
      <td>4.7</td>
    </tr>
    <tr>
      <th>9</th>
      <td>5</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200</td>
      <td>No</td>
      <td>180</td>
      <td>4.2</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['Calories/dollar'] = df['Calories']/df['Price']
```


```python
df['Calories/dollar']
```




    0    81.967213
    1    58.430718
    2    50.125313
    3    50.062578
    4    33.370412
    5    30.060120
    6    28.653295
    7    46.697799
    8    19.245574
    9    28.612303
    Name: Calories/dollar, dtype: float64




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
      <th>Units_Sold</th>
      <th>Rating</th>
      <th>Calories/dollar</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450</td>
      <td>Yes</td>
      <td>200</td>
      <td>4.0</td>
      <td>81.967213</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350</td>
      <td>Yes</td>
      <td>100</td>
      <td>3.9</td>
      <td>58.430718</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200</td>
      <td>Yes</td>
      <td>400</td>
      <td>4.8</td>
      <td>50.125313</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400</td>
      <td>No</td>
      <td>150</td>
      <td>3.8</td>
      <td>50.062578</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1</td>
      <td>Pizza</td>
      <td>Fast Food</td>
      <td>8.99</td>
      <td>300</td>
      <td>Yes</td>
      <td>120</td>
      <td>4.5</td>
      <td>33.370412</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Salad</td>
      <td>Healthy</td>
      <td>4.99</td>
      <td>150</td>
      <td>Yes</td>
      <td>300</td>
      <td>4.6</td>
      <td>30.060120</td>
    </tr>
    <tr>
      <th>6</th>
      <td>10</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100</td>
      <td>Yes</td>
      <td>250</td>
      <td>4.3</td>
      <td>28.653295</td>
    </tr>
    <tr>
      <th>7</th>
      <td>9</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700</td>
      <td>No</td>
      <td>80</td>
      <td>4.4</td>
      <td>46.697799</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250</td>
      <td>Yes</td>
      <td>50</td>
      <td>4.7</td>
      <td>19.245574</td>
    </tr>
    <tr>
      <th>9</th>
      <td>5</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200</td>
      <td>No</td>
      <td>180</td>
      <td>4.2</td>
      <td>28.612303</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


---
**Score: 10**
