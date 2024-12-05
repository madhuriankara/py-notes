---
title: Breakfast
date: 2024-12-05
author: Your Name
cell_count: 8
score: 5
---

```python
import random as rd
```


```python
random_breakfast_bundle = [
    ["Tim Hortons", "Chicken Wrap", 8.45],
    ["Tim Hortons", "Bacon Wrap", 9.45],
    ["Tim Hortons", "Farmers Wrap and Medium double double", 9.45],
]
```


```python
random_breakfast = [
    "Scrambled Omelette",
    "Chicken Wrap"
]

random_amount = [
    11.95,
    12.95,
    11.45,
    9.45
]


```


```python
def get_basic():
    r_food = random_breakfast[ rd.randint(1, len(random_breakfast)-1)]
    r_amount = random_amount[ rd.randint(1, len(random_breakfast)-1)]
    
    print(r_food, r_amount)


```


```python
def get_advanced():
    
    r_food = random_breakfast_bundle[rd.randint(0, len(random_breakfast_bundle))-1]

    print(r_food[0], r_food[1], r_food[2])

    print("Jake Breakfast Details : \n")
    print("Food : ", r_food[1])
    print("at : ", r_food[0])
    print("cost : ", r_food[2])


```


```python
def startpy():
    #get_basic()

    get_advanced()


```


```python
if __name__ == '__main__':
    startpy()
```

    Tim Hortons Farmers Wrap and Medium double double 9.45
    Jake Breakfast Details : 
    
    Food :  Farmers Wrap and Medium double double
    at :  Tim Hortons
    cost :  9.45



```python

```


---
**Score: 5**
