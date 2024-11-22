---
title: Untitled
date: 2024-11-22
author: Your Name
cell_count: 5
score: 5
---

Created on November 22, 2024

Course work: 

@author: Madhuri



```python
import pandas as pd
from pandas_datareader import data as pdr
import numpy as np
import datetime
```


```python
end = datetime.date.today()

begin=end-pd.DateOffset(365*10)

st=begin.strftime('%Y-%m-%d')

ed=end.strftime('%Y-%m-%d')


df = pdr.get_data_google("AAPL",st,ed)


no_of_std = 12



def bollinger_strat(df,window,std):
    rolling_mean = df['Close'].rolling(window).mean()
    rolling_std = df['Close'].rolling(window).std()

    df['Bollinger High'] = rolling_mean + (rolling_std * no_of_std)
    df['Bollinger Low'] = rolling_mean - (rolling_std * no_of_std)


data = [1, 2, 4, 5, 5, 3]

bollinger_strat(data,20,2)
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    Cell In[2], line 10
          5 st=begin.strftime('%Y-%m-%d')
          7 ed=end.strftime('%Y-%m-%d')
    ---> 10 df = pdr.get_data_google("AAPL",st,ed)
         13 no_of_std = 12
         17 def bollinger_strat(df,window,std):


    AttributeError: module 'pandas_datareader.data' has no attribute 'get_data_google'



```python

```


```python

```


---
**Score: 5**
