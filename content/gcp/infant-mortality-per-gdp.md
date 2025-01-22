---
title: Infant-Mortality-Per-Gdp
date: 2025-01-22
author: Your Name
cell_count: 5
score: 5
---

```python
#What is the infant mortality rate for countries with GDP per capita above $50,000?
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
def get_infant_mortality_rate():
    query = """
    SELECT country,
    infant_mortality_per_1000_births,
    gdp__per_capita
    FROM `plucky-order-444214-g8.student_data.country_table` 
    WHERE gdp__per_capita > 50000;
    
    """
    result = client.query(query)
    print("The infant mortality rate for countries with GDP above 50000 is")
    for i in result:
        print(f'{i.country} -  {i.infant_mortality_per_1000_births} - { i.gdp__per_capita}')

get_infant_mortality_rate()
```

    The infant mortality rate for countries with GDP above 50000 is
    Luxembourg  -  481 - 55100.0



```python

```


---
**Score: 5**
