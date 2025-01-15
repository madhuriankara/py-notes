---
title: Magic-Attr
date: 2025-01-15
author: Your Name
cell_count: 11
score: 10
---

```python
from magicattr import get, set
```


```python
!pip install magicattr
```

    Requirement already satisfied: magicattr in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (0.1.6)



```python
class Address:
    def __init__(self, city, country):
        self.city = city
        self.country = country
```


```python
class User:
    def __init__(self, name, age, address):
        self.name = name
        self.age = age
        self.address = address
```


```python
address = Address("New York", "USA")
user = User("Alice", 30, address)

```


```python
user_city = get(user, "address.city")
user_country = get(user, "address.country")
```


```python
print(f"User's city: {user_city}")  
print(f"User's country: {user_country}") 

```

    User's city: New York
    User's country: USA



```python
set(user, "address.city", "Los Angeles")
set(user, "address.country", "Canada")
```


```python
print(f"Updated city: {user.address.city}") 
print(f"Updated country: {user.address.country}") 
```

    Updated city: Los Angeles
    Updated country: Canada



```python

```


```python

```


---
**Score: 10**
