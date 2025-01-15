---
title: Highest-Net-Migration-Rate
date: 2025-01-15
author: Your Name
cell_count: 5
score: 5
---

```python
#Which country has the highest net migration rate?
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
def get_highest_migration_rate():
    query = """
    SELECT country,
    net_migration,
    FROM `plucky-order-444214-g8.student_data.country_table` 
    ORDER BY net_migration DESC

    LIMIT 1;
    """
    result = client.query(query)
    print("The country with highest net migrate rate is:")
    for i in result:
        print(f'{i.country} - {i.net_migration}')

get_highest_migration_rate()
```

    The country with highest net migrate rate is:
    Afghanistan  - 2306



```python

```


---
**Score: 5**
