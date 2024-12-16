---
title: Simple-Insert
date: 2024-12-15
author: Your Name
cell_count: 7
score: 5
---

```python

```


```python

```


```python
from pypika import Query, Table


```


```python
# Define the table
users = Table('users')


```


```python
# Build the INSERT query
query = Query.into(users).columns('name', 'age').insert('Alice', 25)


```


```python
# Print the query
print(str(query))
```

    INSERT INTO "users" ("name","age") VALUES ('Alice',25)



```python

```


---
**Score: 5**
