---
title: Simple-Join
date: 2025-01-22
author: Your Name
cell_count: 6
score: 5
---

```python
from pypika import Query, Table
```


```python

```


```python
# Define tables
users = Table("users")
orders = Table("orders")


```


```python
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
**Score: 5**
