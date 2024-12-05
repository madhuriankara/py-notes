---
title: 2-Address
date: 2024-12-05
author: Your Name
cell_count: 12
score: 10
---

```python
from faker import Faker
```


```python
fake = Faker()
```


```python
for _ in range(5):
    SUITE_NO = f'{fake.random_int(1,99)} - {fake.random_int(1,99)}'
```


```python
    STREET_NAME = fake.street_name()
```


```python
print (f'{SUITE_NO} - {STREET_NAME}')
```

    23 - 55 - Gabriel Summit



```python
for _ in range(5):
    SUITE_NO = f'{fake.random_int(5,10)} - {fake.random_int(2,60)}'
```


```python
STREET_NAME = fake.street_name()
```


```python
print (f'{SUITE_NO} - {STREET_NAME}')
```

    7 - 45 - Malone Point



```python
for _ in range(5):
    SUITE_NO = f'{fake.random_int(1,99)} - {fake.random_int(1,99)}'
```


```python
STREET_NAME = fake.street_name()
```


```python
print (f'{SUITE_NO} - {STREET_NAME}')
```

    28 - 39 - Kristy Squares



```python

```


---
**Score: 10**
