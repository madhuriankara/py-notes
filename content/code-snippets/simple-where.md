---
title: Simple-Where
date: 2024-11-28
author: Your Name
cell_count: 6
score: 5
---

```python
from pypika import Query, Table
```


```python
# Define a table
users = Table("users")
```


```python
# Build a SELECT query with a WHERE clause
query = Query.from_(users).select(users.id, users.name).where(users.age > 30)
```


```python
print(query)
```

    SELECT "id","name" FROM "users" WHERE "age">30



```python

```


```python

```


---
**Score: 5**
