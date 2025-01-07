---
title: Divisible-By-5
date: 2025-01-06
author: Your Name
cell_count: 5
score: 5
---

```python
#Identify students whose participation scores are exactly divisible by 5.
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
    WHERE MOD(participation, 5) = 0
    """
    result = client.query(query)
    print("result")
    
    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f'{i.student_name} - {i.participation}')
query_bigquery()
```

    result
    Top 10 GitHub repositories by commit count:
    Amy Thomas - 55
    Barbara King - 60
    Dorothy Rogers - 60
    Laura Simmons - 60
    Emily Wilson - 60
    Karen Kelly - 65
    Nancy Sanchez - 65
    Patricia Hall - 70
    Megan Ward - 70
    Alice Brown - 70
    Jane Smith - 75
    Paul Mitchell - 80
    David Anderson - 80
    Justin Bennett - 80
    Ronald Lee - 80
    John Doe - 80
    Gregory Rivera - 85
    George Phillips - 85
    Eric Wallace - 85
    Matthew Walker - 85
    Patrick Watson - 85
    Stephen Foster - 85
    Bob Johnson - 85
    Andrew Baker - 90



```python

```


---
**Score: 5**
