---
title: Total-Score-80
date: 2025-01-06
author: Your Name
cell_count: 5
score: 5
---

```python
#Find students who got a job and have all scores (test, participation, and project) above 80.
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
    SELECT student_name,
    got_job,
    test_scores,
    participation,
    project_scores,
   (test_scores + participation + project_scores) AS total_score 
    FROM `plucky-order-444214-g8.student_data.student_data_madhuri`
    WHERE (test_scores + participation + project_scores) > 80 AND got_job = 1
    ORDER BY total_score ASC;
    """
    result = client.query(query)
    print("The total score of students above 80 are:")
    for i in result:
        print(f'{i.student_name} - {i.total_score} - {i.got_job}')
query_bigquery()
    
```

    The total score of students above 80 are:
    Paul Mitchell - 245 - 1
    David Anderson - 246 - 1
    Ronald Lee - 246 - 1
    Justin Bennett - 247 - 1
    Daniel Lewis - 249 - 1
    Brian Edwards - 251 - 1
    Kenneth Butler - 251 - 1
    Alexander Torres - 252 - 1
    Frank Morgan - 253 - 1
    Frank Palmer - 253 - 1
    John Doe - 253 - 1
    Kevin Young - 254 - 1
    Jeffrey Hughes - 256 - 1
    Charles James - 256 - 1
    Charlie Davis - 256 - 1
    Steven Green - 257 - 1
    Eric Morris - 257 - 1
    James White - 257 - 1
    Joseph Nelson - 258 - 1
    Richard Ross - 259 - 1
    Timothy Alexander - 259 - 1
    Gregory Rivera - 260 - 1
    Kevin Wallace - 260 - 1
    George Phillips - 261 - 1
    Eric Wallace - 261 - 1
    Jacob Richardson - 261 - 1
    Brandon Perry - 261 - 1
    Stephen Foster - 262 - 1
    Patrick Watson - 263 - 1
    Matthew Walker - 264 - 1
    Jason Stewart - 266 - 1
    Ryan Coleman - 266 - 1
    Raymond Murphy - 267 - 1
    Bob Johnson - 267 - 1
    Benjamin Gray - 268 - 1
    Joshua Wright - 268 - 1
    Joshua Russell - 268 - 1
    Justin Long - 269 - 1
    Mark Roberts - 269 - 1
    Keith Russell - 269 - 1
    Michael Miller - 270 - 1
    Timothy Reed - 271 - 1
    Peter Sanders - 271 - 1
    Dennis Myers - 271 - 1
    Scott Howard - 272 - 1
    Edward Parker - 274 - 1
    Gary Hamilton - 274 - 1
    Chris Martin - 274 - 1
    Paul Washington - 275 - 1
    Andrew Baker - 278 - 1



```python

```


---
**Score: 5**
