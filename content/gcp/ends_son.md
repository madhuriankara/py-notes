---
title: Ends Son
date: 2024-12-15
author: Your Name
cell_count: 4
score: 0
---

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
    client = bigquery.Client()
    query = """
        SELECT student_name FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
        WHERE student_name Like '%son'
    """
    query_job = client.query(query)
    print(query_job) 

    print("Top 10 GitHub repositories by commit count:")
    for row in query_job:
        print(f"Repository: {row.student_name}")

query_bigquery()
    
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)


    QueryJob<project=plucky-order-444214-g8, location=northamerica-northeast2, id=23c0f535-592c-41f8-9eb0-2207c0c8d07a>
    Top 10 GitHub repositories by commit count:
    Repository: Emily Wilson
    Repository: Stephanie Peterson
    Repository: Jessica Robinson
    Repository: Stephanie Henderson
    Repository: Christina Patterson
    Repository: David Anderson
    Repository: Joseph Nelson
    Repository: Jacob Richardson
    Repository: Patrick Watson
    Repository: Bob Johnson



```python

```


---
**Score: 0**
