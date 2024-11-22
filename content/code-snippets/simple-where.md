---
title: Simple-Where
date: 2024-11-22
author: Your Name
cell_count: 3
score: 0
---

```python
from pypika import Query, Table

# Define a table
users = Table("users")

# Build a SELECT query with a WHERE clause
query = Query.from_(users).select(users.id, users.name).where(users.age > 30)



```


```python
print(query)  # Output: SELECT "id","name" FROM "users" WHERE "age">30
```

    SELECT "id","name" FROM "users" WHERE "age">30



```python

```


---
**Score: 0**
