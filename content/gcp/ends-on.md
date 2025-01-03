---
title: Ends-On
date: 2025-01-03
author: Your Name
cell_count: 6
score: 5
---

```python
#Filter students whose names end with "on".
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
        SELECT student_name FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
        WHERE student_name LIKE '%on'
        """
    result = client.query(query)
    print("result")

    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f"Repository:{i.student_name}")
query_bigquery()
    
```

    result
    Top 10 GitHub repositories by commit count:
    Repository:Emily Wilson
    Repository:Stephanie Peterson
    Repository:Jessica Robinson
    Repository:Stephanie Henderson
    Repository:Christina Patterson
    Repository:David Anderson
    Repository:Joseph Nelson
    Repository:Jacob Richardson
    Repository:Patrick Watson
    Repository:Bob Johnson
    Repository:Gary Hamilton
    Repository:Paul Washington



```python

```


```python

```


---
**Score: 5**
