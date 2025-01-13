---
title: Attendance-Less-Than-85
date: 2025-01-13
author: Your Name
cell_count: 4
score: 0
---

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
    SELECT student_name, attendance FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    WHERE attendance < 85
    """
    result = client.query(query)
    print("result")
    
    print("Top 10 GitHub repositories by commit count:")
    for i in result:
        print(f'{i.student_name} - {i.attendance}')
query_bigquery()
```

    result
    Top 10 GitHub repositories by commit count:
    Amy Thomas - 65
    Alice Flores - 65
    Sharon Woods - 65
    Karen Campbell - 65
    Angela Cox - 66
    Elizabeth Hayes - 66
    Barbara King - 66
    Dorothy Rogers - 67
    Victoria Brooks - 67
    Debra Jenkins - 67
    Donna Adams - 68
    Laura Simmons - 68
    Lisa Perez - 69
    Michelle Bell - 69
    Dorothy Barnes - 69
    Rebecca West - 69
    Emily Wilson - 70
    Deborah Collins - 70
    Stephanie Peterson - 70
    Janet Powell - 70
    Christine Barnes - 70
    Jessica Robinson - 70
    Mary Carter - 70
    Emily Cooper - 71
    Ann Griffin - 71
    Karen Kelly - 71
    Linda Reed - 71
    Laura Clark - 72
    Nancy Sanchez - 72
    Amanda Price - 73
    Diane Gonzalez - 73
    Stephanie Henderson - 74
    Rachel Gonzalez - 74
    Kimberly Bailey - 75
    Heather Bryant - 75
    Patricia Hall - 75
    Mary Price - 75
    Megan Ward - 76
    Rebecca Evans - 76
    Margaret Stone - 77
    Linda Harris - 77
    Christina Patterson - 78
    Betty Scott - 79
    Samantha Ramirez - 79
    Tina Coleman - 79
    Alice Brown - 80
    Sarah Taylor - 80
    Sharon Cook - 80
    Sandra Turner - 81



```python

```


---
**Score: 0**
