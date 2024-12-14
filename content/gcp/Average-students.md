---
title: Average-Students
date: 2024-12-13
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
        SELECT
        AVG(test_scores) as avg_test_score, 
        AVG(attendance) as avg_attendance,
        AVG(project_scores) as avg_project_scores
            FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    """
    query_job = client.query(query)
    print(query_job) 

    print("Top 10 GitHub repositories by commit count:")
    for row in query_job:
        print(f"Repository:{row.avg_test_score},{row.avg_attendance},{row.avg_project_scores}")

query_bigquery()
    
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)


    QueryJob<project=plucky-order-444214-g8, location=northamerica-northeast2, id=1f0ce1a3-de17-437b-b60d-82c8290981ce>
    Top 10 GitHub repositories by commit count:
    Repository:77.78999999999998,81.96000000000002,78.88999999999997



```python

```


---
**Score: 0**
