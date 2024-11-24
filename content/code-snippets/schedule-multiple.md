---
title: Schedule-Multiple
date: 2024-11-24
author: Your Name
cell_count: 10
score: 10
---

```python

```


```python

```


```python


```


```python
import schedule
import time

# Define task functions
def task_1():
    print("Task 1: Running every 5 seconds")

def task_2():
    print("Task 2: Running every 10 seconds")

# Schedule tasks
schedule.every(5).seconds.do(task_1)
schedule.every(10).seconds.do(task_2)

# Keep the program running
while True:
    schedule.run_pending()  # Run all pending tasks
    time.sleep(1)  # Wait for 1 second


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
