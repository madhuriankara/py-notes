---
title: Gdp-Capita-Region
date: 2024-12-15
author: Your Name
cell_count: 5
score: 5
---

```python
#Which region has the highest average GDP per capita
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
def get_highest_average():
    query = """
    SELECT region, AVG(gdp__per_capita) AS gdp_capita 
    FROM `plucky-order-444214-g8.student_data.country_table`
    GROUP BY region
    ORDER BY gdp_capita DESC
    """
    result = client.query(query)
    print("The top 5 most populated countries are:")
    for i in result:
        print(f'{i.region} - {i.gdp_capita}')

get_highest_average()
```

    The top 5 most populated countries are:
    WESTERN EUROPE                      - 27046.428571428572
    NORTHERN AMERICA                    - 26100.0
    BALTICS                             - 11300.0
    NEAR EAST                           - 10456.25
    EASTERN EUROPE                      - 9808.333333333334
    LATIN AMER. & CARIB     - 8682.22222222222
    OCEANIA                             - 8247.619047619048
    ASIA (EX. NEAR EAST)          - 8053.5714285714275
    NORTHERN AFRICA                     - 5460.0
    C.W. OF IND. STATES  - 4000.0
    SUB-SAHARAN AFRICA                  - 2323.529411764706



```python

```


---
**Score: 5**
