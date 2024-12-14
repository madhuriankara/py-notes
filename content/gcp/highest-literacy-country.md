---
title: Highest-Literacy-Country
date: 2024-12-13
author: Your Name
cell_count: 5
score: 5
---

```python
#Which country has the highest literacy rate?
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
def get_highest_literacy_rate():
    query = """
    SELECT country,literacy_ 
    FROM `plucky-order-444214-g8.student_data.country_table`
    ORDER BY literacy_ DESC

    LIMIT 1;
    """
    result = client.query(query)
    print("The country with highest literacy is:")
    for i in result:
        print(f'{i.country} - {i.literacy_}')

get_highest_literacy_rate()
```

    The country with highest literacy is:
    Luxembourg  - 1000



```python

```


---
**Score: 5**
