---
title: Greater-Than-80
date: 2025-01-06
author: Your Name
cell_count: 5
score: 5
---

```python
#Find students with test scores greater than 80.
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
    WHERE test_scores > 80
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
    Joshua Wright - 91
    Raymond Murphy - 91
    Justin Long - 91
    Mark Roberts - 90
    Joshua Russell - 91
    Keith Russell - 91
    Timothy Reed - 92
    Peter Sanders - 92
    Bob Johnson - 92
    Scott Howard - 92
    Dennis Myers - 92
    Edward Parker - 93
    Gary Hamilton - 93
    Chris Martin - 94
    Paul Washington - 94
    Andrew Baker - 95



```python

```


---
**Score: 5**
