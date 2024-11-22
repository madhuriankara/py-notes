---
title: Simple-Insert
date: 2024-11-22
author: Your Name
cell_count: 4
score: 0
---

```python
from pypika import Query, Table

# Define a table
users = Table("users")

# Build an INSERT query
query = Query.into(users).columns("id", "name", "age").insert(1, "John Doe", 28)
```


```python
print(query)  # Output: INSERT INTO "users" ("id","name","age") VALUES (1,'John Doe',28)
```

    INSERT INTO "users" ("id","name","age") VALUES (1,'John Doe',28)



```python

```


```python

```


---
**Score: 0**
