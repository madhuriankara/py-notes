---
title: Correlation
date: 2025-01-06
author: Your Name
cell_count: 5
score: 5
---

```python
#What is the correlation between GDP per capita and literacy rate?
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
def get_correlation():
    query = """
    SELECT CORR(`gdp__per_capita`, literacy_) AS correlation
FROM `plucky-order-444214-g8.student_data.country_table` 
    """
    result = client.query(query)
    print("The correlation between gdp and literacy is")
    for i in result:
        print(f'{i.correlation}')

get_correlation()
```

    The correlation between gdp and literacy is
    0.5131435413092706



```python

```


---
**Score: 5**
