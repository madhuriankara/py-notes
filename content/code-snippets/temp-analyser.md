---
title: Temp-Analyser
date: 2024-12-23
author: Your Name
cell_count: 11
score: 10
---

```python

```


```python
!pip install selenium
```

    Requirement already satisfied: selenium in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (4.26.1)
    Requirement already satisfied: urllib3<3,>=1.26 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from urllib3[socks]<3,>=1.26->selenium) (2.2.3)
    Requirement already satisfied: trio~=0.17 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from selenium) (0.27.0)
    Requirement already satisfied: trio-websocket~=0.9 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from selenium) (0.11.1)
    Requirement already satisfied: certifi>=2021.10.8 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from selenium) (2024.8.30)
    Requirement already satisfied: typing_extensions~=4.9 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from selenium) (4.12.2)
    Requirement already satisfied: websocket-client~=1.8 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from selenium) (1.8.0)
    Requirement already satisfied: attrs>=23.2.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio~=0.17->selenium) (24.2.0)
    Requirement already satisfied: sortedcontainers in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio~=0.17->selenium) (2.4.0)
    Requirement already satisfied: idna in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio~=0.17->selenium) (3.10)
    Requirement already satisfied: outcome in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio~=0.17->selenium) (1.3.0.post0)
    Requirement already satisfied: sniffio>=1.3.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio~=0.17->selenium) (1.3.1)
    Requirement already satisfied: wsproto>=0.14 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from trio-websocket~=0.9->selenium) (1.2.0)
    Requirement already satisfied: pysocks!=1.5.7,<2.0,>=1.5.6 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from urllib3[socks]<3,>=1.26->selenium) (1.7.1)
    Requirement already satisfied: h11<1,>=0.9.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from wsproto>=0.14->trio-websocket~=0.9->selenium) (0.14.0)



```python
from bs4 import BeautifulSoup
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.select import Select
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import os
```


```python
filename = "temp_emails.txt"
```


```python
email_map = {}

def get_email():
    
    phantomjs_path = r'C:\Phantom\phantomjs-2.1.1-windows\bin\phantomjs.exe';
    driver = webdriver.PhantomJS(phantomjs_path)
    wait = WebDriverWait(driver, 10)

    url = 'https://temp-mail.org/'
    driver.get(url)

    #print(driver);

    pagehtml = driver.page_source;
    soup = BeautifulSoup(pagehtml, "html5lib")
    emailInput = soup.find('input', {"class": "mail"});
    print(emailInput.get('value'));
    #print()
    return emailInput.get('value')
```


```python
def storeEmailInFile(email, localFilename):
    hs = open(localFilename,"a")
    if(os.path.getsize(localFilename) > 0):
        hs.write("\n"+email)
    else:
        hs.write(email)

    hs.close()
```


```python
def get_dummy_emails():
    for x in range(10):
        email = get_email()
        
        storeEmailInFile(email, filename)
```


```python
def read_email_file(localFilename):
    f = open(localFilename)

    for line in f.readlines():
        email = line.strip()
        
        username = email.split('@')[0]
        domain = email.split('@')[1]
        print(domain)
        
        if(domain in email_map):
            email_map[domain] += 1
        else:
            email_map[domain] = 0

read_email_file(filename)

print(email_map)
```

    example.com
    testmail.com
    domain.com
    mailbox.org
    fastmail.com
    outlook.com
    protonmail.com
    gmail.com
    yahoo.com
    customdomain.net
    {'69postix.info\\n",': 31, 'kumail8.info\\n",': 29, 'youzend.net\\n",': 31, 'ugimail.net\\n",': 27, 'endrix.org\\n",': 31, 'cryp.email\\n",': 33, '0mixmail.info\\n",': 36, 'crypemail.info\\n",': 23, '20boxme.org\\n",': 30, 'send22u.info\\n",': 38, 'mail4-us.org\\n",': 29, 'kumail8.info"': 0, 'example.com': 3, 'testmail.com': 3, 'domain.com': 3, 'mailbox.org': 3, 'fastmail.com': 3, 'outlook.com': 3, 'protonmail.com': 3, 'gmail.com': 3, 'yahoo.com': 3, 'customdomain.net': 3}



```python

```


```python

```


```python

```


---
**Score: 10**
