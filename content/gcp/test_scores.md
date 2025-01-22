---
title: Test Scores
date: 2025-01-22
author: Your Name
cell_count: 5
score: 5
---

```python
#Get all students whoever got more than 90
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
    client = bigquery.Client()
    query = """
        SELECT student_name,test_scores FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
        WHERE test_scores > 90
    """
    query_job = client.query(query)
    print(query_job) 

    print("Top 10 GitHub repositories by commit count:")
    for row in query_job:
        print(f"Repository: {row.student_name} - {row.test_scores}")

query_bigquery()
    
    
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)


    QueryJob<project=plucky-order-444214-g8, location=northamerica-northeast2, id=c6e6c21d-6f64-4fe4-8301-76cdbf485e93>
    Top 10 GitHub repositories by commit count:
    Repository: Joshua Wright - 91
    Repository: Raymond Murphy - 91
    Repository: Justin Long - 91
    Repository: Joshua Russell - 91
    Repository: Keith Russell - 91
    Repository: Timothy Reed - 92
    Repository: Peter Sanders - 92
    Repository: Bob Johnson - 92
    Repository: Scott Howard - 92
    Repository: Dennis Myers - 92
    Repository: Edward Parker - 93
    Repository: Gary Hamilton - 93
    Repository: Chris Martin - 94
    Repository: Paul Washington - 94
    Repository: Andrew Baker - 95



```python

```


---
**Score: 5**
