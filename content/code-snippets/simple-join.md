---
title: Simple-Join
date: 2024-11-22
author: Your Name
cell_count: 3
score: 0
---

```python
from pypika import Query, Table

# Define tables
users = Table("users")
orders = Table("orders")

# Build a JOIN query
query = (
    Query.from_(users)
    .join(orders)
    .on(users.id == orders.user_id)
    .select(users.name, orders.order_date)
)



```


```python
print(query)
```

    SELECT "users"."name","orders"."order_date" FROM "users" JOIN "orders" ON "users"."id"="orders"."user_id"



```python

```


---
**Score: 0**
