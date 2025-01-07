---
title: Country-Gdp
date: 2025-01-06
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
def get_gdp_by_country():
    query = """
    SELECT  country,gdp__per_capita FROM `plucky-order-444214-g8.student_data.country_table` 
    WHERE gdp__per_capita > 9000
    """
    result = client.query(query)
    print("The GDP above 9000:")
    for i in result:
        print(f'{i.country} - {i.gdp__per_capita}')

get_gdp_by_country()
```

    The GDP above 9000:
    Lithuania  - 11400.0
    Croatia  - 10600.0
    Slovenia  - 19000.0
    Canada  - 29800.0
    Faroe Islands  - 22000.0
    Gibraltar  - 17500.0
    Italy  - 26700.0
    Luxembourg  - 55100.0
    Malta  - 17700.0
    Monaco  - 27000.0
    San Marino  - 34600.0
    Bahrain  - 16900.0
    Kuwait  - 19000.0
    Oman  - 13100.0
    Qatar  - 21500.0
    Saudi Arabia  - 11800.0
    United Arab Emirates  - 23200.0
    Greenland  - 20000.0
    Australia  - 29000.0
    South Africa  - 10700.0
    Antigua & Barbuda  - 11000.0
    Aruba  - 28000.0
    Bahamas, The  - 16700.0
    Barbados  - 15700.0
    British Virgin Is.  - 16000.0
    Cayman Islands  - 35000.0
    Costa Rica  - 9100.0
    Martinique  - 14400.0
    Netherlands Antilles  - 11400.0
    Puerto Rico  - 16800.0
    Trinidad & Tobago  - 9500.0
    Turks & Caicos Is  - 9600.0
    Virgin Islands  - 17200.0
    Brunei  - 18600.0
    Hong Kong  - 28800.0
    Macau  - 19400.0
    Singapore  - 23700.0
    Taiwan  - 23400.0
    Bermuda  - 36000.0
    French Polynesia  - 17500.0
    Guam  - 21000.0
    New Caledonia  - 15000.0
    N. Mariana Islands  - 12500.0
    Mauritius  - 11400.0
    Argentina  - 11200.0
    Chile  - 9900.0
    Uruguay  - 12800.0
    Japan  - 28200.0
    Korea, South  - 17800.0
    Estonia  - 12300.0
    Latvia  - 10200.0
    Czech Republic  - 15700.0
    Hungary  - 13900.0
    Poland  - 11100.0
    Slovakia  - 13300.0
    Cyprus  - 19200.0
    Israel  - 19800.0
    United States  - 37800.0
    New Zealand  - 21600.0
    Andorra  - 19000.0
    Austria  - 30000.0
    Belgium  - 29100.0
    Denmark  - 31100.0
    Finland  - 27400.0
    Germany  - 27600.0
    Greece  - 20000.0
    Guernsey  - 20000.0
    Iceland  - 30900.0
    Ireland  - 29600.0
    Isle of Man  - 21000.0
    Jersey  - 24800.0
    Netherlands  - 28600.0
    Norway  - 37800.0
    Portugal  - 18000.0
    Spain  - 22000.0
    Sweden  - 26800.0
    Switzerland  - 32700.0
    United Kingdom  - 27700.0
    France  - 27600.0
    Liechtenstein  - 25000.0



```python

```


---
**Score: 0**
