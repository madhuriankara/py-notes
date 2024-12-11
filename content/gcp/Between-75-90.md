---
title: Between-75-90
date: 2024-12-10
author: Your Name
cell_count: 5
score: 5
---

```python
#Find students with test scores between 75 and 90.
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
    SELECT student_name, test_scores FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    WHERE test_scores BETWEEN 75 AND 90
    """
    result = client.query(query)
    print("result")
    
    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f'{i.student_name} - {i.test_scores}')
query_bigquery()
```

    result
    Top 10 GitHub repositories by commit count:
    Sarah Taylor - 75
    Sharon Cook - 75
    Sandra Turner - 76
    Jane Smith - 78
    Paul Mitchell - 82
    David Anderson - 82
    Justin Bennett - 83
    Ronald Lee - 83
    Daniel Lewis - 83
    Brian Edwards - 84
    Kenneth Butler - 84
    Kevin Young - 85
    Frank Morgan - 85
    Frank Palmer - 85
    John Doe - 85
    Alexander Torres - 85
    Steven Green - 86
    Jeffrey Hughes - 86
    Eric Morris - 86
    Charles James - 86
    James White - 87
    Gregory Rivera - 87
    Richard Ross - 87
    Timothy Alexander - 87
    Joseph Nelson - 88
    Kevin Wallace - 88
    George Phillips - 87
    Eric Wallace - 87
    Charlie Davis - 88
    Jacob Richardson - 88
    Brandon Perry - 88
    Matthew Walker - 89
    Patrick Watson - 89
    Stephen Foster - 89
    Jason Stewart - 89
    Michael Miller - 90
    Benjamin Gray - 90
    Ryan Coleman - 90
    Mark Roberts - 90



```python

```


---
**Score: 5**
