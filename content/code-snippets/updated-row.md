---
title: Updated-Row
date: 2024-11-22
author: Your Name
cell_count: 3
score: 0
---

```python
from pypika import Query, Table, functions as fn
import sqlite3  # Use your preferred database connector (e.g., psycopg2 for PostgreSQL)

# Define the table
users = Table("users")

# Build a query to fetch updated rows based on an `updated_at` column
last_checked_time = "2024-11-01 00:00:00"
query = (
    Query.from_(users)
    .select(users.id, users.name, users.updated_at)
    .where(users.updated_at > last_checked_time)
)
```


```python
# Generate the SQL string
sql_query = str(query)
print("Generated SQL:", sql_query)

# Execute the query using SQLite (or adapt to your database)
def execute_query(sql):
    try:
        # Connect to the database
        conn = sqlite3.connect("example.db")  # Replace with your database path/connection string
        cursor = conn.cursor()

        # Execute the query
        cursor.execute(sql)
        rows = cursor.fetchall()

        # Print the results
        print("Updated rows:")
        for row in rows:
            print(row)
    except Exception as e:
        print("Error:", e)
    finally:
        # Ensure the connection is closed
        conn.close()

# Run the function with the generated query
execute_query(sql_query)

```

    Generated SQL: SELECT "id","name","updated_at" FROM "users" WHERE "updated_at">'2024-11-01 00:00:00'
    Error: no such table: users



```python

```


---
**Score: 0**
