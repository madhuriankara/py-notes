---
title: Got-Job-1
date: 2025-01-13
author: Your Name
cell_count: 5
score: 5
---

```python
#Select students who have both high project scores (e.g., above 85) and got a job.
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
    SELECT student_name, project_scores, got_job FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    WHERE project_scores > 85 AND got_job = 1
    """
    result = client.query(query)
    print("result")
    
    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f'{i.student_name} - {i.project_scores}- {i.got_job}')
query_bigquery()
```

    result
    Top 10 GitHub repositories by commit count:
    Kevin Young - 87- 1
    Frank Morgan - 86- 1
    Frank Palmer - 86- 1
    John Doe - 88- 1
    Alexander Torres - 86- 1
    Steven Green - 88- 1
    Jeffrey Hughes - 87- 1
    Eric Morris - 87- 1
    Charles James - 87- 1
    James White - 86- 1
    Gregory Rivera - 88- 1
    Richard Ross - 88- 1
    Timothy Alexander - 88- 1
    Joseph Nelson - 86- 1
    Kevin Wallace - 88- 1
    George Phillips - 89- 1
    Eric Wallace - 89- 1
    Jacob Richardson - 89- 1
    Brandon Perry - 89- 1
    Matthew Walker - 90- 1
    Patrick Watson - 89- 1
    Stephen Foster - 88- 1
    Jason Stewart - 90- 1
    Michael Miller - 92- 1
    Benjamin Gray - 91- 1
    Ryan Coleman - 90- 1
    Joshua Wright - 90- 1
    Raymond Murphy - 90- 1
    Justin Long - 91- 1
    Mark Roberts - 91- 1
    Joshua Russell - 90- 1
    Keith Russell - 91- 1
    Timothy Reed - 91- 1
    Peter Sanders - 91- 1
    Bob Johnson - 90- 1
    Scott Howard - 91- 1
    Dennis Myers - 91- 1
    Edward Parker - 92- 1
    Gary Hamilton - 92- 1
    Chris Martin - 91- 1
    Paul Washington - 92- 1
    Andrew Baker - 93- 1



```python

```


---
**Score: 5**
