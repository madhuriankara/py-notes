---
title: Profit-Margin
date: 2025-01-06
author: Your Name
cell_count: 20
score: 20
---

```python
#Calculate the profit margin for each food item, assuming a fixed cost of 70% of the Price.
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
df['Cost'] = df['Price']* 0.70
```


```python
df['Cost']
```




    0     3.843
    1     4.193
    2     2.793
    3     5.593
    4     6.293
    5     3.493
    6     2.443
    7    10.493
    8     9.093
    9     4.893
    Name: Cost, dtype: float64




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
      <th>Profit</th>
      <th>Cost</th>
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
      <td>3.843</td>
      <td>3.843</td>
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
      <td>4.193</td>
      <td>4.193</td>
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
      <td>2.793</td>
      <td>2.793</td>
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
      <td>5.593</td>
      <td>5.593</td>
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
      <td>6.293</td>
      <td>6.293</td>
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
      <td>3.493</td>
      <td>3.493</td>
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
      <td>2.443</td>
      <td>2.443</td>
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
      <td>10.493</td>
      <td>10.493</td>
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
      <td>9.093</td>
      <td>9.093</td>
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
      <td>4.893</td>
      <td>4.893</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['Profit_Margin'] = ((df['Price'] - df['Cost']) / df['Price']) * 100
```


```python
df['Profit_Margin']
```




    0    30.0
    1    30.0
    2    30.0
    3    30.0
    4    30.0
    5    30.0
    6    30.0
    7    30.0
    8    30.0
    9    30.0
    Name: Profit_Margin, dtype: float64




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
      <th>Profit</th>
      <th>Cost</th>
      <th>Profit_Margin</th>
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
      <td>3.843</td>
      <td>3.843</td>
      <td>30.0</td>
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
      <td>4.193</td>
      <td>4.193</td>
      <td>30.0</td>
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
      <td>2.793</td>
      <td>2.793</td>
      <td>30.0</td>
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
      <td>5.593</td>
      <td>5.593</td>
      <td>30.0</td>
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
      <td>6.293</td>
      <td>6.293</td>
      <td>30.0</td>
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
      <td>3.493</td>
      <td>3.493</td>
      <td>30.0</td>
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
      <td>2.443</td>
      <td>2.443</td>
      <td>30.0</td>
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
      <td>10.493</td>
      <td>10.493</td>
      <td>30.0</td>
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
      <td>9.093</td>
      <td>9.093</td>
      <td>30.0</td>
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
      <td>4.893</td>
      <td>4.893</td>
      <td>30.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.drop('Profit_Margin',axis = 1)
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
      <th>Profit</th>
      <th>Cost</th>
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
      <td>3.843</td>
      <td>3.843</td>
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
      <td>4.193</td>
      <td>4.193</td>
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
      <td>2.793</td>
      <td>2.793</td>
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
      <td>5.593</td>
      <td>5.593</td>
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
      <td>6.293</td>
      <td>6.293</td>
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
      <td>3.493</td>
      <td>3.493</td>
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
      <td>2.443</td>
      <td>2.443</td>
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
      <td>10.493</td>
      <td>10.493</td>
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
      <td>9.093</td>
      <td>9.093</td>
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
      <td>4.893</td>
      <td>4.893</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.drop('Profit',axis = 1)
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
      <th>Cost</th>
      <th>Profit_Margin</th>
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
      <td>3.843</td>
      <td>30.0</td>
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
      <td>4.193</td>
      <td>30.0</td>
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
      <td>2.793</td>
      <td>30.0</td>
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
      <td>5.593</td>
      <td>30.0</td>
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
      <td>6.293</td>
      <td>30.0</td>
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
      <td>3.493</td>
      <td>30.0</td>
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
      <td>2.443</td>
      <td>30.0</td>
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
      <td>10.493</td>
      <td>30.0</td>
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
      <td>9.093</td>
      <td>30.0</td>
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
      <td>4.893</td>
      <td>30.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.drop('Profit_Margin',axis = 1)
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
      <th>Profit</th>
      <th>Cost</th>
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
      <td>3.843</td>
      <td>3.843</td>
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
      <td>4.193</td>
      <td>4.193</td>
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
      <td>2.793</td>
      <td>2.793</td>
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
      <td>5.593</td>
      <td>5.593</td>
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
      <td>6.293</td>
      <td>6.293</td>
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
      <td>3.493</td>
      <td>3.493</td>
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
      <td>2.443</td>
      <td>2.443</td>
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
      <td>10.493</td>
      <td>10.493</td>
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
      <td>9.093</td>
      <td>9.093</td>
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
      <td>4.893</td>
      <td>4.893</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.drop('Cost',axis = 1)
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
      <th>Profit</th>
      <th>Profit_Margin</th>
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
      <td>3.843</td>
      <td>30.0</td>
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
      <td>4.193</td>
      <td>30.0</td>
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
      <td>2.793</td>
      <td>30.0</td>
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
      <td>5.593</td>
      <td>30.0</td>
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
      <td>6.293</td>
      <td>30.0</td>
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
      <td>3.493</td>
      <td>30.0</td>
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
      <td>2.443</td>
      <td>30.0</td>
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
      <td>10.493</td>
      <td>30.0</td>
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
      <td>9.093</td>
      <td>30.0</td>
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
      <td>4.893</td>
      <td>30.0</td>
    </tr>
  </tbody>
</table>
</div>




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
      <th>Profit</th>
      <th>Cost</th>
      <th>Profit_Margin</th>
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
      <td>3.843</td>
      <td>3.843</td>
      <td>30.0</td>
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
      <td>4.193</td>
      <td>4.193</td>
      <td>30.0</td>
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
      <td>2.793</td>
      <td>2.793</td>
      <td>30.0</td>
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
      <td>5.593</td>
      <td>5.593</td>
      <td>30.0</td>
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
      <td>6.293</td>
      <td>6.293</td>
      <td>30.0</td>
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
      <td>3.493</td>
      <td>3.493</td>
      <td>30.0</td>
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
      <td>2.443</td>
      <td>2.443</td>
      <td>30.0</td>
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
      <td>10.493</td>
      <td>10.493</td>
      <td>30.0</td>
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
      <td>9.093</td>
      <td>9.093</td>
      <td>30.0</td>
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
      <td>4.893</td>
      <td>4.893</td>
      <td>30.0</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


---
**Score: 20**
