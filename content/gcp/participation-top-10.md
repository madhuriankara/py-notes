---
title: Participation-Top-10
date: 2024-12-23
author: Your Name
cell_count: 5
score: 5
---

```python
#Sort students in descending order of their participation scores and list the top 10.
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
    SELECT student_name, participation FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    ORDER BY participation DESC
    LIMIT 10;
    """
    result = client.query(query)
    print("The students in descending order")
    for i in result:
        print(f'{i.student_name} - {i.participation}')
query_bigquery()
```

    The students in descending order
    Andrew Baker - 90
    Gary Hamilton - 89
    Paul Washington - 89
    Edward Parker - 89
    Chris Martin - 89
    Scott Howard - 89
    Mark Roberts - 88
    Michael Miller - 88
    Dennis Myers - 88
    Peter Sanders - 88



```python

```


---
**Score: 5**
