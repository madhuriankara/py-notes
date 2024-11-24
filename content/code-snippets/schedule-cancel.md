---
title: Schedule-Cancel
date: 2024-11-23
author: Your Name
cell_count: 8
score: 5
---

```python
!pip install schedule

```


```python
import schedule
import time


```


```python
# Define task function
def print_message():
    print("This job will be canceled.")
# Schedule the task to run every 2 seconds
job = schedule.every(2).seconds.do(print_message)

# Run the job for 5 seconds and then cancel it
time.sleep(5)
schedule.cancel_job(job)
print("Job has been canceled.")

# Keep the program running
while True:
    schedule.run_pending()
    time.sleep(1)

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
**Score: 5**
