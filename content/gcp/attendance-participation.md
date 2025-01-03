---
title: Attendance-Participation
date: 2025-01-03
author: Your Name
cell_count: 6
score: 5
---

```python
#Identify students with attendance below 75% but participation above 80.
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
    SELECT student_name,attendance, participation FROM `plucky-order-444214-g8.student_data.student_data_madhuri`
    WHERE attendance < 75 AND participation > 80 
    ORDER BY participation DESC;
    """
    result = client.query(query)
    print("Students with attendance and participation score:")
    for i in result:
        print(f'{i.student_name} - {i.attendance} - {i.participation}')

query_bigquery()
```

    Students with attendance and participation score:



```python

```


```python

```


---
**Score: 5**
