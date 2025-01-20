---
title: Simple-Select
date: 2025-01-20
author: Your Name
cell_count: 8
score: 5
---

```python
from pypika import Query, Table
```


```python
!pip install pypika
```

    Requirement already satisfied: pypika in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (0.48.9)



```python

```


```python
# Define a table
users = Table("users")
```


```python
# Build a SELECT query
query = Query.from_(users).select(users.id, users.name)
```


```python
print(query)
```

    SELECT "id","name" FROM "users"



```python

```


```python

```


---
**Score: 5**
