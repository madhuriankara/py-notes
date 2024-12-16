---
title: Histogram-Calories
date: 2024-12-15
author: Your Name
cell_count: 17
score: 15
---

```python
#Create a histogram of the Calories column.
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
df = pd.merge(food, food_sales, on ='Food_Name')
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
      <td>120</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Burger</td>
      <td>Fast Food</td>
      <td>5.49</td>
      <td>450</td>
      <td>Yes</td>
      <td>200</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Pasta</td>
      <td>Italian</td>
      <td>7.99</td>
      <td>400</td>
      <td>No</td>
      <td>150</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Sushi</td>
      <td>Japanese</td>
      <td>12.99</td>
      <td>250</td>
      <td>Yes</td>
      <td>50</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Tacos</td>
      <td>Mexican</td>
      <td>6.99</td>
      <td>200</td>
      <td>No</td>
      <td>180</td>
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
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>Fried Rice</td>
      <td>Asian</td>
      <td>5.99</td>
      <td>350</td>
      <td>Yes</td>
      <td>100</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Ice Cream</td>
      <td>Dessert</td>
      <td>3.99</td>
      <td>200</td>
      <td>Yes</td>
      <td>400</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Steak</td>
      <td>Grill</td>
      <td>14.99</td>
      <td>700</td>
      <td>No</td>
      <td>80</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Soup</td>
      <td>Healthy</td>
      <td>3.49</td>
      <td>100</td>
      <td>Yes</td>
      <td>250</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib.pyplot as plt
```


```python
df['Calories'].plot(kind='hist', bins=6, edgecolor='black', alpha=0.7)
plt.title('Distribution of Calories')
plt.xlabel('Calories')
plt.ylabel('Frequency')
```




    Text(0, 0.5, 'Frequency')




    
![png](histogram-calories_files/histogram-calories_7_1.png)
    



```python
#Bar Graph
```


```python
category_counts = df['Category'].value_counts()
```


```python
category_counts.plot(kind='bar', color='skyblue', edgecolor='black')
plt.title('Count of Items in Each Category')
plt.xlabel('Category')
plt.ylabel('Count')
plt.show()

```


    
![png](histogram-calories_files/histogram-calories_10_0.png)
    



```python
#Create a scatter plot of Price vs. Calories.
```


```python
plt.scatter(df['Price'], df['Calories'], color='purple', edgecolor='black')
plt.title('Price vs. Calories')
plt.xlabel('Price')
plt.ylabel('Calories')
plt.show()
```


    
![png](histogram-calories_files/histogram-calories_12_0.png)
    



```python
#piechart
```


```python
category_counts = df['Category'].value_counts()
```


```python
category_counts.plot(kind='pie', autopct='%1.1f%%',colors=['skyblue', 'pink'])
plt.title('Percentage Distribution of Items by Category')
plt.show()
```


    
![png](histogram-calories_files/histogram-calories_15_0.png)
    



```python

```


---
**Score: 15**
