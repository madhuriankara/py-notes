---
title: Job-No-Job
date: 2024-12-15
author: Your Name
cell_count: 5
score: 5
---

```python
#Group students by whether they got a job or not and count the number of students in each group.
```


```python
from google.cloud import bigquery
```


```python
client = bigquery.Client()
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)



```python
def query_bigquery():
    query = """
    SELECT got_job, COUNT(*) AS student_number FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    GROUP BY got_job;
    """
    result = client.query(query)
    print("Number of students grouped by job status:")
    for row in result:
        job_status = "Got Job" if row.got_job == 1 else "Did Not Get Job"
        print(f'{job_status}: {row.student_number} students')
  
query_bigquery()
```

    Number of students grouped by job status:
    Did Not Get Job: 50 students
    Got Job: 50 students



```python

```


---
**Score: 5**
