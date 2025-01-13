---
title: Five-Populated-Countries
date: 2025-01-13
author: Your Name
cell_count: 5
score: 5
---

```python
#What is the population of the top 5 most populated countries?
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
def get_populated_countries():
    query = """
    SELECT country, population FROM `plucky-order-444214-g8.student_data.country_table`
    ORDER BY population DESC
    
    LIMIT 5;
    
"""
    result = client.query(query)
    print("The top 5 most populated countries are:")
    for i in result:
        print(f'{i.country} - {i.population}')

get_populated_countries()
```

    The top 5 most populated countries are:
    China  - 1313973713
    India  - 1095351995
    United States  - 298444215
    Indonesia  - 245452739
    Brazil  - 188078227



```python

```


---
**Score: 5**
