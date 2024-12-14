---
title: Score-Greater-Than-250
date: 2024-12-13
author: Your Name
cell_count: 6
score: 5
---

```python
#List students who have a total score (sum of test, participation, and project scores) above 250.
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
        SELECT
            student_name,
            test_scores,
            participation,
            project_scores,
            (test_scores + participation + project_scores) AS total_score
        FROM
            `plucky-order-444214-g8.student_data.student_data_madhuri`
        WHERE
            (test_scores + participation + project_scores) > 250
        ORDER BY
            total_score DESC;
    """
    
    # Execute the query
    result = client.query(query)

    print("Students with total scores above 250:")
    for row in result:
        print(f"{row.student_name} - Total Score: {row.total_score}")

query_bigquery()
```

    Students with total scores above 250:
    Andrew Baker - Total Score: 278
    Paul Washington - Total Score: 275
    Edward Parker - Total Score: 274
    Gary Hamilton - Total Score: 274
    Chris Martin - Total Score: 274
    Scott Howard - Total Score: 272
    Timothy Reed - Total Score: 271
    Peter Sanders - Total Score: 271
    Dennis Myers - Total Score: 271
    Michael Miller - Total Score: 270
    Justin Long - Total Score: 269
    Mark Roberts - Total Score: 269
    Keith Russell - Total Score: 269
    Benjamin Gray - Total Score: 268
    Joshua Wright - Total Score: 268
    Joshua Russell - Total Score: 268
    Raymond Murphy - Total Score: 267
    Bob Johnson - Total Score: 267
    Jason Stewart - Total Score: 266
    Ryan Coleman - Total Score: 266
    Matthew Walker - Total Score: 264
    Patrick Watson - Total Score: 263
    Stephen Foster - Total Score: 262
    George Phillips - Total Score: 261
    Eric Wallace - Total Score: 261
    Jacob Richardson - Total Score: 261
    Brandon Perry - Total Score: 261
    Gregory Rivera - Total Score: 260
    Kevin Wallace - Total Score: 260
    Richard Ross - Total Score: 259
    Timothy Alexander - Total Score: 259
    Joseph Nelson - Total Score: 258
    Steven Green - Total Score: 257
    Eric Morris - Total Score: 257
    James White - Total Score: 257
    Jeffrey Hughes - Total Score: 256
    Charles James - Total Score: 256
    Charlie Davis - Total Score: 256
    Kevin Young - Total Score: 254
    Frank Morgan - Total Score: 253
    Frank Palmer - Total Score: 253
    John Doe - Total Score: 253
    Alexander Torres - Total Score: 252
    Brian Edwards - Total Score: 251
    Kenneth Butler - Total Score: 251



```python

```


```python

```


---
**Score: 5**
