---
title: Country-Population
date: 2025-01-22
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
def get_country_population():
    query = """
    SELECT population, 
           country
    FROM `plucky-order-444214-g8.student_data.country_table`
    WHERE country = 'Russia '
    """
    result = client.query(query)
    
    print("The population of the country:")
    for i in result:
        print(f'{i.country} - {i.population}')

get_country_population()
        
```

    The population of the country:
    Russia  - 142893540



```python

```


---
**Score: 0**
