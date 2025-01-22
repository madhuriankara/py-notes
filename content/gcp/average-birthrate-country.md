---
title: Average-Birthrate-Country
date: 2025-01-22
author: Your Name
cell_count: 5
score: 5
---

```python
#What is the average birthrate for countries in each climate type?
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
def get_average_birthrate():
    query = """
    SELECT climate,
    AVG(birthrate) AS birthrate,
    FROM `plucky-order-444214-g8.student_data.country_table` 
    GROUP BY climate;
    """
    result = client.query(query)
    print("The average birthrate of countries in each climate type is:")
    for i in result:
        print(f'{i.climate} - {i.birthrate}')

get_average_birthrate()
```

    The average birthrate of countries in each climate type is:
    None - 1576.0
    1 - 2401.1428571428573
    2 - 2402.7454545454552
    3 - 1288.333333333333
    4 - 906.0
    15 - 2563.9999999999995
    25 - 1723.3333333333333



```python

```


---
**Score: 5**
