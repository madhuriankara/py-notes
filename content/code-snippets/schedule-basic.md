---
title: Schedule-Basic
date: 2025-01-15
author: Your Name
cell_count: 11
score: 10
---

```python
import schedule
import time

# Define the task function
def job():
    print("Job is running!")

# Schedule the job to run every 2 seconds
schedule.every(2).seconds.do(job)

# Keep the program running
while True:
    schedule.run_pending()  # Run all pending tasks
    time.sleep(1)  # Wait for 1 second

```

    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!
    Job is running!



```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


---
**Score: 10**
