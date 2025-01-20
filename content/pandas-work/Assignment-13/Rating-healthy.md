---
title: Rating-Healthy
date: 2025-01-20
author: Your Name
cell_count: 28
score: 25
---

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
df =pd.concat([food, food_sales, ratings], ignore_index=True)
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
      <td>1.0</td>
      <td>Pizza</td>
      <td>Fast Food</td>
      <td>8.99</td>
      <td>300.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.0</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3.0</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400.0</td>
      <td>No</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.0</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200.0</td>
      <td>No</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6.0</td>
      <td>Salad</td>
      <td>Healthy</td>
      <td>4.99</td>
      <td>150.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.0</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.0</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9.0</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700.0</td>
      <td>No</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10.0</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100.0</td>
      <td>Yes</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>NaN</td>
      <td>Pizza</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>120.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>NaN</td>
      <td>Burger</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>200.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>NaN</td>
      <td>Pasta</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>150.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>NaN</td>
      <td>Sushi</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>NaN</td>
      <td>Tacos</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>180.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>NaN</td>
      <td>Salad</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>300.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>16</th>
      <td>NaN</td>
      <td>Fried Rice</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NaN</td>
      <td>Ice Cream</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>400.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>18</th>
      <td>NaN</td>
      <td>Steak</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>80.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>19</th>
      <td>NaN</td>
      <td>Soup</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>250.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20</th>
      <td>NaN</td>
      <td>Pizza</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.5</td>
    </tr>
    <tr>
      <th>21</th>
      <td>NaN</td>
      <td>Burger</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>NaN</td>
      <td>Pasta</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.8</td>
    </tr>
    <tr>
      <th>23</th>
      <td>NaN</td>
      <td>Sushi</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.7</td>
    </tr>
    <tr>
      <th>24</th>
      <td>NaN</td>
      <td>Tacos</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>NaN</td>
      <td>Salad</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.6</td>
    </tr>
    <tr>
      <th>26</th>
      <td>NaN</td>
      <td>Fried Rice</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.9</td>
    </tr>
    <tr>
      <th>27</th>
      <td>NaN</td>
      <td>Ice Cream</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.8</td>
    </tr>
    <tr>
      <th>28</th>
      <td>NaN</td>
      <td>Steak</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.4</td>
    </tr>
    <tr>
      <th>29</th>
      <td>NaN</td>
      <td>Soup</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.3</td>
    </tr>
  </tbody>
</table>
</div>




```python
merged_df = pd.merge(food, food_sales, on='Food_Name', how='outer')
```


```python
merged_df = pd.merge(merged_df, ratings, on='Food_Name', how='outer')
```


```python
merged_df
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
#Find the average rating for items in the Healthy category.
```


```python
average_df = merged_df[merged_df['Category'] == 'Healthy']['Rating'].mean()
```


```python
average_df
```




    4.449999999999999




```python

```


```python
#Merge the dataset with a sales data file and calculate total revenue for each Category.
```


```python
merged_df['Total_Revenue'] = merged_df['Price']* merged_df['Units_Sold']
```


```python
Total_Revenue
```




    0    1098.0
    1     599.0
    2    1596.0
    3    1198.5
    4    1078.8
    5    1497.0
    6     872.5
    7    1199.2
    8     649.5
    9    1258.2
    dtype: float64




```python
merged_df
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
      <th>Total_Revenue</th>
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
      <td>1098.0</td>
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
      <td>599.0</td>
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
      <td>1596.0</td>
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
      <td>1198.5</td>
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
      <td>1078.8</td>
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
      <td>1497.0</td>
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
      <td>872.5</td>
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
      <td>1199.2</td>
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
      <td>649.5</td>
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
      <td>1258.2</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Find food items with a rating below 4.0 and display their details.
```


```python

```


```python
merged_df_rating = merged_df.loc[merged_df['Rating']< 4][['Food_Name','Rating']]
```


```python
merged_df_rating 
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
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Fried Rice</td>
      <td>3.9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Pasta</td>
      <td>3.8</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Add a new column that combines Category and Rating into a single string.
```


```python
merged_df['Rating_category'] = merged_df['Category'] + '-' + merged_df['Rating'].astype(str)
```


```python
merged_df['Rating_category']
```




    0    Fast Food-4.0
    1        Asian-3.9
    2      Dessert-4.8
    3      Italian-3.8
    4    Fast Food-4.5
    5      Healthy-4.6
    6      Healthy-4.3
    7        Grill-4.4
    8     Japanese-4.7
    9      Mexican-4.2
    Name: Rating_category, dtype: object




```python
merged_df
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
      <th>Total_Revenue</th>
      <th>new_colum</th>
      <th>Rating_category</th>
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
      <td>1098.0</td>
      <td>Fast Food-4.0</td>
      <td>Fast Food-4.0</td>
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
      <td>599.0</td>
      <td>Asian-3.9</td>
      <td>Asian-3.9</td>
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
      <td>1596.0</td>
      <td>Dessert-4.8</td>
      <td>Dessert-4.8</td>
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
      <td>1198.5</td>
      <td>Italian-3.8</td>
      <td>Italian-3.8</td>
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
      <td>1078.8</td>
      <td>Fast Food-4.5</td>
      <td>Fast Food-4.5</td>
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
      <td>1497.0</td>
      <td>Healthy-4.6</td>
      <td>Healthy-4.6</td>
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
      <td>872.5</td>
      <td>Healthy-4.3</td>
      <td>Healthy-4.3</td>
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
      <td>1199.2</td>
      <td>Grill-4.4</td>
      <td>Grill-4.4</td>
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
      <td>649.5</td>
      <td>Japanese-4.7</td>
      <td>Japanese-4.7</td>
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
      <td>1258.2</td>
      <td>Mexican-4.2</td>
      <td>Mexican-4.2</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


```python

```


```python

```


---
**Score: 25**
