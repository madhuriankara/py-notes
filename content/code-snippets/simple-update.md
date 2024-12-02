---
title: Simple-Update
date: 2024-12-02
author: Your Name
cell_count: 5
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
# Build an UPDATE query
query = Query.update(users).set(users.name, "Jane Doe").where(users.id == 1)
```


```python
print(query)
```

    UPDATE "users" SET "name"='Jane Doe' WHERE "id"=1



```python

```


---
**Score: 5**
