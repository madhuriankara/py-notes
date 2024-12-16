---
title: Participation-More-Test-Scores
date: 2024-12-15
author: Your Name
cell_count: 5
score: 5
---

```python
#Select students who scored higher in participation than in their test scores.
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
    SELECT student_name, participation, test_scores FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    WHERE participation > test_scores
    """
    result = client.query(query)
    print("result")
    
    print("Here is the result")
    for i in result:
        print(f'{i.student_name} - {i.participation} - {i.test_scores}')
query_bigquery()
```

    result
    Here is the result



```python

```


---
**Score: 5**
