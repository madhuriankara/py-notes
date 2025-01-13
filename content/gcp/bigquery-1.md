---
title: Bigquery-1
date: 2025-01-13
author: Your Name
cell_count: 5
score: 5
---

```python
#!pip install google-cloud-bigquery

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
    # Initialize BigQuery client
    client = bigquery.Client()
    query = """
        SELECT student_name, participation FROM `plucky-order-444214-g8.student_data.student_data_madhuri` LIMIT 2
    """

    # Run the query
    query_job = client.query(query)
    print(query_job)

    # Fetch and print results
    print("Top 10 GitHub repositories by commit count:")
    for row in query_job:
        print(f"Repository: {row.student_name}")

# Run the example
query_bigquery()
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)


    QueryJob<project=plucky-order-444214-g8, location=northamerica-northeast2, id=97dd66f7-ce69-4cbd-ad5b-13d5d69ea0ed>
    Top 10 GitHub repositories by commit count:
    Repository: Amy Thomas
    Repository: Alice Flores



```python

```


---
**Score: 5**
