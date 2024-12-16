---
title: Student-Name-5
date: 2024-12-15
author: Your Name
cell_count: 5
score: 5
---

```python
#Filter students whose names contain exactly 5 letters.

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
    SELECT student_name, project_scores, got_job FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    WHERE LENGTH(student_name) = 10
    """
    result = client.query(query)
    print("result")
    
    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f'{i.student_name}')
query_bigquery()
```

    result
    Top 10 GitHub repositories by commit count:
    Amy Thomas
    Angela Cox
    Lisa Perez
    Linda Reed
    Mary Price
    Megan Ward
    Jane Smith
    Ronald Lee



```python

```


---
**Score: 5**
