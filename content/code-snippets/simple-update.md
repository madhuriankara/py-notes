---
title: Simple-Update
date: 2024-11-22
author: Your Name
cell_count: 4
score: 0
---

```python
from pypika import Query, Table

# Define a table
users = Table("users")

# Build an UPDATE query
query = Query.update(users).set(users.name, "Jane Doe").where(users.id == 1)


```


```python
print(query)  # Output: UPDATE "users" SET "name"='Jane Doe' WHERE "id"=1

```

    UPDATE "users" SET "name"='Jane Doe' WHERE "id"=1



```python

```


```python

```


---
**Score: 0**
